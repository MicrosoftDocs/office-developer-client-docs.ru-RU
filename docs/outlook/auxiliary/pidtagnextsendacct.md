---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: Указывает дополнительный accountsendstamp для сообщения.
ms.openlocfilehash: 3aa88a1fd5a73cc4ae2e990e6dad0697083bb694
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396479"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

Указывает дополнительный учетной записи «отправить» метка для сообщения.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Идентификатор:  <br/> |0x0E29  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Приложения Outlook  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство применяется к объекту сообщение MAPI. Для полученного сообщения отметку «отправить» дополнительного учетной записи указывает учетную запись вперед или ответ направляются в организации, если прямого или ответ, не удается отправить с основная учетная запись. Для исходящих сообщений дополнительного учетная запись «отправить» метка определяет учетную запись для отправки сообщения, если не удается отправить сообщение с учетной записью основной. Значением является значение [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) в интерфейсе [IOlkAccount](iolkaccount.md) учетной записи, с которого отправляются сообщения. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)
- [Свойства MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [Каноническое свойство PidTagNextSendAcct](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

