# PREABLE
* AWS ACCOUNT
* GIT HUB ACCOUNT
* VSCODE ACCOUNT
* IAM USER CREDENTIALS
### Instance was lauched by group leader and an IAM user account was opened for all the group members.


# AWS CLI CONFIGURATION
* Run *** aws configure*** with IAM user credentials received from the group capt
* details of the keys on the IAM user created are 
* Secret key: xxxxxx
* Key: xxxxxxx
with the region and name settings

# CREATING KEY PAIR
* aws ec2 create-key-pair --key-name sly --query 'KeyMaterial' --output text > sly.pem
* "my key pair" that was used spoecifically for my instance is 
![Alt text](<PICTURES/3. IAM ACCESS KEY AND KEY PAIRS.png>)
# CREATING SECURITY GROUP
* aws ec2 create-security-group --group-name MySecurityGroup --description "My security Group" with GroupId": "sg-0a830d8cb6e87cbef"
"my New Security Group" is the uniquegroup name ..
![Alt text](<PICTURES/4. MY SECURITY GROUP CLI.png>)

# ESTABLISH LINK WITH SECURITY GROUP
* aws ec2 authorize-security-group-ingress --group-name MysecurityGroup --protocol tcp -- port 22 --cidr 0.0.0.0/0
![Alt text](<PICTURES/5. security protocol.png>)
![Alt text](<PICTURES/6. SECURITY GROUP INGRESS.png>)
# LAUNCHING MY INSTANCE
* aws ec2 run-instances --image-id ami-03a6eaae9938c858c --count 1 --instance-type t2.
micro --key-name sly --security-groups MySecurityGroup..
![Alt text](<PICTURES/7. CLI instances begin.png>)
![Alt text](<PICTURES/8. CLI DISP OF INSTANCE.png>)
![Alt text](<PICTURES/9. CLI DISPLAY OF INSTANCE.png>)
![Alt text](<PICTURES/10. CLI DISPLAY OF INSTANCE (2).png>)
![Alt text](<PICTURES/11. PIC OF INSTANCE ALREADY RUNNING.png>)
![Alt text](<PICTURES/12. PIC instances disp 2.png>)
![Alt text](<PICTURES/13. INSTANCE TERMINATED.png>)