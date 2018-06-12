---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Представляет параметры транспорта, используемые Outlook для определения необходимости синхронизации задач и отключить элементы пользовательского интерфейса (UI), которые учетной записи не поддерживаются.
ms.openlocfilehash: 95b61ea994557be76303f8b9b0541353b6ed13f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807946"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Представляет параметры транспорта, используемые Outlook для определения необходимости синхронизации задач и отключить элементы пользовательского интерфейса (UI), которые учетной записи не поддерживаются.
  
## <a name="quick-info"></a>Краткие сведения

В разделе [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2010  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Свойство tag:  <br/> |0x20100102  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

Получение или задание этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.
  
Возвращает **MAPIACCT_SEND_ONLY** , если учетная запись можно только отправлять сообщения, но не могут получать сообщения. В этом случае Outlook отключает пользовательского интерфейса, который не применяется к этому типу учетные записи (например, пользовательский Интерфейс для **Отправки и получения**).
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

