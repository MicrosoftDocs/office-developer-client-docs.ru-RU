---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Возвращает уникальный идентификатор учетной записи в профилях Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409435"
---
# <a name="prop_acct_mini_uid"></a>PROP_ACCT_MINI_UID

Возвращает уникальный идентификатор учетной записи в профилях Outlook.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0003  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тег свойства:  <br/> |0x00030003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). Если клиент пытается установить это свойство, это свойство возвращает E_OLK_PROP_READ_ONLY **.** 
  
Это свойство отличается от [PROP_ACCT_ID](prop_acct_id.md) тем, что его значение уникально идентифицирует учетную запись в профиле, в котором была создана учетная запись, и за ее пределами, в то время как **PROP_ACCT_ID** является уникальной только для всех учетных записей в том профиле, в котором была создана учетная запись. Когда сообщение с этими свойствами перемещается на второй компьютер с другим профилем Outlook **и другим** набором учетных записей, PROP_ACCT_MINI_UID может уникальным образом определить исходную учетную запись в исходном профиле. Однако **PROP_ACCT_ID** может конфликтовть с учетной записью в профиле второго компьютера. 
  
## <a name="see-also"></a>См. также

- [PROP_ACCT_ID](prop_acct_id.md)  
- [Сведения об API управления учетными записями](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

