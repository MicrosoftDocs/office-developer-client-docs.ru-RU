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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит состояние сообщения на основе сведений, доступных для пулера MAPI.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SPOOLER_STATUS  <br/> |
|Идентификатор:  <br/> |0x0E10  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |MAPI, не передаваемая  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство вычисляется MAPI для объектов сообщений.
  
Это свойство отображается только в входящие сообщения и зарезервировано во всех остальных случаях. В нем указывается, было ли доставлено сообщение в окончательное расположение или поставщик крюков для обмена сообщениями потенциально удалил сообщение при его повторной отправке.
  
Клиентские приложения никогда не должны устанавливать это свойство. Для входящие сообщения клиент или поставщик услуг может вызвать [IMAPIProp::GetProps](imapiprop-getprops.md) в этом свойстве, чтобы определить состояние сообщения. Значение S_OK указывает, что сообщение было успешно доставлено в хранилище сообщений. Значение, MAPI_E_OBJECT_DELETED указывает, что сообщение было удалено и никогда не было зафиксировано в магазине. 
  
Поставщики магазинов сообщений должны поддерживать это свойство в сообщениях, таблицах получателей и исходя из таблицы очередей. Клиенты и поставщики должны иметь возможность устанавливать столбцы на исходя из таблицы очередей и ограничивать их в зависимости от этого свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

