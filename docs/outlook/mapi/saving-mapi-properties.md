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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Многие объекты поддерживают модель транзакций обработки, при которой изменения свойств не будут постоянны, пока не будут зафиксированы позже. В то время как изменения свойств обрабатываются методами [IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::D eleteProps,](imapiprop-deleteprops.md) этап фиксации обрабатывается [методом IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Доступ к последней версии свойств объекта можно получить только после успешного вызова **SaveChanges.** 
  
Когда **SaveChanges** возвращает значение ошибки MAPI_E_OBJECT_CHANGED, это предупреждение о том, что другой клиент одновременно внося изменения в объект. В зависимости от поставщика, реализующих объект, несколько клиентов могут успешно открыть объект, вызывая его метод **OpenEntry** с установленным флагом MAPI_MODIFY, предоставляя им доступ для чтения и записи. Объект, который возвращается из такого вызова **OpenEntry,** является моментальный снимок данных хранилища. Каждая последующие попытки изменить эти данные могут переписать предыдущую попытку. 
  
Получив MAPI_E_OBJECT_CHANGED из **SaveChanges,** клиент может: 
  
- Сделайте копию объекта для удержания изменений.
    
- Еще раз вызовите **SaveChanges,** указав FORCE_SAVE. 
    
Вызов **SaveChanges** с флагом FORCE_SAVE переоценит предыдущее сохранение и сделает изменения клиента постоянными. 
  
## <a name="see-also"></a>См. также



[Обзор свойств MAPI](mapi-property-overview.md)

