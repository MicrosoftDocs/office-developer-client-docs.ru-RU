---
title: Каноническое свойство PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326637"
---
# <a name="pidtagbody-canonical-property"></a>Каноническое свойство PidTagBody

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит текст сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_BODY, PR_BODY_A PR_BODY_W  <br/> |
|Идентификатор:  <br/> |0x1000  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства обычно используются только в межпользовательских сообщениях (IPM). 
  
Хранилища сообщений, поддерживающие формат RTF, игнорируют все изменения пробелов в тексте сообщения. При первом сохранении **PR_BODY** в хранилище сообщений также генерируется и сохраняется свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), в формате RTF отображается текст сообщения. Если затем вызывается метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) и **PR_BODY** был изменен, хранилище сообщений вызывает функцию [ртфсинк](rtfsync.md) , чтобы обеспечить синхронизацию с версией RTF. Если было изменено только пустое пространство, свойства остаются неизменными. При этом сохраняется любое нетривиальное форматирование RTF, когда сообщение проходит через клиентов, не поддерживающих RTF, и систем обмена сообщениями. 
  
Значение этого свойства должно быть выражено на кодовой странице операционной системы, в которой выполняется служба MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

