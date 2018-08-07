---
title: Создание профиля Outlook с помощью MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: Mfcmapi (en) предоставляет доступ к хранилищу MAPI для облегчения изучения проблем Exchange и Outlook и предоставляет разработчикам с поддержкой для разработки MAPI.
ms.openlocfilehash: 8df9a4c2783829b7f3540046daecb12ce0b6b86a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808602"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Создание профиля Outlook с помощью MFCMAPI

Mfcmapi (en) предоставляет доступ к хранилищу MAPI для облегчения изучения проблем Exchange и Outlook и предоставляет разработчикам с поддержкой для разработки MAPI.

**Относится к**: Office 365 | Outlook | Outlook 2016 
  
Не только для разработчиков рекомендуется использовать пользовательский интерфейс Outlook для создания профилей для Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Настройка профиля Outlook с помощью mfcmapi (en)

1. Откройте [mfcmapi (en)](https://mfcmapi.codeplex.com/)и в меню **профиля** нажмите кнопку **Показать**. 
    
2. В меню **действия** выберите **Создать профиль**. 
    
3. Создайте новое имя профиля и нажмите кнопку **ОК**. 
    
4. Щелкните правой кнопкой мыши новый профиль и нажмите кнопку **Добавить службу**в меню **служб** . 
    
5. Снимите флажок «Пользовательского интерфейса службы отображения» и нажмите кнопку **ОК**. 
    
6. Дважды щелкните только что созданный профиль и нажмите кнопку **MSEMS** службы. 
    
7. Найдите раздел профиля Exchange.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Требуется это значение в шаге 9.
    
8. Дважды щелкните служба **MSEMS** . 
    
9. Найдите раздел профиля **Exchange** с помощью ИД пользователя в шаге 7 и затем одним щелчком мыши для выбора строки. 
    
10. В меню Свойства выберите команду **Дополнительные свойства**. 
    
11. Нажмите кнопку **Добавить**, а затем добавьте следующие свойства: 
    
    **Для Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` и`PR_DISPLAY_NAME_W`
    
    **Для Outlook для Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`, и`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Для Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, и `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Нажмите **кнопку ОК**, а затем настройте каждого свойства определяется в таблице ниже, в зависимости от версии, в которой вы подключаетесь. 
    
13. В меню **сеанса** нажмите кнопку **Вход в систему и отображения хранилища**и выберите профиль (если он не установлен). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Тег** <br/> |**Описание** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-адрес пользователя  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Отображаемое имя пользователя  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Значение этого свойства, в разделе **EMSMDB** и обновления соответствующих UID для соответствующего свойства  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook для Office 365
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним для целевого почтового ящика; Например администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |код настраиваемого сервера  <br/> |Значение, полученное из **службы автообнаружения**. в формате <guid>@tenant.onmicrosoft.com; Например F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автообнаружения* : ответа и учетная запись/протокол/сервера (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.Office365.com  <br/> | *Узел автообнаружения* : ответа и учетная запись/протокол/сервера (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/> ROH_FLAGS_USE_SSL (0X2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0X4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20)  <br/> |Содержит параметры профиля, используемые Outlook для подключения к Microsoft Exchange Server с помощью удаленный вызов процедур (RPC) по протоколу (HTTP). *Узел автообнаружения* : ответа/учетная запись/протокол/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0X1)  <br/> |Представляет протокол проверки подлинности, которое будет использоваться для этого профиля *Узла автообнаружения* : ответа/учетная запись/протокол/AuthPackage (Выражение) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0X0)  <br/> |Описание схемы проверки подлинности для RPC *Узла автообнаружения* : ответа/учетная запись/протокол/AuthPackage (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |Элемент CertPrincipalName  <br/> |Для поддержки взаимная проверка подлинности; к примеру, msstd:outlook.com *Узел автообнаружения* : ответа/учетная запись/протокол/CertPrincipalName (EXPR)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Свойство** <br/> |**Значение** <br/> |**Описание** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |псевдоним почтового ящика  <br/> |Псевдоним для целевого почтового ящика; Например администратор  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |код настраиваемого сервера  <br/> |Значение, полученное из **службы автообнаружения**. в формате <guid>@tenant.onmicrosoft.com; Например F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Узел автообнаружения* : ответа и учетная запись/протокол/сервера (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | имя домена сервера клиентского доступа  <br/> | Полное доменное имя (FQDN); к примеру, e2013cas.contoso.com *Узел автообнаружения* : ответа и учетная запись/протокол/сервера (Выражение) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0X1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0X8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0X20))  <br/> |Содержит параметры профиля, используемые Outlook для подключения к Microsoft Exchange Server с помощью удаленный вызов процедур (RPC) через протокол HTTP (Hypertext Transfer) *Узла автообнаружения* : ответа/учетная запись/протокол/SSL (Выражение) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0X2)  <br/> |Представляет протокол проверки подлинности, которое будет использоваться для этого профиля *Узла автообнаружения* : ответа/учетная запись/протокол/AuthPackage (Выражение) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0XA)  <br/> |Описание схемы проверки подлинности для RPC *Узла автообнаружения* : ответа/учетная запись/протокол/AuthPackage (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Все значения свойств, перечисленных выше могут отличаться от указанных для конкретной организации. 
> - <sup>1</sup> необходимо использовать версию Юникод, а не в формате ANSI. 
> - Необходимо использовать обычные старые XML (POX) на основе службы автообнаружения. Это единственный поддерживаемый автообнаружения при настройке профилей Outlook и Exchange.
> - Outlook можно использовать для выполнения запроса автообнаружения от вашего имени щелкнуть правой кнопкой мыши значок Outlook на **Панели задач**, во время и **Тестирования автоматической настройки электронной почты**, удерживая нажатой клавишу CTRL. 
> - Для PR_ROH_FLAGS среды может потребоваться флаг ROHFLAGS_SSL_ONLY (0x2), чтобы сообщить MAPI для использования только протокола SSL. Если в среде необходимо взаимная проверка подлинности, необходимо установить этот флаг также [ROHFLAGS_MUTUAL_AUTH (0x4)]. Параметр ROHFLAGS_MUTUAL_AUTH (0x4) необходимо также установить свойство PR_ROH_PROXY_PRINCIPAL_NAME. Следует устанавливать это будет имя участника сервера.
> - <sup>2</sup> для Outlook 2010, необходимо использовать протокол EXPR. Outlook 2013 с помощью протокола EXHTTP. 
> - <sup>3</sup> это значение не может быть в ответ службы автообнаружения. Если не указан, клиент должен использовать протокол Kerberos или NTLM. 
    
Советы по устранению неполадок, [как настроить профиль Outlook с помощью mfcmapi (en) для Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)см.
  
## <a name="see-also"></a>См. также

- [Справочник по MAPI для Outlook](https://msdn.microsoft.com/en-us/library/office/cc765775.aspx)  
- [Программное создание профиля в Outlook](https://msdn.microsoft.com/en-us/library/office/mt707568.aspx)
    

