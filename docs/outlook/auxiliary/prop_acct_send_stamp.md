---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Возвращает accountsendstamp.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807934"
---
# <a name="propacctsendstamp"></a>PROP_ACCT_SEND_STAMP

Возвращает отметку учетной записи «отправить».
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x000E  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Свойство tag:  <br/> |0x000E001F  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

