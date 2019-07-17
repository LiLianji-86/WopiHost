### ����
- ֧��`DOCX`�༭���Լ�`PPTX`��`XLSX`
- ֧��Эͬ������Word��Excel�� PowerPoint��
- ����΢���ṩ��ʾ�����Ե���
- <https://github.com/Microsoft/Office-Online-Test-Tools-and-Documentation>

### ����
- ��ȡ������`web.config`����������
- ֧��linux���𣬻���jexus
- ֧�����Ĳ���
- ��Ӵ�����־���

### ˵��
- ���Ĳ������ȱ����ٴ�������`WOPISrc`������������룬��`��������`
- �ĵ���Ŀ¼��Ҫ����`��дȨ��`
- ��������ʱ��Լ30������

### ����
- ����`access_token`Ϊ��Ȩ��֤�����Լ�ʵ�֣�Эͬ���ͬһtoken��Ӧ���ǣ�
- ����`UserId`Ϊ�˺�
- ����`UserName`Ϊ����
- ���������Ķ�����α���

----------

> ��װ�̳̣�https://docs.microsoft.com/zh-cn/officeonlineserver/deploy-office-online-server

> ��װ�����У���֤ **Windows Update** �������

> ͨ��Զ�̷��ʷ�������װʱ������ͨ����Դ������̵ķ�ʽֱ�����У�������ͨ�������̷��ķ�ʽ���У���`\\192.168.1.188\G$`

> Server2012 R2 ���ϣ�������Server2016Ϊ��

> ����`PowerShell`�������Ƿ�������Ĭ��Administrator�˺�Ϊ **����Ա** 

### ��һ������ɫ�ͷ���

Windows Server 2012 R2:
```
Add-WindowsFeature Web-Server,Web-Mgmt-Tools,Web-Mgmt-Console,Web-WebServer,Web-Common-Http,Web-Default-Doc,Web-Static-Content,Web-Performance,Web-Stat-Compression,Web-Dyn-Compression,Web-Security,Web-Filtering,Web-Windows-Auth,Web-App-Dev,Web-Net-Ext45,Web-Asp-Net45,Web-ISAPI-Ext,Web-ISAPI-Filter,Web-Includes,InkandHandwritingServices,NET-Framework-Features,NET-Framework-Core,NET-HTTP-Activation,NET-Non-HTTP-Activ,NET-WCF-HTTP-Activation45,Windows-Identity-Foundation,Server-Media-Foundation
```
Windows Server 2016��
```
Add-WindowsFeature Web-Server,Web-Mgmt-Tools,Web-Mgmt-Console,Web-WebServer,Web-Common-Http,Web-Default-Doc,Web-Static-Content,Web-Performance,Web-Stat-Compression,Web-Dyn-Compression,Web-Security,Web-Filtering,Web-Windows-Auth,Web-App-Dev,Web-Net-Ext45,Web-Asp-Net45,Web-ISAPI-Ext,Web-ISAPI-Filter,Web-Includes,NET-Framework-Features,NET-Framework-45-Features,NET-Framework-Core,NET-Framework-45-Core,NET-HTTP-Activation,NET-Non-HTTP-Activ,NET-WCF-HTTP-Activation45,Windows-Identity-Foundation,Server-Media-Foundation
```
### �ڶ�������������

 **.NET Framework 4.5.2** 

https://go.microsoft.com/fwlink/p/?LinkId=510096

 **Visual C++ Redistributable Packages for Visual Studio 2013** 

https://www.microsoft.com/download/details.aspx?id=40784

 **Visual C++ Redistributable for Visual Studio 2015** 

https://go.microsoft.com/fwlink/p/?LinkId=620071

 **Microsoft.IdentityModel.Extention.dll** 

https://go.microsoft.com/fwlink/p/?LinkId=620072

### ��������������
##### ��˵����
https://www.cnblogs.com/wanggege/p/4605678.html

��ӽ�ɫ�͹��ܣ�ѡ�� **Active Directory �����** ��װ���ȴ���ɣ���Ҫ�رգ�
��� **���˷���������Ϊ�������** ��ѡ�� **�������** ���������������  **`oos.com`**  ���Լ���㶨�壬�������룬��װ���Զ�����

### ���Ĳ�����װOffice Online Server
û�а������ڣ�MSDN�Ҹ����� ����
```
ed2k://|file|cn_office_online_server_last_updated_march_2017_x64_dvd_10245068.iso|730759168|DA70F58CB8FFAF37C02302F2501CE635|/
```

##### Office Online Serverע�����
https://docs.microsoft.com/zh-cn/officeonlineserver/plan-office-online-server

- ��Ҫ��װSQL Server�ȷ���������
- ��Ҫ�ڶ˿� 80��443 �� 809 �ϰ�װ���� Web ������ (IIS) ��ɫ���κη�����ɫ
- ��Ҫ��װ�κΰ汾�� Office
- ��Ҫ����������ϰ�װ Office Online Server
- �����֮��һ̨�ɾ��ķ�����

### ���岽����װ���԰�
http://go.microsoft.com/fwlink/p/?LinkId=798136

### ��������ټ���
<https://download.microsoft.com/download/6/B/D/6BD1D664-1212-4AB2-9BE8-447731F2CA0E/wacserver2016-kb4011025-fullfile-x64-glb.exe>

### ������������OfficeWebApps ģ��
```
Import-Module -Name OfficeWebApps
```

### ���߲�������Office Online Server��
```
New-OfficeWebAppsFarm -InternalURL "http://oos.com" -AllowHttp -EditingEnabled
```

### �ڰ˲�����֤Office Online Server��
http://oos.com/hosting/discovery	��ķ�ʽ���ʣ���Ҫ���ʵĿͻ��˼�����

http://localhost/hosting/discovery	���ط���

http://192.168.1.78/hosting/discovery	IP����	���������ܷ��ʣ�ȥ��IIS���Ѿ��Զ������վ��

### �ھŲ�������Wopi��Ŀ
https://github.com/netnr/WopiHost

https://gitee.com/netnr/WopiHost

�������񣬸�������

### ��ʮ����ʹ��
- [OfficeOnlineServerʹ���ĵ�](https://www.netnr.com/doc/code/4964095842855914510)
- WopiHost ��Ŀ `doc/OfficeOnlineServer.doc`

### ����
- `Get-OfficeWebAppsFarm` ���ص�ǰ������������ OfficeWebAppsFarm �������ϸ��Ϣ
- `New-OfficeWebAppsFarm` �ڱ��ؼ�����ϴ����� Office Online Server ��
- `Set-OfficeWebAppsFarm` �������� Office Online Server ��������
- `Remove-OfficeWebAppsMachine` �� Office Online Server ����ɾ�����з�������ɾ��Farm��
- �������<https://docs.microsoft.com/zh-cn/officeonlineserver/windows-powershell-for-office-online-server/windows-powershell-for-office-online-server>

### ��ͼ

Word��ͼ

![word](https://static.netnr.com/2018/11/13/593bab5043.png)

Excel��ͼ

![excel](https://static.netnr.com/2018/11/13/852ec9c947.png)