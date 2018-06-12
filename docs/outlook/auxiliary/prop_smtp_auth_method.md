---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Указывает метод проверки подлинности для учетной записи SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807960"
---
# <a name="propsmtpauthmethod"></a>PROP_SMTP_AUTH_METHOD

Указывает метод проверки подлинности для учетной записи SMTP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0208  <br/> |
|Тип свойства:  <br/> |PT_DWORD  <br/> |
|Свойство tag:  <br/> |0x02080003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Значение является битовой маской из следующих констант. В разделе [константы (Управление учетными записями API)](constants-account-management-api.md) их значения. 
  
- **SMTP_AUTH_SAME_AS_POP** означает, что использование один набор учетных данных в качестве сервера входящих сообщений, предоставляемый [PROP_INET_USER](prop_inet_user.md) и [PROP_INET_PASSWORD](prop_inet_password.md).
    
- **SMTP_AUTH_USER_PASS** означает, что с помощью учетных данных, как автор [PROP_SMTP_USER](prop_smtp_user.md) и [PROP_SMTP_PASSWORD](prop_smtp_password.md).
    
- **SMTP_AUTH_RECEIVE_BEFORE_SEND** означает, что разрешения на запрос пользователя для входа на сервер входящей почты перед отправкой. 
    
## <a name="see-also"></a>См. также

- [Загружаемые файлы для управления сообщения для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md)  
- [Constants (Account management API)](constants-account-management-api.md)

