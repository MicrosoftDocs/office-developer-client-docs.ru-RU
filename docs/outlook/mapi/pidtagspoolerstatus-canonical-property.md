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
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408679"
---
# <a name="pidtagspoolerstatus-canonical-property"></a>Каноническое свойство PidTagSpoolerStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит состояние сообщения на основе сведений, доступных для диспетчера очереди MAPI.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Идентификатор:  <br/> |0x0E10  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Несъемный MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство вычисляется MAPI для объектов Message.
  
Это свойство отображается только для входящих сообщений и зарезервировано во всех остальных случаях. Указывает, было ли сообщение доставлено в конечное расположение или же может ли поставщик обработчика сообщений удалить сообщение при его повторной маршрутизации.
  
Клиентские приложения никогда не должны задавать это свойство. Для входящего сообщения клиент или поставщик услуг может вызвать [IMAPIProp::/PROPS](imapiprop-getprops.md) для этого свойства, чтобы определить состояние сообщения. Значение S_OK указывает, что сообщение было успешно доставлено в хранилище сообщений. Значение MAPI_E_OBJECT_DELETED указывает на то, что сообщение было удалено и не было зафиксировано в хранилище. 
  
Поставщики хранилища сообщений должны поддерживать это свойство в сообщениях, таблицах получателей и таблице исходящей очереди. Клиенты и поставщики должны иметь возможность задавать столбцы в таблице исходящей очереди и ограничиваться в соответствии с этим свойством.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

