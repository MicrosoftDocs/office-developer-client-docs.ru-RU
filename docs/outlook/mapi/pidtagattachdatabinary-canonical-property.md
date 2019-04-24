---
title: Каноническое свойство PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356548"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Каноническое свойство PidTagAttachDataBinary

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит двоичные данные вложения, доступ к которым осуществляется с помощью интерфейса OLE (технология **** связывания и внедрения объектов). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_ДАТА_БИН  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит вложение, когда значение свойства **пр_аттач_месод** ([PIDTAGATTACHMETHOD](pidtagattachmethod-canonical-property.md)) равно аттач_би_валуе, которое является обычным методом вложения и только один, который требуется для поддержки. **Пр_аттач_дата_бин** также содержит вложение OLE 1,0 **олестреам** , когда значение **пр_аттач_месод** равно аттач_оле. 
  
 Вложения **олестреам** можно скопировать в файл, вызвав метод OLE **IStream:: CopyTo** . Тип кодирования OLE можно определить в свойстве **пр_аттач_таг** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Для вложенного файла документа OLE поставщик хранилища сообщений должен отвечать на вызов [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) на **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), а также может ответить на вызов в **пр_аттач_дата_бин **. Обратите внимание, что **пр_аттач_дата_бин** и **пр_аттач_дата_обж** совместно используют один и тот же идентификатор свойства и, таким образом, являются двумя представлениями одного и того же свойства. 
  
Для объекта хранилища, например составного файла в формате OLE 2,0 докфиле, некоторые поставщики услуг позволяют открыть его с помощью интерфейса MAPI **помощью istreamdocfile** для улучшения производительности. Поставщик, который поддерживает **помощью istreamdocfile** , должен предоставлять его в **пр_аттач_дата_обж** и может при необходимости предоставлять его в **пр_аттач_дата_бин**. 
  
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

