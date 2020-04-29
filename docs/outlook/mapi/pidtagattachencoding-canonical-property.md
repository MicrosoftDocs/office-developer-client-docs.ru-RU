---
title: Каноническое свойство PidTagAttachEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachEncoding
api_type:
- HeaderDef
ms.assetid: 3b30cec6-da1e-4ef1-8c17-24b66f31cf0a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4bda4783012a3a5cd50d9c0aea6a37ccd238b660
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345495"
---
# <a name="pidtagattachencoding-canonical-property"></a>Каноническое свойство PidTagAttachEncoding

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор объекта ASN. 1, указывающий кодировку для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Идентификатор:  <br/> |0x3702  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство определяет алгоритм, используемый для преобразования данных во вложении.
  
 **Note (Примечание** ) Свойства **PR_ATTACH_ENCODING** и **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) не следует путать. Они не являются связанными или связанными. **PR_ATTACH_TAG** определяет приложение, которое изначально создало вложение. "Объект" имеет гораздо больше общего смысла в идентификаторе объекта Term и в X. 400, чем в объектно ориентированном программировании. 
  
Синтаксис идентификатора объекта и примеры идентификаторов объектов определяются в МАПИОИД. H файл заголовка. Значения **PR_ATTACH_ENCODING** не ограничиваются теми, что заданы в мапиоид. Высоты. Например, прикрепленные файлы Macintosh могут использовать идентификатор, например Макбинари. 
  
Для получения полных сведений об этих идентификаторах объектов, ознакомьтесь с документацией по ASN. 1, X. 208 и X. 209. Идентификатор объекта находится в элементе ссылки на приложение в среде ФТБП (часть текста для передачи файлов). 
  
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



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

