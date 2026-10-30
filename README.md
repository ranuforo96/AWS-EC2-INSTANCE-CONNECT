# AWS-EC2-INSTANCE-CONNECT
Actions taken to utilize a browser-based alternative to traditional SSH access for connecting to Linux EC2 instances

To begin,  access your EC2 dashboard and select Instance in the left navigation pane

<img width="960" height="1080" alt="image" src="https://github.com/user-attachments/assets/8b66b63c-746d-4831-ace3-c9a4e4d498d7" />

To proceed, select the EC2 instance you want to connect to the Linux command prompt and then click Connect 

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

<img width="1920" height="927" alt="image" src="https://github.com/user-attachments/assets/82cc560c-91f4-46c0-82ba-c017aef43d57" />

<img width="1920" height="923" alt="image" src="https://github.com/user-attachments/assets/85451af5-279d-4421-a94e-75b0a46fa4ca" />

Upon removing the port 80 rule, you will no longer be granted access to the Linux terminal

<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/9a741acb-f4e1-4ae1-9a36-10fab110944a" />

However, if we add it back, we will be able to continue using the Linux terminal

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/91dcc1c7-4733-474d-aadf-2ee742a021c8" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/867031b7-6226-468c-8aa4-c9344746ca8d" />

Here I..

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/49cf47e0-28cf-40d3-88ec-dd075a4a3bfc" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9b50193d-5979-4c77-937d-ca1be4b25933" />

Rules was saved successfully

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7175dc6b-b0fa-42ba-9e37-1153c2abebb7" />

Now, if I try accessing the Amazon Linux 2023 terminal, I should have no issues

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/578dcda9-7e1f-4f6e-a37f-cb4a84374032" />

Review the information once more and press Connect to access the terminal

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7e12aa83-3fdf-47a3-aa40-c6f0dfe4ba32" />

I have now regained access with no errors 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6adf0634-f7f8-4091-99a0-70694a6b8f5e" />

