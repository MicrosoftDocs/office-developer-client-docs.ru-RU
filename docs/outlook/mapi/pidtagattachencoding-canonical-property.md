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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор объекта ASN.1, который указывает кодиление для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_ENCODING  <br/> |
|Идентификатор:  <br/> |0x3702  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство определяет алгоритм, используемый для преобразования данных в приложении.
  
 **Примечание** Свойства **PR_ATTACH_ENCODING** и **PR_ATTACH_TAG** [(PidTagAttachTag)](pidtagattachtag-canonical-property.md)не следует путать. Они не являются сопряженными или связанными. **PR_ATTACH_TAG** определяет приложение, изначально сгенерированное вложение. "Объект" имеет гораздо более общее значение в идентификаторе объекта терминов и в X.400, чем в объектно-ориентированном программировании. 
  
Синтаксис идентификатора объекта и идентификаторы образцов объектов определяются в MAPIOID. Файл заглавной папки H. Значения для **PR_ATTACH_ENCODING** не ограничиваются значениями, определенными в MAPIOID.H. Например, присоединенные файлы Macintosh могут использовать идентификатор, например MacBinary. 
  
Полные сведения об этих идентификаторах объектов см. в документации по ASN.1, X.208 и X.209. Идентификатор объекта находится в элементе приложения-ссылки среды FTBP (Часть тела передачи файлов). 
  
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



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

