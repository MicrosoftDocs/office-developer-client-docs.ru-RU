---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Указывает метод проверки подлинности для учетной записи SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434643"
---
# <a name="prop_smtp_auth_method"></a>PROP_SMTP_AUTH_METHOD

Указывает метод проверки подлинности для учетной записи SMTP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0208  <br/> |
|Тип свойства:  <br/> |PT_DWORD  <br/> |
|Тег свойства:  <br/> |0x02080003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Значением является битоваяmass следующих констант. Их значения см. в записях [Constants (API](constants-account-management-api.md) управления учетной записью). 
  
- **SMTP_AUTH_SAME_AS_POP** означает использование тех же учетных данных, что и [](prop_inet_user.md) для почтового сервера входящих сообщений, PROP_INET_USER и [PROP_INET_PASSWORD.](prop_inet_password.md)
    
- **SMTP_AUTH_USER_PASS** означает использование учетных данных, предоставленных PROP_SMTP_USER [и](prop_smtp_user.md) [PROP_SMTP_PASSWORD.](prop_smtp_password.md)
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** означает запрос пользователя на вход на почтовый сервер входов перед отправкой почты. 
    
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constants (Account management API)](constants-account-management-api.md)

