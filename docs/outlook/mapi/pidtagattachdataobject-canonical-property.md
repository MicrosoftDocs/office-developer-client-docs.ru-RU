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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398075"
---
# <a name="pidtagattachdataobject-canonical-property"></a>Каноническое свойство PidTagAttachDataObject

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит объект вложения, обычно доступе через интерфейс объекта связывания и внедрения (OLE) **IStorage** . 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит вложения, когда значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) **ATTACH_EMBEDDED_MSG** или **ATTACH_OLE**. Можно определить тип кодировки OLE из **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Для вложения, связанные со значением **ATTACH_EMBEDDED_MSG** интерфейс [IMessage:IMAPIProp](imessageimapiprop.md) можно использовать для более быстрого доступа. 
  
Свойство **PR_ATTACH_DATA_OBJ** содержит собственные данные для отображения динамических внедренный объект OLE, и свойство **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) должны быть пустой или несуществующий. 
  
Для вложения файла документа OLE поставщика хранилища сообщений, необходимо ответить на звонок [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на **PR_ATTACH_DATA_OBJ** и при необходимости может ответить на звонок на **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ). Свойства **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** совместно использовать один и тот же идентификатор свойства и таким образом, два представления одного свойства. 
  
Для объекта хранилища такие как составной файл в формате документа OLE 2.0, некоторых поставщиков услуг позволяет открыть с помощью интерфейса MAPI **IStreamDocfile** подкласс **IStream** без дополнительных членов, предназначено для оптимизации производительности. Потенциальные сохранением является достаточно попыткой открыть **PR_ATTACH_DATA_OBJ** через **IStreamDocfile**. Если возвращаются **MAPI_E_INTERFACE_NOT_SUPPORTED** клиента можно открыть **PR_ATTACH_DATA_BIN** с **IStream**. 
  
Если клиентское приложение или поставщик услуг не могут открыть вложенные объекты вложения с помощью **PR_ATTACH_DATA_OBJ** с помощью **PR_ATTACH_METHOD**, следует использовать **PR_ATTACH_DATA_BIN**. 
  
Дополнительные сведения о интерфейсов OLE и форматов видеть [OLE и передачи данных](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
## <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

