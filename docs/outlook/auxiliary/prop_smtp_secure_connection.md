---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Указывает тип зашифрованного подключения, используемого для учетной записи SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328331"
---
# <a name="propsmtpsecureconnection"></a>PROP_SMTP_SECURE_CONNECTION

Указывает тип зашифрованного подключения, используемого для учетной записи SMTP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x020A  <br/> |
|Тип свойства:  <br/> |ПТ_ДВОРД  <br/> |
|Тег свойства:  <br/> |0x020A0003  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Комментарии

Значение может быть одной из следующих констант. В этом разделе приведены [константы (API управления учетНыми записями)](constants-account-management-api.md) для их значений. 
  
|**Константы**|**Описание**|
|:-----|:-----|
|**ЕНКРИПТ_КОНН_НО_СЕКУРИТИ** <br/> |Не используйте шифрование.  <br/> |
|**ЕНКРИПТ_КОНН_ССЛ** <br/> |Используйте шифрование SSL.  <br/> |
|**ЕНКРИПТ_КОНН_ТЛС** <br/> |Используйте шифрование TLS и протокол проверки подлинности.  <br/> |
|**ЕНКРИПТ_КОНН_АУТО** <br/> |Автоматически определять и использовать метод шифрования, поддерживаемый почтовым сервером.  <br/> |
   
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constants (Account management API)](constants-account-management-api.md)

