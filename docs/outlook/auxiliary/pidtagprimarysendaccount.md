---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Указывает основную учетную запись для сообщения.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327708"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Указывает основную учетную запись "отправить" для сообщения.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Идентификатор:  <br/> |0x0E28  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Счет  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство применяется к объекту сообщения MAPI. В полученном сообщении в основной учетной записи указывается, с какой учетной записью следует отправить сообщение или ответ. Для исходяния сообщения оно определяет, с какой учетной записью отправлять сообщение. Его значением является [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) из интерфейса [IOlkAccount](iolkaccount.md) учетной записи, с которой отправляется сообщение. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)
- [Свойства MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Каноническое свойство PidTagPrimarySendAccount](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

