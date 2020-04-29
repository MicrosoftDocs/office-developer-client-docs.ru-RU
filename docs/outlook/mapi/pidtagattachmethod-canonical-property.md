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
description: 'Дата последнего изменения: 07 сентября 2016 г.'
ms.openlocfilehash: b84549ab31c939b4e6115795916ebd3520a96dbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327260"
---
# <a name="pidtagattachmethod-canonical-property"></a>Каноническое свойство PidTagAttachMethod

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит константу, определенную MAPI, которая представляет способ доступа к содержимому вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_METHOD  <br/> |
|Идентификатор:  <br/> |0x3705  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь только одно из следующих значений:
  
NO_ATTACHMENT 
  
> Вложение только что было создано. 
    
ATTACH_BY_VALUE 
  
> Свойство **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) содержит данные вложений. 
    
ATTACH_BY_REFERENCE 
  
> Свойство **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) или **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)) содержит полный путь, указывающий вложение получателям, у которых есть доступ к общему файловому серверу. 
    
ATTACH_BY_REF_RESOLVE 
  
> Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, указывающий вложение. 
    
ATTACH_BY_REF_ONLY 
  
> Свойство **PR_ATTACH_PATHNAME** или **PR_ATTACH_LONG_PATHNAME** содержит полный путь, указывающий вложение. 
    
ATTACH_EMBEDDED_MSG 
  
> Свойство **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) содержит внедренный объект, поддерживающий интерфейс **iMessage** . 
    
ATTACH_OLE 
  
> Вложение является внедренным объектом OLE.
    
ATTACH_BY_WEBREFERENCE 
  
> Содержимое вложения отсутствует в сообщении. 
    
При создании все объекты вложения имеют начальное значение **PR_ATTACH_METHOD** **NO_ATTACHMENT**. 
  
Клиентские приложения и поставщики услуг необходимы только для поддержки метода вложения, представленного значением **ATTACH_BY_VALUE** . Другие методы вложения являются необязательными. Хранилище сообщений не обеспечивает согласованности между значением **PR_ATTACH_METHOD** и значениями других свойств вложения. 
  
Имена в формате UNC рекомендуются для полных путей, которые следует использовать с **ATTACH_BY_REFERENCE** и **ATTACH_BY_REF_ONLY**. При **ATTACH_BY_REF_RESOLVE**абсолютный путь выполняется быстрее, так как диспетчер очереди MAPI преобразует вложение в **ATTACH_BY_VALUE**. 
  
Если параметр **ATTACH_BY_REFERENCE** задан, **PR_ATTACH_DATA_BIN** должен быть пустым. Исходящий шлюз может превратить **ATTACH_BY_REFERENCE** вложение в вложение **ATTACH_BY_VALUE** , скопировав данные вложений в свойство **PR_ATTACH_DATA_BIN** . 
  
Если параметр **ATTACH_BY_REF_RESOLVE** задан, **PR_ATTACH_DATA_BIN** должен быть пустым. При отправке сообщения, содержащего вложение **ATTACH_BY_REF_RESOLVE** , диспетчер очереди MAPI копирует данные вложений в **ATTACH_BY_VALUE** вложение. В этом процессе разрешения данные вложений размещаются в **PR_ATTACH_DATA_BIN**. 
  
Если задано значение **ATTACH_BY_REF_ONLY** , **PR_ATTACH_DATA_BIN** должно быть пустым, а система обмена сообщениями никогда не разрешает ссылку вложения. Используйте это значение, если хотите отправить ссылку, но не данные. 
  
Когда объект OLE находится в формате OLE 2,0 **IStorage** , доступ к данным осуществляется с помощью **PR_ATTACH_DATA_OBJ**. Когда объект OLE представлен в формате OLE 1,0 **олестреам** , доступ к данным предоставляется через **PR_ATTACH_DATA_BIN** в виде **IStream**. Тип OLE-кодировки можно определить с помощью значения **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Дополнительные сведения о интерфейсах и форматах OLE приведены в *справочнике по OLE для программистов* . 
  
## <a name="remarks"></a>Примечания

Если **PR_ATTACH_METHOD** **ATTACH_BY_WEBREFERENCE**, содержимое вложения отсутствует в сообщении. Вместо этого свойство **PR_ATTACH_LONG_FILENAME** содержит абсолютный URL-адрес содержимого вложений, которое хранится в сети. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

