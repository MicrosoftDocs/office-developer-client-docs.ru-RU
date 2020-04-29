---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Указывает вторичный аккаунтсендстамп для сообщения.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327715"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Указывает отметку "Отправить" для сообщения с дополнительной учетной записью.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Идентификатор:  <br/> |0x0E29  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Приложение Outlook  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство применяется к объекту сообщения MAPI. Для полученного сообщения штамп "Отправить" дополнительной учетной записи указывает, с какой учетной записью следует отправлять пересылку или отвечать, если пересылка или ответ не может быть отправлена с основной учетной записью. Для исходящих сообщений метка "Отправить" для дополнительной учетной записи определяет, с какой учетной записью отправляется сообщение, если сообщение не может быть отправлено с основной учетной записью. Его значение — это [PROP_ACCT_SEND_STAMPое](prop_acct_send_stamp.md) значение из интерфейса [иолкаккаунт](iolkaccount.md) учетной записи, с которой отправляется сообщение. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)
- [Свойства MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Каноническое свойство PidTagNextSendAcct](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

