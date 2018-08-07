---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Представляет идентификатор записи хранилища доставки по умолчанию для учетной записи.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807933"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Представляет идентификатор записи хранилища доставки по умолчанию для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0018  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x00180102  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

Получение или задание этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.
  
Один из побочные эффекты Установка хранилища в качестве хранилища доставки по умолчанию для учетной записи — это, что при запуске Outlook, Outlook создает папки поиска для этого хранилища, если они еще не существует и список дел в хранилище.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)
- [Constants (Account management API)](constants-account-management-api.md)

