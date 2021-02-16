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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330123"
---
# <a name="pidtagresponsibility-canonical-property"></a>Каноническое свойство PidTagResponsibility

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если какой-либо поставщик транспорта уже принял на себя ответственность за доставку сообщения этому получателю, и FALSE, если пулер MAPI считает, что этот поставщик транспорта должен взять на себя ответственность.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESPONSIBILITY  <br/> |
|Идентификатор:  <br/> |0x0E0F  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |MAPI, не передаваемый  <br/> |
   
## <a name="remarks"></a>Примечания

Когда пулер MAPI представляет исходящие сообщения поставщику транспорта через [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md)он устанавливает для этого свойства false для всех получателей, для которых пулер MAPI считает, что этот поставщик транспорта отвечает, и TRUE для всех остальных получателей. Поставщик транспорта должен попытаться обработать всех получателей с PR_RESPONSIBILITY **false.** После успешной отправки или неудачной отправки получателю поставщик транспорта должен установить для этого свойства в текстовом сообщении true, чтобы указать, что он несет ответственность за этого получателя. 
  
Если после проверки получателя поставщик транспорта решает, что не может или не  должен обработать его, поставщик транспорта должен оставить PR_RESPONSIBILITY false. Затем пулер MAPI будет искать другого поставщика транспорта, который может обработать этого получателя. Пулер MAPI создает отчет о ненастройке для всех получателей, ответственность за которые не несет ни один поставщик транспорта. 
  
Если поставщик транспорта пытается доставить сообщение, он должен вызвать метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы указать MAPI причины сбоя, чтобы MAPI смог создать отчет о ненастройстве. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[������������ �������� PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

