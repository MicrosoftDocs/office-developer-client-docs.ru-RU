---
title: Сохранение свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425892"
---
# <a name="saving-mapi-properties"></a>Сохранение свойств MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Многие объекты поддерживают модель обработки транзакций, при которой изменения свойств не делаются постоянными, пока они не будут совершены позднее. Если изменения свойств обрабатываются методами [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) то шаг фиксации обрабатывается [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Доступ к последней версии свойств объекта можно получить только после успешного вызова **в SaveChanges.** 
  
Когда **SaveChanges** возвращает значение ошибки MAPI_E_OBJECT_CHANGED, это предупреждение о том, что другой клиент одновременно совершает изменения в объекте. В зависимости от поставщика, реализуемого объекта, нескольким клиентам можно успешно открыть объект, позвонив его **методу OpenEntry** с набором флага MAPI_MODIFY, предоставляя им доступ к чтением и записи. Объект, возвращаемый с такого **вызова OpenEntry,** — это снимок данных хранилища. Каждая последующая попытка изменить эти данные может переписать предыдущую попытку. 
  
После получения MAPI_E_OBJECT_CHANGED из **SaveChanges** клиент имеет возможность: 
  
- Сделайте копию объекта для удержания изменений.
    
- Сделайте еще один вызов **в SaveChanges,** указав FORCE_SAVE. 
    
Вызов **SaveChanges** с флагом FORCE_SAVE переоценки предыдущего сохранения и делает изменения клиента постоянными. 
  
## <a name="see-also"></a>См. также



[Обзор свойств MAPI](mapi-property-overview.md)

