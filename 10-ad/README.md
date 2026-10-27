# 域渗透（`10-ad`）

_Kerberos、ACL 滥用、NTLM 中继_

## active-directory-kerberos-attacks  `P1`

Active Directory Kerberos 攻击。当需要通过 AS-REP roasting、Kerberoasting、黄金/白银/钻石票据、委派滥用或 pass-the-ticket 攻击 AD 认证时使用。

## active-directory-acl-abuse  `P1`

Active Directory ACL 滥用。当利用配置错误的 AD 权限时使用——含 GenericAll、WriteDACL、DCSync 权限、shadow credentials、LAPS 读取、GPO 滥用与 BloodHound 引导的攻击路径。

## ntlm-relay-coercion  `P1`

NTLM 中继与认证强制。当需要捕获并中继 NTLM 认证，经 SMB、LDAP、HTTP 或 MSSQL 中继目标提权，配合 PetitPotam、PrinterBug 等强制方法时使用。
