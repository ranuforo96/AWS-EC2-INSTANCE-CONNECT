# AWS-EC2-INSTANCE-CONNECT
Actions taken to utilize a browser-based alternative to traditional SSH access for connecting to Linux EC2 instances

To begin,  access your EC2 dashboard and select Instance in the left navigation pane

<img width="960" height="1080" alt="image" src="https://github.com/user-attachments/assets/8b66b63c-746d-4831-ace3-c9a4e4d498d7" />

To proceed, select the EC2 instance you want to connect to through the Linux command prompt and then click Connect 

<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/be649ea0-d6c8-42a0-ad0c-03c58cfc1b1e" />

For the "In web browser" tab it offers a few ways to connect; for this demonstration, I will be using EC2 Instance Connect. So I will leave the selection as is

<img width="1920" height="852" alt="image" src="https://github.com/user-attachments/assets/36f7772b-22bb-4487-abe0-98427d2e34e7" />

Next, you want to verify the Public IPv4 address and just below that will be your username which will be provided by default. Once these are both verified you can then proceed by right-clicking Connect at the bottom of the page

<img width="936" height="794" alt="image" src="https://github.com/user-attachments/assets/ad711e20-2555-414d-b0f1-57dde5011f7d" />

You should now have access to the Amazon Linux 2023 terminal

<img width="968" height="1080" alt="image" src="https://github.com/user-attachments/assets/521f48a8-aaea-4b84-9c19-e51247785f4d" />

To confirm it is functioning properly, you can run some basic commands such as "whoami" or "ping google.com"

<img width="965" height="1080" alt="image" src="https://github.com/user-attachments/assets/4dc102cc-83e2-4273-a928-e73a959fc320" />

<img width="961" height="1079" alt="image" src="https://github.com/user-attachments/assets/704657f5-2357-445d-998f-7068e9aafcbe" />

Although EC2 Instance Connect is browser-based, it still requires Port 22 (SSH) to be open in your instance's Security Group. Deleting or blocking Port 22 will cause connection timeouts because the underlying transport protocol is still SSH

For example, to inspect the initial security configuration, open your instance (My First EC2), select the Security tab, and click the attached security group (launch-wizard-1) to review its active rules

<img width="1024" height="576" alt="image" src="https://github.com/user-attachments/assets/f31ec44e-addf-4574-8656-e86f18e78f6d" />

<img width="1024" height="492" alt="image" src="https://github.com/user-attachments/assets/5f5c9681-9484-4884-91be-154ecfafe113" />

If I were to delete the SSH rule by editing the inbound rules, I would no longer have access to the Linux terminal

<img width="1024" height="494" alt="image" src="https://github.com/user-attachments/assets/199f2701-b860-4b4b-8c21-34fd7b4bf147" />

<img width="1024" height="496" alt="image" src="https://github.com/user-attachments/assets/7c5d04d3-0b10-4b2e-95d0-5338551c9d5e" />

<img width="1024" height="494" alt="image" src="https://github.com/user-attachments/assets/c14eb8b2-8ab3-4a38-bb1d-9253cdb9cdb2" />

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/85451af5-279d-4421-a94e-75b0a46fa4ca" />

