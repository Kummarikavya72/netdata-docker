# netdata-docker
1. Launched EC2 instance (Amazon Linux)
2. Opened ports 22 (SSH), 80 (HTTP), and 19999 (Netdata) in Security Group
3. Installed Docker using:
   sudo yum install docker -y
4. Started Docker and enabled it:
   sudo systemctl start docker
   sudo systemctl enable docker
5. Pulled and ran Netdata container using:
   sudo docker run -d --name=netdata -p 19999:19999 --cap-add=SYS_PTRACE --security-opt apparmor=unconfined netdata/netdata
6. Accessed dashboard in browser at:
   http://<public-ip>:19999
this is how i complted task 5 know i will add the screenshots below
dashboard link ![image](https://github.com/user-attachments/assets/020c4226-0111-4a32-991d-dfbd46ee915e)
![image](https://github.com/user-attachments/assets/140cf302-8772-4837-87f0-bbf206ce951a)
image of logs ![image](https://github.com/user-attachments/assets/2af49613-3b7a-4a4e-94ea-7df269735de5)
I saw charts for CPU usage, RAM, network, and disk performance.
It also showed details about my Docker containers.
Netdata updates every second and gives real-time stats.
