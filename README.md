<h1>Configuring NetFlow</h1>


<h2>Description</h2>
In this lab, I learned to configure NetFlow. NetFlow is a software system that seeks to collect key network traffic information (statistics) and, most commonly, send these statistics to a central network collector.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 
- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click PuTTY SSH Client and proceed to put in the IP address, port number, click Telnet and then click open: <br/>
<img src="https://i.postimg.cc/tgxTkMBH/Screen-Shot-2022-08-14-at-6-58-42-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the R1 terminal window type the following commands <br/>
1. configure terminal <br/>
2. ip flow-export version 9 <br/>
3. ip flow-export destination 192.168.0.100 9999 <br/>
4. interface e0/0 <br/>
5. ip flow ingress <br/>
6. ip flow egress <br/>
7. end <br/>
<img src="https://i.postimg.cc/Y00Yrw6m/Screen-Shot-2022-08-14-at-7-03-33-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the R1 terminal window type "show ip flow interface" command to display the NetFlow accounting configuration for interfaces<br/>
Then type the "show ip flow export" command to displays the status and statistics for NetFlow accounting data export <br/>
<img src="https://i.postimg.cc/t4JrJL5y/Screen-Shot-2022-08-14-at-7-05-29-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />






  
  
 

  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
