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
