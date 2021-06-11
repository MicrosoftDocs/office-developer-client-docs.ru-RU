---
title: Создание профиля Outlook с помощью MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI предоставляет доступ к хранилищам MAPI для облегчения расследования Exchange и Outlook и предоставления разработчикам поддержки для разработки MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345992"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Создание профиля Outlook с помощью MFCMAPI

MFCMAPI предоставляет доступ к хранилищам MAPI для облегчения расследования Exchange и Outlook и предоставления разработчикам поддержки для разработки MAPI.

**Относится к**: Office 365 | Outlook | Outlook 2016 
  
Для не разработчиков рекомендуется использовать пользовательский интерфейс Outlook для создания профилей для Exchange 2013 г.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Настройка профиля Outlook с помощью MFCMAPI

1. Откройте [MFCMAPI](https://mfcmapi.codeplex.com/)и в меню **Profile** щелкните **Показать профили.** 
    
2. В меню **Действия** нажмите кнопку **Создать профиль**. 
    
3. Создайте новое имя для профиля, а затем нажмите **кнопку ОК**. 
    
4. Щелкните правой кнопкой мыши новый профиль, а затем в меню **Services** нажмите **кнопку Добавить службу**. 
    
5. Отойдите от окна пользовательского интерфейса службы отображения и нажмите **кнопку ОК**. 
    
6. Дважды щелкните вновь созданный профиль, а затем щелкните **службу MSEMS.** 
    
7. Найдите раздел Exchange профилей.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Это значение потребуется в шаге 9.
    
8. Дважды щелкните **службу MSEMS.** 
    
9. Найдите **раздел Exchange** профилей с помощью UID из шага 7, а затем одним щелчком мыши выберите строку. 
    
10. В меню Свойства нажмите **кнопку Дополнительные свойства**. 
    
11. Нажмите **кнопку Добавить,** а затем добавить следующие свойства: 
    
    **Для Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` и`PR_DISPLAY_NAME_W`
    
    **Для Outlook для Office 365**: `PR_PROFILE_UNRESOLVED_NAME` , `PR_PROFILE_UNRESOLVED_SERVER` , , , `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` , `PR_PROFILE_AUTH_PACKAGE` и`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Для Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME` , , , , и `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` . 
    
12. Нажмите **кнопку ОК,** а затем настройте каждое свойство в соответствии с приведенной ниже таблицей в зависимости от версии, к которая подключается. 
    
13. В меню **Сеанс** щелкните **Logon и Display Store,** а затем выберите профиль (если он еще не выбран). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**Описание** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP Адрес пользователя  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Имя отображения пользователя  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Настройка значения этого свойства, расположенного в разделе **EMSMDB,** и обновление соответствующего UID для соответствующего свойства  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook для Office 365
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним целевого почтового ящика; например, Администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |персонализированный серверный id  <br/> |Значение, извлеченные из **автонаруже.** в <guid> формате @tenant.onmicrosoft.com; например, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автооткрытия:*  Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Узел автооткрытия:*  Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Содержит параметры в профиле, используемом Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедуры (RPC) над протоколом передачи Hypertext (HTTP). *Узел автооткрытия:*  Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Представляет протокол проверки подлинности, используемый для этого узла автонаружения *профиля:*  Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Описывает схему проверки подлинности, используемую для узла автонаружения *RPC:*  Response/Account/Protocol/AuthPackage (EXCH) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Элемент CertPrincipalName  <br/> |Используется для поддержки взаимной проверки подлинности; например, узел автооткрытия  msstd:outlook.com: Response/Account/Protocol/CertPrincipalName (EXPR) ) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним целевого почтового ящика; например, Администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |персонализированный серверный id  <br/> |Значение, извлеченные из **автонаруже.** в <guid> формате @tenant.onmicrosoft.com; например, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автооткрытия:*  Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | доменное имя сервера клиентского доступа  <br/> | Полное доменное имя (FQDN); например, узел  *e2013cas.contoso.com:*  Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Содержит параметры в профиле, используемом Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедуры (RPC)  над автооткрытым узлом Hypertext Transfer Protocol (HTTP) : Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Представляет протокол проверки подлинности, используемый для этого узла автонаружения *профиля:*  Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Описывает схему проверки подлинности, используемую для автонаружения узла *RPC:*  Response/Account/Protocol/AuthPackage (EXCH) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Все указанные выше значения свойств могут отличаться для конкретной организации. 
> - <sup>1</sup> Необходимо использовать версию Unicode, а не версию ANSI. 
> - Необходимо использовать автооткрытие на основе обычного старого XML (POX). Это единственный поддерживаемый автооткрывок для настройки Outlook/Exchange профилей.
> - Вы можете использовать Outlook, чтобы сделать запрос автообнаружения от вашего имени, щелкнув правой кнопкой мыши значок Outlook в подносе **системы,** удерживая CTRL и щелкнув тест автоконфигурации электронной почты **.** 
> - Для PR_ROH_FLAGS среды может потребоваться, чтобы флаг ROHFLAGS_SSL_ONLY (0x2) для того, чтобы сообщить MAPI использовать только SSL. Если для среды требуется взаимная проверка подлинности, необходимо также установить этот флаг [ROHFLAGS_MUTUAL_AUTH (0x4)]. Для ROHFLAGS_MUTUAL_AUTH (0x4) необходимо также установить PR_ROH_PROXY_PRINCIPAL_NAME. Это должно быть главным именем сервера.
> - <sup>2</sup> Для Outlook 2010 года необходимо использовать протокол EXPR. Outlook 2013 г. используется протокол EXHTTP. 
> - <sup>3</sup> Это значение не может быть в ответе автооткрытия. Если не указано, клиент должен использовать Kerberos или NTLM. 
    
Советы по устранению неполадок см. в Outlook профиля с помощью [MFCMAPI Exchange 2013 г.](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)
  
## <a name="see-also"></a>См. также

- [Справочник по MAPI для Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Программным образом создайте профиль в Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

