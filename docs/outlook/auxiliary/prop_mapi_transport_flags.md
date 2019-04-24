---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые не поддерживаются учетной записью.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326483"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые не поддерживаются учетной записью.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x2010  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x20100102  <br/> |
|Обращения  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

Получите или задайте значение этого свойства с помощью [иолкаккаунт::](iolkaccount-getprop.md) GetProperty или [Иолкаккаунт:: сетпроп](iolkaccount-setprop.md), соответственно.
  
Возвращает **мапиаккт_сенд_онли** , если учетная запись может отправлять только сообщения, но не может получать сообщения. В этом случае Outlook отключает пользовательский интерфейс, который не применяется к учетным записям этого типа (например, Пользовательский интерфейс для **отправки и получения**).
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

