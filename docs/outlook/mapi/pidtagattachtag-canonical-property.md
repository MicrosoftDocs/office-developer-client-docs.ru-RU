---
title: Каноническое свойство PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5a908b3543dff5cf011c9bd4d5d05b3a07004ead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361084"
---
# <a name="pidtagattachtag-canonical-property"></a>Каноническое свойство PidTagAttachTag

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор объекта ASN.1, определяющий приложение, которое предоставило вложение. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_TAG  <br/> |
|Идентификатор:  <br/> |0x370A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство определяет приложение, которое изначально вызвало вложение.
  
 **Примечание** Свойства **PR_ATTACH_ENCODING** ([PidTagAttachEncoding)](pidtagattachencoding-canonical-property.md) **и** PR_ATTACH_TAG не следует путать. Они не связаны и не связаны. **PR_ATTACH_ENCODING** определяет алгоритм, используемый для преобразования данных во вложении. "Object" имеет гораздо более общее значение в идентификаторе объекта термина и в использовании X.400, чем в объектно-ориентированном программировании. 
  
Синтаксис идентификатора объекта и образцы идентификаторов объектов определены в MAPIOID. Файл h-загона. Значения **для** PR_ATTACH_TAG не ограничиваются значениями, определенными в MAPIOID.H. 
  
Полные сведения об этих идентификаторах объектов см. в документации по ASN.1, X.208 и X.209. Идентификатор объекта находится в элементе application-reference среды FTBP. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

