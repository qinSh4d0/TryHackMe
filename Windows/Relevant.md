![image](https://github.com/user-attachments/assets/39fd5673-b13e-470b-94db-bde824699250)
![image](https://github.com/user-attachments/assets/0ace8236-308f-4923-accd-34ad4ba7b5b4)

nmap result re smb-security-mode indicates likely anonymous access to SMB is enabled

![image](https://github.com/user-attachments/assets/31f6f7e0-e3f2-43aa-a11c-81bcf2a5d55b)
![image](https://github.com/user-attachments/assets/908af3a3-fa66-4ba6-9838-912f344d7287)
![image](https://github.com/user-attachments/assets/067b3381-88ca-4e78-aaa0-2a50718313b1)
![image](https://github.com/user-attachments/assets/38b9775d-b896-452a-8acf-2e555f6c5f9a)
![image](https://github.com/user-attachments/assets/a912c59a-ae8f-4df1-94cd-ca84309010ee)

Not find entry point. Take a break.

Continue.  Restart machine.   New IP.

![image](https://github.com/user-attachments/assets/dfebaff6-01a7-442a-b276-b8f7186241f5)
![image](https://github.com/user-attachments/assets/decde10f-95e4-4db9-b172-ed1cbe4e4066)
![image](https://github.com/user-attachments/assets/19b15e16-28b3-47b1-8d07-6c1696c38b03)
![image](https://github.com/user-attachments/assets/07f17f24-a54e-4542-9688-e276021068e9)
![image](https://github.com/user-attachments/assets/eecea065-94ba-4c8a-af0d-e687cffff523)
![image](https://github.com/user-attachments/assets/414660c6-d6e5-430c-aac7-7bf17aea0263)
![image](https://github.com/user-attachments/assets/6b6c101c-7e9b-4e79-82e2-c0388a627a29)
![image](https://github.com/user-attachments/assets/75b60a8e-39f2-4862-811d-1b65ce7921d1)
![image](https://github.com/user-attachments/assets/3bec0047-6ad5-413d-85dc-5f29a3e204f3)
![image](https://github.com/user-attachments/assets/bcf8c104-97b6-4480-bd3b-cde3ff231f0e)
![image](https://github.com/user-attachments/assets/49342140-1ec9-478e-83a6-3e59fa83a28e)
![image](https://github.com/user-attachments/assets/de5e847e-84fb-4091-b86c-40efd2b0fc75)
![image](https://github.com/user-attachments/assets/324d9347-7069-42d2-818d-66560f0cb329)
![image](https://github.com/user-attachments/assets/4d7f926e-5e2c-4776-a950-484a8b633840)

1. anonymous writing to share is allowed

2. directory brute-forcing show result .aspx

3. msfvenom generate .aspx payload and place in share

4. web browser visit payload to get reverse shell

5.  user iis apppool --> SeImpersonatePrivilege Enabled

6.  systeminfo --> x64-based PC

7.  upload PrintSpoofer64.exe to C:\inetpub\wwwroot\nt4wrksv  (share)

8.  PrintSpoofer.exe -i -c cmd --> PrivEsc to SYSTEM
