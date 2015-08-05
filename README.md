Author  : CarbonSphere <br>
Email   : carbonsphere@gmail.com<br>

<h2>Docker Easy RSA</h2>

<h4>docker pull carbonsphere/dock-easy-rsa</h4>
<h4>git clone https://github.com/carbonsphere/dock-easy-rsa.git</h4>

<h3>RUN Procedure</h3>

  - Pull required container
    1. docker pull carbonsphere/docker-easy-rsa

    2. get example from github "git clone https://github.com/carbonsphere/dock-easy-rsa.git"

    3. cd dock-easy-rsa/example
       Create "vars" or you can use default by "cp vars.example vars"

    4. Edit default variables in "vars" file

    5. Initialize CA certificate and server certificate
       "./gen_ca_init.sh"

    Note: This script will create CA & Server certificates/keys & DH2048 and copy it into directory "openvpn"
    Warning: This script will also clear all directories "keys" & "openvpn". Since it is only necessary to run it once for your CA server.
    Note: A signed CA certificate can also be used by replacing it in "keys" directory.

    6. Create Client Certificate and key
       "./gen_client.sh"

    Note: This will ask for client name and after creation, it will put all necessary files into directory "{entered_client_name}" 

The goal of this container is to allow you to manage and generate server/client certificates and keys without installing all the mumbo jumbo. It categorize all functions into server/client certificate generation scripts.





