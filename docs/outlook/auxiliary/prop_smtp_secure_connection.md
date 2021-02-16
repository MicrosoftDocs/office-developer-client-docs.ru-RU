---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Указывает тип зашифрованного подключения для учетной записи SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421286"
---
# <a name="prop_smtp_secure_connection"></a>PROP_SMTP_SECURE_CONNECTION

Указывает тип зашифрованного подключения для учетной записи SMTP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x020A  <br/> |
|Тип свойства:  <br/> |PT_DWORD  <br/> |
|Тег свойства:  <br/> |0x020A0003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Значение может быть одной из следующих констант. Их значения см. в записях [Constants (API](constants-account-management-api.md) управления учетной записью). 
  
|**Константы**|**Описание**|
|:-----|:-----|
|**ENCRYPT_CONN_NO_SECURITY** <br/> |Не используйте шифрование.  <br/> |
|**ENCRYPT_CONN_SSL** <br/> |Используйте шифрование SSL.  <br/> |
|**ENCRYPT_CONN_TLS** <br/> |Используйте протокол шифрования и проверки подлинности TLS.  <br/> |
|**ENCRYPT_CONN_AUTO** <br/> |Автоматически обнаруживать и использовать метод шифрования, поддерживаемый почтовым сервером.  <br/> |
   
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constants (Account management API)](constants-account-management-api.md)

