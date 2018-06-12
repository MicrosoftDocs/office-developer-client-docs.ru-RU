---
title: PROP_ACCT_DELIVERY_FOLDER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a409c49b-b390-021e-2ec1-7a5932a0c8de
description: Представляет идентификатор записи папки доставки по умолчанию для учетной записи.
ms.openlocfilehash: 56b648b6a79e7497cab1980a86ca11d1c7a6aa3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807951"
---
# <a name="propacctdeliveryfolder"></a>PROP_ACCT_DELIVERY_FOLDER

Представляет идентификатор записи папки доставки по умолчанию для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0019  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x00190102  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

Получение или задание этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.
  
Папка доставки по умолчанию — **папки «Входящие»**.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

