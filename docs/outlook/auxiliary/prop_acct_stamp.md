---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Возвращает штамп учетной записи.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19807953"
---
# <a name="propacctstamp"></a>PROP_ACCT_STAMP

Возвращает штамп учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x000D  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Свойство tag:  <br/> |0x000D001F  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md). При попытке установить для этого свойства, данное свойство возвращает **E_OLK_PROP_READ_ONLY**. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

