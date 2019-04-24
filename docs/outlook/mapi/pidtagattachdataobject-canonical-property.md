---
title: Каноническое свойство PidTagAttachDataObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339286"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Каноническое свойство PidTagAttachDataObject

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит объект вложения, доступ к которому обычно осуществляется с помощью интерфейса OLE **IStorage** для связывания и внедрения объектов. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_ДАТА_ОБЖ  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |ПТ_ОБЖЕКТ  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство содержит вложение, когда значение свойства **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) равно **аттач_ембеддед_мсг** или **аттач_оле**. Тип кодирования OLE можно определить из **пр_аттач_таг** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Для вложений, связанных со значением **аттач_ембеддед_мсг** , можно использовать интерфейс [iMessage: IMAPIProp](imessageimapiprop.md) для более быстрого доступа. 
  
Для внедренного динамического объекта OLE свойство **пр_аттач_дата_обж** содержит собственные сведения о отрисовке, а свойство **пр_аттач_рендеринг** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) должно быть либо несуществующим, либо пустым. 
  
Для вложенного файла документа OLE поставщик хранилища сообщений должен отвечать на вызов [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) на **пр_аттач_дата_обж** , а также может ответить на вызов в **пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). Свойства **пр_аттач_дата_бин** и **пр_аттач_дата_обж** используют один и тот же идентификатор свойства, поэтому они являются двумя представлениями одного и того же свойства. 
  
Для объекта хранилища, такого как составной файл в формате OLE 2,0 докфиле, некоторые поставщики услуг позволяют открыть его с помощью интерфейса MAPI **помощью istreamdocfile** , который является подКлассом **IStream** без дополнительных членов, предназначенный для оптимизации производительности. Для того, чтобы выровнять попытки открыть **пр_аттач_дата_обж** через **помощью istreamdocfile**, достаточно сэкономить. Если возвращается **мапи_е_интерфаце_нот_суппортед** , клиент может открыть **Пр_аттач_дата_бин** с помощью **IStream**. 
  
Если клиентское приложение или поставщик услуг не может открыть вложенный объект с помощью **пр_аттач_дата_обж** с помощью **пр_аттач_месод**, он должен использовать **пр_аттач_дата_бин**. 
  
Дополнительные сведения о OLE interfaces и formats можно найти в статье [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
## <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

