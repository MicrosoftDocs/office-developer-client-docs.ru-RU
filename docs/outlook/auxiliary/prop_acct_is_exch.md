---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: Значение true, если учетная запись является учетной записью Exchange.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807930"
---
# <a name="propacctisexch"></a>PROP_ACCT_IS_EXCH

Значение true, если учетная запись является учетной записью Exchange.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0014  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Свойство tag:  <br/> |0x00140003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

