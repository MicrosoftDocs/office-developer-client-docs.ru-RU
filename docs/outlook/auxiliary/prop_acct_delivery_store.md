---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Представляет идентификатор элемента хранилища доставки по умолчанию для учетной записи.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418899"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Представляет идентификатор элемента хранилища доставки по умолчанию для учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунт](iolkaccount.md).
  
|||
|:-----|:-----|
|Идентификатор:  <br/> |0x0018  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Тег свойства:  <br/> |0x00180102  <br/> |
|Обращения  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

Получите или задайте значение этого свойства с помощью [иолкаккаунт::](iolkaccount-getprop.md) GetProperty или [Иолкаккаунт:: сетпроп](iolkaccount-setprop.md), соответственно.
  
Один из побочных эффектов задания хранилища в качестве хранилища доставки по умолчанию для учетной записи состоит в том, что при запуске Outlook создает папки поиска для этого хранилища, если они еще не существуют, и перечислите магазин в списке дел.
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)
- [Constants (Account management API)](constants-account-management-api.md)

