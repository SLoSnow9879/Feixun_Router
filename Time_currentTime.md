The FIR151B A2、FIR302E A2、FIR303B A2 and so on routers has remote command execution

1. Login feixun FIR303B A2 router by default password admin /admin

2. Find the system tool → Time management → Current time. There is remote command execution at this argument.
![image](https://user-images.githubusercontent.com/96364879/182766028-521d06f0-76ea-46d9-99f8-b7ab674a8da5.png)

3. Click Save button.

4. Use burpsuite intercept and change current_time argument to \`ping -c 2 qwer.r4y19h.dnslog.cn\`, forward this request
![image](https://user-images.githubusercontent.com/96364879/182766190-27028ba1-1396-4e7e-8a9b-aae95af6d081.png)

5. See the dnslog results. The command has been executed successfully.
![image](https://user-images.githubusercontent.com/96364879/182766240-94fb60b4-bb2f-471e-a526-ead0d551d3ce.png)
