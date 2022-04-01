# Task 3.2 Connecting individual networks using the Internet and VLAN settings.
![screen1](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m3/task3.2/screen/screen1.png)

# Checked the connection of computers to their own gateways with the ping command.
![screen2](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m3/task3.2/screen/screen2.png)
![screen3](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m3/task3.2/screen/screen3.png)
![screen4](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m3/task3.2/screen/screen4.png)

# VLAN settings in the Data Center.
### Checked the connection between the servers using the ping command and the route of the packet using tracert.
![screen5](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m3/task3.2/screen/screen5.png)
### Changed subnet mask on servers to 255.255.255.192 and Checked the connection between the servers using the ping command and the route of the packet using tracert again.
![screen6](https://github.com/NikPryvalov/DevOps_online_Kharkiv_2022Q1Q2/blob/main/m3/task3.2/screen/screen6.png)
#### And now ping and traceroute success on 2.21.83.1 (default gateway), but unsuccessful on endpoint devices. This explain because network with mask /26 include only 62 hosts. Our servers with addresses 100 and 150 - out of limits, of the network.
