---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Представляет ИД записи для стандартного хранения доставки для учетной записи.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418899"
---
# <a name="prop_acct_delivery_store"></a>PROP_ACCT_DELIVERY_STORE

Представляет ИД записи для стандартного хранения доставки для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0018  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x00180102  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

Получите или установите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.
  
Одним из побочных эффектов настройки магазина в качестве стандартного хранения доставки для учетной записи является то, что при запуске Outlook создает папки поиска для этого магазина, если они еще не существуют, и перечисляет его в To-Do Bar.
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)
- [Constants (Account management API)](constants-account-management-api.md)

