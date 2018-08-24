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
ms.openlocfilehash: 90fe316bfd11d712f02187b6a569450b747a6409
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587931"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

