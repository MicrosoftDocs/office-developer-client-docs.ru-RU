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
  
Содержит объект вложения, обычно доступный через интерфейс **IStorage** для связывания и встраивления объектов (OLE). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_DATA_OBJ  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство содержит вложение, если значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)ATTACH_EMBEDDED_MSG **или** **ATTACH_OLE**. Тип кодиировки OLE можно определить по PR_ATTACH_TAG **(** [PidTagAttachTag).](pidtagattachtag-canonical-property.md) 
  
Для вложения, связанного **со значением ATTACH_EMBEDDED_MSG,** интерфейс [IMessage:IMAPIProp](imessageimapiprop.md) можно использовать для ускорения доступа. 
  
Для внедренного динамического объекта OLE свойство **PR_ATTACH_DATA_OBJ** содержит собственные сведения об отрисовке, а свойство **PR_ATTACH_RENDERING** ([PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)должно быть несущестным или пустым. 
  
Для вложенного файла документа OLE поставщик хранения сообщений должен ответить на вызов [IMAPIProp::OpenProperty](imapiprop-openproperty.md) по **PR_ATTACH_DATA_OBJ** и при желании ответить на вызов PR_ATTACH_DATA_BIN **(** [PidTagAttachDataBinary).](pidtagattachdatabinary-canonical-property.md) Свойства **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** имеют один и тот же идентификатор свойства и, следовательно, являются двумя вариантами одного и того же свойства. 
  
Для объекта хранилища, например составного файла в формате docfile OLE 2.0, некоторые поставщики услуг позволяют открывать его с помощью интерфейса MAPI **IStreamDocfile,** **подкласса IStream** без дополнительных членов, предназначенных для оптимизации производительности. Возможного сохранения достаточно, чтобы обосновать попытки открыть PR_ATTACH_DATA_OBJ **через** **IStreamDocfile.** Если **MAPI_E_INTERFACE_NOT_SUPPORTED** возвращается, клиент может открыть  PR_ATTACH_DATA_BIN **iStream.** 
  
Если клиентского приложения или поставщика службы не  удается открыть подпроект вложения с помощью PR_ATTACH_DATA_OBJ с помощью **PR_ATTACH_METHOD,** он должен **использовать PR_ATTACH_DATA_BIN**. 
  
Дополнительные сведения об интерфейсах и форматах OLE см. в [OLE и передаче данных.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
## <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

