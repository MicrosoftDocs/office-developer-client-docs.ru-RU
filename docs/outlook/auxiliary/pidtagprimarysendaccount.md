---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Указывает основной accountsendstamp для сообщения.
ms.openlocfilehash: f94ac104a77e8400909dc06db44ce8ca03e4653f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807931"
---
# <a name="pidtagprimarysendaccount"></a>PidTagPrimarySendAccount

Задает отметку «отправить» основная учетная запись для сообщения.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Идентификатор:  <br/> |0x0E28  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Учетная запись  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство применяется к объекту сообщение MAPI. Для полученного сообщения отметку «отправить» основная учетная запись указывает, какие прямого или ответ направляются с помощью учетной записи. Для исходящих сообщений он определяет, какая учетная запись для отправки сообщения с. Значением является значение [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) в интерфейсе [IOlkAccount](iolkaccount.md) учетной записи, с которого отправляются сообщения. 
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)
- [Свойства MAPI](http://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Каноническое свойство PidTagPrimarySendAccount](http://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

