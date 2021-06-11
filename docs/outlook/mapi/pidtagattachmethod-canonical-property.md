---
title: Каноническое свойство PidTagAttachMethod
manager: soliver
ms.date: 9/7/2016
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMethod
api_type:
- HeaderDef
ms.assetid: 32089213-ef7b-4152-84ab-b44e9911332b
description: 'Последнее изменение: 07 сентября 2016 г.'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327260"
---
# <a name="pidtagattachmethod-canonical-property"></a>Каноническое свойство PidTagAttachMethod

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит констант, определяемую MAPI, представляющую способ доступа к содержимому вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_METHOD  <br/> |
|Идентификатор:  <br/> |0x3705  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь одно из следующих значений:
  
NO_ATTACHMENT 
  
> Вложение только что создано. 
    
ATTACH_BY_VALUE 
  
> Свойство **PR_ATTACH_DATA_BIN** [(PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)содержит данные вложения. 
    
ATTACH_BY_REFERENCE 
  
> Свойство **PR_ATTACH_PATHNAME** [(PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)или **PR_ATTACH_LONG_PATHNAME** [(PidTagAttachLongPathname)](pidtagattachlongpathname-canonical-property.md)содержит полностью квалифицированный путь, определяющий вложение получателей с доступом к общему серверу файлов. 
    
ATTACH_BY_REF_RESOLVE 
  
> Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полностью квалифицированный путь, определяющий вложение. 
    
ATTACH_BY_REF_ONLY 
  
> Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полностью квалифицированный путь, определяющий вложение. 
    
ATTACH_EMBEDDED_MSG 
  
> Свойство **PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)содержит встроенный объект, который поддерживает **интерфейс IMessage.** 
    
ATTACH_OLE 
  
> Вложение — это встроенный объект OLE.
    
ATTACH_BY_WEBREFERENCE 
  
> Содержимое вложения не находится в сообщении. 
    
После создания все объекты вложения имеют начальное **PR_ATTACH_METHOD** значение **NO_ATTACHMENT**. 
  
Клиентские приложения и поставщики услуг необходимы только для поддержки  метода вложения, представленного ATTACH_BY_VALUE значением. Другие методы вложения необязательны. Хранилище сообщений не обеспечивает согласованность между значением **PR_ATTACH_METHOD** и значениями других свойств вложений. 
  
Универсальные имена конвенции о именованиях (UNC) рекомендуется использовать для полностью  квалифицированных путей, которые следует использовать с ATTACH_BY_REFERENCE **и ATTACH_BY_REF_ONLY**. С **ATTACH_BY_REF_RESOLVE** абсолютный путь быстрее, так как шпалер MAPI преобразует вложение **в ATTACH_BY_VALUE**. 
  
Если **ATTACH_BY_REFERENCE** установлено, **PR_ATTACH_DATA_BIN** должны быть пустыми. Исходящие шлюзы могут  превратить ATTACH_BY_REFERENCE в ATTACH_BY_VALUE, **копируя** данные вложения в **свойство PR_ATTACH_DATA_BIN.** 
  
Если **ATTACH_BY_REF_RESOLVE** установлено, **PR_ATTACH_DATA_BIN** должны быть пустыми. При отправлении **сообщения ATTACH_BY_REF_RESOLVE** вложения, пуллер MAPI копирует данные **вложения** в ATTACH_BY_VALUE вложение. Этот процесс разрешения помещает данные вложения в **PR_ATTACH_DATA_BIN**. 
  
Если **ATTACH_BY_REF_ONLY** **установлено,** PR_ATTACH_DATA_BIN должно быть пустым, а система обмена сообщениями никогда не разрешит ссылку на вложения. Используйте это значение, если вы хотите отправить ссылку, но не данные. 
  
Когда объект OLE находится в формате **IStorage** OLE 2.0, данные доступны через **PR_ATTACH_DATA_OBJ**. Когда объект OLE находится в формате OLE 1.0 **OLESTREAM,** данные доступны через PR_ATTACH_DATA_BIN как **IStream.**  Тип кодировки OLE можно определить по значению **PR_ATTACH_TAG** [(PidTagAttachTag).](pidtagattachtag-canonical-property.md) 
  
Дополнительные сведения об интерфейсах и форматах OLE см. в справке *к программисту OLE.* 
  
## <a name="remarks"></a>Примечания

Если **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE,** содержимое вложения не находится в сообщении. Вместо этого **PR_ATTACH_LONG_FILENAME** содержит абсолютный URL-адрес содержимого вложения, хранимого в Интернете. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

