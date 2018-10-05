---
title: PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e1bc4900-d261-f692-386b-139ef6960212
description: Указывает основной accountsendstamp для сообщения.
ms.openlocfilehash: 902c71bd4a1bd5a25ab50c4b26bcfa6d5e8489e6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394086"
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
- [Свойства MAPI](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx)
- [Каноническое свойство PidTagPrimarySendAccount](https://msdn.microsoft.com/library/2f268b3b-2e4c-4aea-8879-bdd0ac1df35c%28Office.15%29.aspx)

