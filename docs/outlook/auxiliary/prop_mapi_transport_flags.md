---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые учетная запись не поддерживает.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404528"
---
# <a name="prop_mapi_transport_flags"></a>PROP_MAPI_TRANSPORT_FLAGS

Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые учетная запись не поддерживает.
  
## <a name="quick-info"></a>Краткие сведения

См. [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2010  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x20100102  <br/> |
|Access:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

Получите или установите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md) или [IOlkAccount::SetProp](iolkaccount-setprop.md)соответственно.
  
Возвращает **MAPIACCT_SEND_ONLY,** если учетная запись может отправлять только сообщения, но не может получать сообщения. В этом случае Outlook отключает пользовательский интерфейс, не применимый к учетным записям этого типа (например, пользовательский интерфейс для отправки **и получения).**
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

