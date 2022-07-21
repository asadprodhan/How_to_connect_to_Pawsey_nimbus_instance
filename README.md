# **How to connect to Pawsey’s Nimbus Instance** <br />


## **Background**


Bioinformatics research inevitably requires a powerful computing facility. This is because Bioinformatics analysis involves a large sequence dataset. Pawsey Supercomputer Centre, Perth, offers a great solution to it. The centre provides with a custom-tailored computing infrastructure to all Australian researchers. It also has a strong support team comprised of professional Bioinformaticians to help researchers along with their computing journey.



Pawsey Supercomputer Centre has two types of computing facilities- high performance computing (HPC) and cloud based virtual machine called ‘Nimbus Instance’. 



Here, I outline the steps to get connected to Pawsey's ‘Nimbus Instance’.



## **Method**


**Step 1: Make an application to have access to ‘Nimbus Instance’ (https://apply.pawsey.org.au/)**


**Step 2: Log in into https://nimbus.pawsey.org.au and build an instance**


As a part of this step, you will generate ‘a key pair’ that will be required for ssh connection via any ‘secure shell (ssh)’ client (software) (https://support.pawsey.org.au/documentation/display/US/Create+a+Nimbus+Instance) 



**Step 3: Attach a storage volume to your Instance**


Instructions are here:


https://support.pawsey.org.au/documentation/display/US/Attach+a+Storage+Volume



**Step 4: Access your Instance through a ssh client**



To access the Pawsey’s Nimbus Instance, see the instructions in the following link:


https://support.pawsey.org.au/documentation/display/US/Access+and+Use+Your+Nimbus+Instance#AccessandUseYourNimbusInstance-LoginviaWindowswithPuTTY


## **Note:**


- In your Instance, you have two IP addresses: one Instance-specific and one external. You need the external IP address in this step


- You need to add an inbound and outbound rule for Port 22 to your local computer’s firewall


- Pay attention to the remote host name. It is not just the IP address but ubuntu@IP_address



**Here is an example of connecting to Pawsey’s Ubuntu Instance using MobaXterm:**



- See the MobaXterm screenshot below (Fig. 1)


- Enter remote host as


```
ssh ubuntu@Public_external_IP_for_your_instance
```


- Tick the ‘Specify username’ box. It is the username that you use to log in into your Nimbus Instance website (dashboard)



- Tick the ‘Use private key’ box. Browse to your key. It is a file with ‘.pem’ extension. Select it and press OK.



**Now, ssh connection established and you can use your Instance**


<br />
<br />
<p align="center">
  <img 
    src="https://github.com/asadprodhan/How_to_connect_to_Pawsey_nimbus_instance/blob/main/MobaXterm_ssh_host_address.PNG"
  >
<p align = "center">
Figure 1. ssh connection to Nimbus Instance via MobaXterm
</p>
<br />
<br />



**Step 5: Transfer your data to your Instance that you want to analyse**



**Data can be transferred back and forth between your ‘local computer’ and ‘Instance’ using one of the following options:**


- command line in your shell


- MobaXterm’s drag and drop function, or


- a software, for example, WinSCP, FileZila etc.



## **How to use FileZilla for transferring data?**



You need to download it and log in into it with the following details:


> Host: same as Step 4, Username and Password: same as your Pawsey account, Port: 22, Passphrase: the one that you have generated with Putty at Step 4


*** The End***

