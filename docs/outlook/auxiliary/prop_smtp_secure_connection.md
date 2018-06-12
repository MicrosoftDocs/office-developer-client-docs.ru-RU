---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Указывает тип шифрованного подключения для учетной записи SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807956"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Указывает тип шифрованного подключения для учетной записи SMTP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x020A  <br/> |
|Тип свойства:  <br/> |PT_DWORD  <br/> |
|Свойство tag:  <br/> |0x020A0003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Значение может быть одна из следующих констант. В разделе [константы (Управление учетными записями API)](constants-account-management-api.md) их значения. 
  
|**Константы**|**Описание**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Не используйте любой шифрования.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Используйте шифрование Secure сокетов (SSL).  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Используйте протокол проверки подлинности и шифрования безопасности TLS (Transport Layer).  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Автоматическое определение и использование метода шифрования, поддерживаемые почтовым сервером.  <br/> |
   
## <a name="see-also"></a>См. также

- [Загружаемые файлы для управления сообщения для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constants (Account management API)](constants-account-management-api.md)

