---
title: Каноническое свойство PidTagResponsibility
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393816"
---
# <a name="pidtagresponsibility-canonical-property"></a>Каноническое свойство PidTagResponsibility

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если некоторые поставщика транспорта уже принял ответственность за доставки сообщения для получателя и FALSE, если диспетчер очереди MAPI учитывает принятие данного поставщика транспорта ответственности.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESPONSIBILITY  <br/> |
|Идентификатор:  <br/> |0x0E0F  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |MAPI передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

При диспетчер очереди MAPI представляет исходящее сообщение поставщика транспорта, через [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)его этому свойству значение FALSE для всех получателей, для которых диспетчер очереди MAPI учитывает этого поставщика транспорта ответственность и значение TRUE для всех получатели. Поставщика транспорта производится попытка обработки всех получателей с **PR_RESPONSIBILITY** задано значение FALSE. После успешной отправки или conclusively восстановления после сбоя для отправки получателю, поставщика транспорта следует этому свойству присвоено значение TRUE в сообщении источник, чтобы указать, что ответственность за этот получатель принял. 
  
Если после проверки получателя, поставщика транспорта решает, что не может или не должен обрабатывать, поставщика транспорта, следует оставить **PR_RESPONSIBILITY** set значение FALSE. Диспетчер очереди MAPI будет искать другого поставщика транспорта, который может обрабатывать получателя. Диспетчер очереди MAPI в конечном счете создает отчет о недоставке для получателей, для которых отсутствует транспорт принимает ответственности. 
  
Если поставщика транспорта пытается и не удается доставить сообщение, он должен вызвать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для указания MAPI причины сбоя, чтобы MAPI можно создать отчет о недоставке. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[������������ �������� PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

