---
title: Создание профиля Outlook с помощью MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI предоставляет доступ к хранилищам MAPI для упрощения исследования проблем Exchange и Outlook, а также для предоставления разработчикам поддержки разработки MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345992"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Создание профиля Outlook с помощью MFCMAPI

MFCMAPI предоставляет доступ к хранилищам MAPI для упрощения исследования проблем Exchange и Outlook, а также для предоставления разработчикам поддержки разработки MAPI.

**Относится к**: Office 365 | Outlook | Outlook 2016 
  
Для пользователей, не являющихся разработчиками, рекомендуется использовать пользовательский интерфейс Outlook для создания профилей для Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Настройка профиля Outlook с помощью MFCMAPI

1. Откройте [MFCMAPI](https://mfcmapi.codeplex.com/)и в меню **профиль** выберите пункт **Показать профили**. 
    
2. В меню **действия** выберите команду **создать профиль**. 
    
3. Создайте новое имя для профиля и нажмите кнопку **ОК**. 
    
4. Щелкните правой кнопкой мыши новый профиль, а затем в меню **службы** выберите команду **Добавить службу**. 
    
5. Снимите флажок "Пользовательский интерфейс службы отображения" и нажмите кнопку **ОК**. 
    
6. Дважды щелкните только что созданный профиль и выберите службу **мсемс** . 
    
7. Откройте раздел Профиль Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Это значение потребуется на шаге 9.
    
8. Дважды щелкните службу **мсемс** . 
    
9. Найдите раздел профиль **Exchange** с помощью идентификатора UID из шага 7, а затем щелкните один раз, чтобы выбрать строку. 
    
10. В меню Свойство выберите пункт **Дополнительные свойства**. 
    
11. Нажмите кнопку **Добавить**, а затем добавьте следующие свойства: 
    
    **Для Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` и`PR_DISPLAY_NAME_W`
    
    **Для Outlook для Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME`,, `PR_PROFILE_AUTH_PACKAGE`, и`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Для Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER`,, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`и `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Нажмите кнопку **ОК**, а затем настройте каждое свойство в соответствии с приведенной ниже таблицей в зависимости от версии, к которой выполняется подключение. 
    
13. В меню **сеанс** выберите пункт **Вход и отображение хранилища**, а затем выберите профиль (если он еще не выбран). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Tag** <br/> |**Описание** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-адрес пользователя  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Отображаемое имя пользователя  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Настройка значения этого свойства, расположенного в разделе **емсмдб** , и обновление соответствующего идентификатора для соответствующего свойства  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook для Office 365
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним целевого почтового ящика; Например, администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |персонализированный идентификатор сервера  <br/> |Значение, полученное из **автообнаружения**. в формате <guid>@tenant. onmicrosoft.com; Например, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автообнаружения* : Response/Account/Protocol/Server (курс)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Узел автообнаружения* : Response/Account/Protocol/Server (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Содержит параметры в профиле, используемом Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедур (RPC) по протоколу HTTP. *Узел автообнаружения* : Response/Account/Protocol/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Представляет протокол проверки подлинности, который будет использоваться для этого *узла автообнаружения* профиля: Response/Account/Protocol/АУСПАККАЖЕ (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Описание схемы проверки подлинности, которая будет использоваться для *узла АВТООБНАРУЖЕНИЯ* RPC: Response/Account/Protocol/АУСПАККАЖЕ (курс) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Элемент ЦертпринЦипалнаме  <br/> |Используется для поддержки взаимной проверки подлинности; Например, мсстд:Аутлук. com *node автообнаружения* : Response/Account/Protocol/ЦЕРТПРИНЦИПАЛНАМЕ (expr)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним целевого почтового ящика; Например, администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |персонализированный идентификатор сервера  <br/> |Значение, полученное из **автообнаружения**. в формате <guid>@tenant. onmicrosoft.com; Например, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автообнаружения* : Response/Account/Protocol/Server (курс)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | доменное имя сервера клиентского доступа  <br/> | Полное доменное имя (FQDN); Например, *узел автообнаружения* E2013cas.contoso.com: Response/Account/Protocol/Server (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Содержит параметры в профиле, используемом Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедур (RPC) по *узлу АВТООБНАРУЖЕНИЯ* http: Response/Account/Protocol/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Представляет протокол проверки подлинности, который будет использоваться для этого *узла автообнаружения* профиля: Response/Account/Protocol/АУСПАККАЖЕ (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Описание схемы проверки подлинности, используемой для *узла АВТООБНАРУЖЕНИЯ* RPC: Response/Account/Protocol/АУСПАККАЖЕ (курс) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Все значения свойств, упомянутые выше, могут различаться в зависимости от конкретной организации. 
> - <sup>1</sup> необходимо использовать версию Юникод, а не версию ANSI. 
> - Необходимо использовать автообнаружение на основе простого старого XML (POX). Это единственный поддерживаемый автообнаружение для настройки профилей Outlook/Exchange.
> - Чтобы сделать запрос автообнаружения от вашего имени, можно использовать Outlook, щелкнув правой кнопкой мыши значок Outlook в **панели задач**, удерживая клавишу CTRL и выбрав пункт **Проверка автонастройки электронной почты**. 
> - Для PR_ROH_FLAGS в вашей среде может потребоваться флаг ROHFLAGS_SSL_ONLY (0x2), указывающий MAPI на использование только протокола SSL. Если для вашей среды требуется взаимная проверка подлинности, необходимо также установить этот флаг (а также этот флаг [ROHFLAGS_MUTUAL_AUTH (0x4)]. Для параметра ROHFLAGS_MUTUAL_AUTH (0x4) потребуется также задать PR_ROH_PROXY_PRINCIPAL_NAME свойства. Это значение должно быть основным именем сервера.
> - <sup>2</sup> для Outlook 2010, необходимо использовать протокол expr. Outlook 2013 использует протокол ЕКСХТТП. 
> - <sup>3</sup> это значение может отсутствовать в отклике автообнаружения. Если этот параметр не указан, клиент должен использовать Kerberos или NTLM. 
    
Советы по поиску и устранению неисправностей приведены [в статье Настройка профиля Outlook с помощью MFCMAPI для Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>См. также

- [Справочник по MAPI для Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Программное создание профиля в Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

