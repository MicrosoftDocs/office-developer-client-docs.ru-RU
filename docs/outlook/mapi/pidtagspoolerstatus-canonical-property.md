---
title: Каноническое свойство PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d04144a4f5ef714b59b608bfe19367bcb3c1ced8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588575"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Каноническое свойство PidTagSpoolerStatus

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отображается состояние сообщения на основе сведений, которые могут диспетчер очереди MAPI.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Идентификатор:  <br/> |0x0E10  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство вычисляется путем MAPI на объекты сообщений.
  
Это свойство отображается только входящих сообщений и зарезервирован во всех остальных случаях. Он указывает ли сообщение было доставлено в конечное расположение или обмена мгновенными сообщениями поставщика обработчик потенциально удалена ли сообщение во время его маршрутизации.
  
Клиентские приложения никогда не следует устанавливать это свойство. Для входящего сообщения клиента или поставщика можно вызвать [IMAPIProp::GetProps](imapiprop-getprops.md) на это свойство, чтобы определить состояние сообщения. Значение S_OK указывает, что сообщение было успешно доставлено в хранилище сообщений. Значение MAPI_E_OBJECT_DELETED указывает, что сообщение было удалено и никогда не было зафиксировано в хранилище. 
  
Поставщики хранилища сообщений должны поддерживать это свойство на сообщения, получателя таблиц и таблице исходящей очереди. Клиенты и поставщики должна появиться возможность задать столбцы в таблице исходящей очереди и ограничения на основе этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

