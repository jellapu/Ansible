---
ssh -i ~\downlo\ansible_ley.pem ubuntu@publicip
sudo apt update
sudo apt install openjdk-11-jdk -y
sudo useradd spc/usr/share/spc/spring-petclinic.jar   #ask this doubt
sudo mkdir /usr/share/spc
cd /usr/share/spc/
wget url petclinic
sudo wget url petclinic
sudo mv spring-petclinic-2.4.2.jar spring -petclinic.jar
cd ..
sudo chown spc:spc spc/
cd spc/
sudo chown spc:spc spring-petclincic.jar
sudo chmod 500 /usr/share/spc/spring-petclinic.jar
sudo vi /etc/systemd/system/spc.service

---
[Unit]
Description=Spring petclinic application
After=network.target

[Service]

User=spc
ExecStart=/usr/bin/java -jar /usr/share/spc/spring-petclinic.jar SuccessExitStatus=143

[Install]
WantedBy=multi-user.target
---
sudo systemctl daemon-reload
sudo systemctl enable spc.service
sudo systemctl start spc.service
sudo systemctl status spc.service

http://publicip:8080 # check at this node





























https://referenceapplicationskhaja.s3.us-west-2.amazonaws.com/spring-petclinic-2.4.2.jar


https://gist.github.com/shaikkhajaibrahim/c1b11f62dc7a69bce47104161d6139c1

17th i will practise


