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
description: 'Последнее изменение: 07 сентября 2016'
ms.openlocfilehash: 1720e9a2eeb54daed1e559f99b0c63ce09585419
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810873"
---
# <a name="pidtagattachmethod-canonical-property"></a>Каноническое свойство PidTagAttachMethod

 
  
**Относится к**: Outlook 
  
Содержит определенные MAPI константу, представляющее того, который может осуществляться содержимого вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_METHOD  <br/> |
|Идентификатор:  <br/> |0x3705  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство может иметь только один из следующих значений:
  
NO_ATTACHMENT 
  
> Вложение только что создано. 
    
ATTACH_BY_VALUE 
  
> Свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) содержит данные вложения. 
    
ATTACH_BY_REFERENCE 
  
> **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) или свойство **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) содержит полный путь, идентифицирующий вложения получателям с доступом к общего файла сервер. 
    
ATTACH_BY_REF_RESOLVE 
  
> Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, идентифицирующий вложение. 
    
ATTACH_BY_REF_ONLY 
  
> Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, идентифицирующий вложение. 
    
ATTACH_EMBEDDED_MSG 
  
> Свойство **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) содержит внедренный объект, который поддерживает интерфейс **IMessage** . 
    
ATTACH_OLE 
  
> Вложение представляет внедренный объект OLE.
    
ATTACH_BY_WEBREFERENCE 
  
> Содержимое вложения не в сообщении. 
    
При создании, вложения у каждого объекта есть начальное значение **PR_ATTACH_METHOD** **NO_ATTACHMENT**. 
  
Клиентские приложения и поставщиков услуг только необходимых для поддержки метод вложения, представленный значением **ATTACH_BY_VALUE** . Другие методы вложения являются необязательными. Хранилище сообщений не требует принудительного согласованность значение **PR_ATTACH_METHOD** и значения свойства вложения. 
  
Для полные пути, которые можно использовать с **ATTACH_BY_REFERENCE** и **ATTACH_BY_REF_ONLY**рекомендуются универсальных имен именования соглашение (UNC). С помощью **ATTACH_BY_REF_RESOLVE**абсолютный путь быстрее, так как диспетчер очереди MAPI преобразует вложения в **ATTACH_BY_VALUE**. 
  
Если значение **ATTACH_BY_REFERENCE** , **PR_ATTACH_DATA_BIN** должен быть пустым. Исходящие шлюза можно преобразовать **ATTACH_BY_REFERENCE** вложения в **ATTACH_BY_VALUE** вложения, скопировав данные вложения в свойстве **PR_ATTACH_DATA_BIN** . 
  
Если значение **ATTACH_BY_REF_RESOLVE** , **PR_ATTACH_DATA_BIN** должен быть пустым. При отправке сообщения с вложением **ATTACH_BY_REF_RESOLVE** диспетчер очереди MAPI копирует данные вложения в **ATTACH_BY_VALUE** вложения. Этот процесс разрешения помещает данные вложения в **PR_ATTACH_DATA_BIN**. 
  
Если значение **ATTACH_BY_REF_ONLY** , **PR_ATTACH_DATA_BIN** должна быть пустой и системы обмена сообщениями никогда не разрешает ссылку вложения. Это значение используется, когда требуется отправить ссылку, но не данные. 
  
Если объект OLE в формате OLE 2.0 **IStorage** , данных доступен через **PR_ATTACH_DATA_OBJ**. Если объект OLE в формате OLE 1.0 **OLESTREAM** , данных доступен через **PR_ATTACH_DATA_BIN** как интерфейс **IStream**. Можно определить тип кодировки OLE по значению **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Дополнительные сведения о интерфейсов OLE и форматы *OLE Справочник программиста* см. 
  
## <a name="remarks"></a>Замечания

При **ATTACH_BY_WEBREFERENCE** **PR_ATTACH_METHOD** не является содержимое вложения в сообщении. Вместо этого свойство **PR_ATTACH_LONG_FILENAME** содержит абсолютный URL-адрес для содержимого вложения, которая хранится в Интернете. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

