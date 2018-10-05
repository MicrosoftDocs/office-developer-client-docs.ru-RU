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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390928"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Каноническое свойство PidTagAttachDataBinary

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит двоичные вложения данные обычно через интерфейс объекта связывания и внедрения (OLE) **IStream** . 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Идентификатор:  <br/> |0x3701  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит вложения, если значение свойства **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) ATTACH_BY_VALUE, метод обычного вложения, и только один, которые должны поддерживаться. Если значение **PR_ATTACH_METHOD** ATTACH_OLE **PR_ATTACH_DATA_BIN** также содержит вложения OLE 1.0 **OLESTREAM** . 
  
 **OLESTREAM** вложения могут быть скопированы в файл путем вызова метода OLE **IStream::CopyTo** . Тип кодировки OLE можно определить по свойству **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). 
  
Для вложения файла документа OLE поставщика хранилища сообщений, необходимо ответить на звонок [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) и при необходимости может ответить на звонок на **PR_ATTACH_DATA_BIN **. Обратите внимание, что **PR_ATTACH_DATA_BIN** и **PR_ATTACH_DATA_OBJ** совместно использовать один и тот же идентификатор свойства и таким образом, два представления одного свойства. 
  
Для объекта хранилища например составные файл в формате документа OLE 2.0, некоторых поставщиков услуг позволяет открыть с помощью интерфейса MAPI **IStreamDocfile** для повышения производительности. Поставщик, который поддерживает **IStreamDocfile** должен предоставлять на **PR_ATTACH_DATA_OBJ** и может при необходимости привести на **PR_ATTACH_DATA_BIN**. 
  
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

