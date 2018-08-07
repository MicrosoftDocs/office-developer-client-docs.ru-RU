---
title: IMAPIGetSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession
api_type:
- COM
ms.assetid: d1b662e2-1516-46b2-ba94-4092d79b5a39
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 17c9a7ba54d7dd0b4d97c06f6343e563223f8100
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808972"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**Относится к**: Outlook 
  
Предоставляет доступ к текущему сеансу MAPI, связанного с объектом поддержки. Поставщики MAPI могут запрашивать их поддержка объект MAPI для этого интерфейса. Дополнительные сведения о поддержке объекты см [поддержки объектов](support-object-overview.md).
  
|||
|:-----|:-----|
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIGetSession  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetMAPISession](imapigetsession-getmapisession.md) <br/> |Вызывается, чтобы получить указатель текущего сеанса MAPI.  <br/> |
   
## <a name="see-also"></a>См. также



[GetMAPISession](imapigetsession-getmapisession.md)
  
[IMAPISupport](imapisupportiunknown.md)


[Интерфейсы MAPI](mapi-interfaces.md)
  
[Обзор поддержки объектов](support-object-overview.md)

