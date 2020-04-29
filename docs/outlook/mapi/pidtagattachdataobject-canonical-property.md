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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит объект вложения, доступ к которому обычно осуществляется с помощью интерфейса OLE **IStorage** для связывания и внедрения объектов. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит вложение, когда значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) равно **ATTACH_EMBEDDED_MSG** или **ATTACH_OLE**. Тип кодировки OLE можно определить на основе **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Для вложений, связанных со значением **ATTACH_EMBEDDED_MSG** , интерфейс [iMessage: IMAPIProp](imessageimapiprop.md) можно использовать для более быстрого доступа. 
  
Для внедренного динамического объекта OLE свойство **PR_ATTACH_DATA_OBJ** содержит собственные сведения о отрисовке, а свойство **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) должно быть либо несуществующим, либо пустым. 
  
Для вложенного файла документа OLE поставщик хранилища сообщений должен отвечать на вызов [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) на **PR_ATTACH_DATA_OBJ** , а также может отвечать на вызов на **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)). Свойства **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** используют один и тот же идентификатор свойства, поэтому они являются двумя представлениями одного и того же свойства. 
  
Для объекта хранилища, такого как составной файл в формате OLE 2,0 докфиле, некоторые поставщики услуг позволяют открыть его с помощью интерфейса MAPI **помощью istreamdocfile** , который является подклассом **IStream** без дополнительных членов, предназначенный для оптимизации производительности. Для того чтобы выполнить попытку открыть **PR_ATTACH_DATA_OBJ** через **помощью istreamdocfile**, достаточно сэкономить возможность. Если возвращается **MAPI_E_INTERFACE_NOT_SUPPORTED** , клиент может открыть **PR_ATTACH_DATA_BIN** с помощью **IStream**. 
  
Если клиентскому приложению или поставщику услуг не удается открыть вложенный объект с помощью **PR_ATTACH_DATA_OBJ** с помощью **PR_ATTACH_METHOD**, необходимо использовать **PR_ATTACH_DATA_BIN**. 
  
Дополнительные сведения о OLE interfaces и formats можно найти в статье [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
## <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

