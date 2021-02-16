---
title: Создание профиля Outlook с помощью MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI предоставляет доступ к хранилищам MAPI, чтобы упростить исследование проблем Exchange и Outlook, а также предоставить разработчикам поддержку разработки MAPI.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345992"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Создание профиля Outlook с помощью MFCMAPI

MFCMAPI предоставляет доступ к хранилищам MAPI, чтобы упростить исследование проблем Exchange и Outlook, а также предоставить разработчикам поддержку разработки MAPI.

**Относится к**: Office 365 | Outlook | Outlook 2016 
  
Пользователям, не относянымся к разработчикам, рекомендуется использовать пользовательский интерфейс Outlook для создания профилей для Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Настройка профиля Outlook с помощью MFCMAPI

1. Откройте [MFCMAPI](https://mfcmapi.codeplex.com/)и в **меню** "Профиль" выберите пункт **"Показать профили".** 
    
2. В меню **"Действия"** щелкните **"Создать профиль".** 
    
3. Создайте новое имя профиля и нажмите кнопку **"ОК".** 
    
4. Щелкните правой кнопкой мыши новый профиль, а затем в меню **"Службы"** выберите пункт **"Добавить службу".** 
    
5. Отойдите в поле "Пользовательский интерфейс службы отображения" и нажмите кнопку **"ОК".** 
    
6. Дважды щелкните созданный профиль и выберите службу **MSEMS.** 
    
7. Найдите раздел "Профиль Exchange".
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Это значение потребуется на шаге 9.
    
8. Дважды щелкните **службу MSEMS.** 
    
9. Найдите **раздел профиля Exchange** с помощью UID из шага 7 и щелкните строку одним щелчком. 
    
10. В меню "Свойство" выберите **"Дополнительные свойства".** 
    
11. Нажмите **кнопку "Добавить"** и добавьте следующие свойства: 
    
    **Для Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` и `PR_DISPLAY_NAME_W`
    
    **Для Outlook для Office 365:** `PR_PROFILE_UNRESOLVED_NAME` , , , , `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` и `PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Для Exchange 2013:** `PR_PROFILE_UNRESOLVED_NAME` , , , , и `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` . 
    
12. Нажмите **кнопку**"ОК", а затем настройте каждое свойство в соответствии с приведенной ниже таблицей в зависимости от версии подключения. 
    
13. В меню **"Сеанс"** щелкните "Ложок" и "Хранилище отображения", а затем выберите профиль (если он еще не выбран).  
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Property** <br/> |**Tag** <br/> |**Описание** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-адрес пользователя  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Отображаемого имени пользователя  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Настройка значения этого свойства, расположенного в разделе **EMSMDB,** и обновление соответствующего UID для соответствующего свойства  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook для Office 365
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним целевого почтового ящика; например, администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |персонализированный ид сервера  <br/> |Значение, извлекаемого из **автооружия.** в <guid> формате @tenant.onmicrosoft.com; например, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автооружия:*  ответ/учетная запись/протокол/сервер (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *Узел автооружия:*  ответ/учетная запись/протокол/сервер (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Содержит параметры в профиле, используемом Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедуры (RPC) по протоколу HTTP. *Узел автооружия:*  ответ/учетная запись/протокол/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Представляет протокол проверки подлинности, используемый для узла автооружения этого профиля: ответ/учетная запись/протокол/AuthPackage (EXPR) <sup>2</sup>  <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Описывает схему проверки подлинности, используемую для узла автонаружения *RPC:*  ответ/учетная запись/протокол/AuthPackage (EXCH) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Элемент CertPrincipalName  <br/> |Используется для поддержки взаимной проверки подлинности; например, msstd:outlook.com *Autodiscover Node*  : Response/Account/Protocol/CertPrincipalName (EXPR) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним целевого почтового ящика; например, администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |персонализированный ид сервера  <br/> |Значение, извлекаемого из **автооружия.** в <guid> формате @tenant.onmicrosoft.com; например, F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автооружия:*  ответ/учетная запись/протокол/сервер (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | доменное имя сервера клиентского доступа  <br/> | Полное доменное имя (FQDN); например, узел e2013cas.contoso.com  *автооружия:*  ответ/учетная запись/протокол/сервер (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Содержит параметры профиля, используемого Outlook для подключения к Microsoft Exchange Server с помощью удаленного вызова процедуры (RPC) через узел автоотнаружения *http:*  response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Представляет протокол проверки подлинности, используемый для узла автооружения этого профиля: ответ/учетная запись/протокол/AuthPackage (EXPR) <sup>2</sup>  <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Описывает схему проверки подлинности, используемую для узла автонаружения *RPC:*  ответ/учетная запись/протокол/AuthPackage (EXCH) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Все значения свойств, упомянутые выше, могут отличаться для конкретной организации. 
> - <sup>1</sup> Необходимо использовать версию Юникод, а не версию ANSI. 
> - Необходимо использовать автооружие на основе обычного старого XML(POX). Это единственный поддерживаемый автообнаружение для настройки профилей Outlook и Exchange.
> - Outlook можно использовать для запроса автообнаружения от вашего имени, щелкнув правой кнопкой мыши значок Outlook в области **задач,** удерживая CTRL и нажимая кнопку "Проверить автонастройку электронной почты".  
> - Для PR_ROH_FLAGS среде может потребоваться флаг ROHFLAGS_SSL_ONLY (0x2), чтобы MAPI мог использовать только SSL. Если в вашей среде требуется взаимная проверка подлинности, необходимо также установить этот флаг [ROHFLAGS_MUTUAL_AUTH (0x4)]. Настройка ROHFLAGS_MUTUAL_AUTH (0x4) требует, чтобы также было установлено PR_ROH_PROXY_PRINCIPAL_NAME. Это имя должно быть главным именем сервера.
> - <sup>2</sup> Для Outlook 2010 необходимо использовать протокол EXPR. Outlook 2013 использует протокол EXHTTP. 
> - <sup>3</sup> Это значение может не быть в ответе автооружия. Если он не указан, клиент должен использовать Kerberos или NTLM. 
    
Советы по устранению неполадок см. в подразделе "Настройка профиля Outlook с помощью [MFCMAPI для Exchange 2013".](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)
  
## <a name="see-also"></a>См. также

- [Справочник по MAPI для Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Создание профиля в Outlook программным путем](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

