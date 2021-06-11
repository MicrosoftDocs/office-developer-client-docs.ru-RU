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
  
Содержит двоичные данные вложения, обычно доступные с помощью интерфейса **IStream,** связывающих объекты и встраив их. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит вложение, когда значение **свойства PR_ATTACH_METHOD** [(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)ATTACH_BY_VALUE, которое является обычным методом вложения и единственным, которое необходимо поддерживать. **PR_ATTACH_DATA_BIN** также содержит вложение OLE 1.0 **OLESTREAM,** если значение PR_ATTACH_METHOD ATTACH_OLE.  
  
 **Вложения OLESTREAM** можно скопировать в файл, позвонив по методу OLE **IStream::CopyTo.** Тип кодировки OLE можно определить из **свойства PR_ATTACH_TAG** [(PidTagAttachTag).](pidtagattachtag-canonical-property.md) 
  
Для вложения в файл OLE поставщик хранения сообщений должен отвечать на вызов [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **по PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)и может необязательно отвечать на **вызов PR_ATTACH_DATA_BIN**. Обратите **внимание, PR_ATTACH_DATA_BIN** **и PR_ATTACH_DATA_OBJ** имеют один и тот же идентификатор свойств и таким образом являются двумя renditions одного и того же свойства. 
  
Для объекта хранения, например сложного файла в формате docfile OLE 2.0, некоторые поставщики услуг позволяют открывать его с интерфейсом **MAPI IStreamDocfile** для повышения производительности. Поставщик, который поддерживает **IStreamDocfile,**  должен PR_ATTACH_DATA_OBJ его на PR_ATTACH_DATA_BIN **.** 
  
Дополнительные сведения об интерфейсах и форматах OLE см. в [OLE и Data Transfer.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
## <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

