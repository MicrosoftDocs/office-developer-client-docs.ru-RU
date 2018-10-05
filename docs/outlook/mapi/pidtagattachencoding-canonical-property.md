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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382773"
---
# <a name="pidtagattachencoding-canonical-property"></a>Каноническое свойство PidTagAttachEncoding

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор объекта ASN.1, который задает кодирование для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Идентификатор:  <br/> |0x3702  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет алгоритм, используемый для преобразования данных в вложения.
  
 **Примечание** Не следует путать **PR_ATTACH_ENCODING** и свойства **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)). Они не пару и связанные с. **PR_ATTACH_TAG** — определяет приложения, изначально создавшего вложение. «Объект» имеет гораздо более общие значение в идентификатор объекта терминов и в X.400, чем в объектно ориентированного программирования. 
  
Идентификаторы объектов синтаксис и образец идентификатор объекта определены в MAPIOID. Файл заголовка. Значения для **PR_ATTACH_ENCODING** не только, определенных в MAPIOID. З. Например вложенные файлы Macintosh можно использовать идентификатор, такие как файлы. 
  
Полные сведения о идентификаторы объектов обратитесь к документации по ASN.1, X.208 и X.209. Идентификатор объекта находится в элементе ссылка приложения среды FTBP (файл перенос текста часть). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

