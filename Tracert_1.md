The FIR151B A2、FIR302E A2、FIR300B A2 and so on routers has remote command execution

1.Login feixun FIR151B A2 router by default password admin /admin

2.Find the system tool → system diagnosis → Tracert → IP address / domain name. There is remote command execution at Tracert
![image](https://user-images.githubusercontent.com/96364879/182758133-03dbe705-4bb9-4bea-898b-13bf2e3cc557.png)

3.Enter the website IP at the IP address / domain name, for example: 8.8.8.8

4.Click Start diagnosis
 
5.Use burpsuite intercept and change pingAddr argument to 8.8.8.8|ls, forward this request
![image](https://user-images.githubusercontent.com/96364879/182757974-54817a9c-a3e5-41cf-9e87-44ae60882932.png)

6.Look at the diagnostic results. The command has been executed successfully
![image](https://user-images.githubusercontent.com/96364879/182756632-c4f380cb-ceb0-4611-9642-5a9eb0861c55.png)
