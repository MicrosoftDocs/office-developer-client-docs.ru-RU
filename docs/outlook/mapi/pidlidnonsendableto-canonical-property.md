---
title: Каноническое свойство PidLidNonSendableTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableTo
api_type:
- COM
ms.assetid: 90e14969-652b-422a-9b0a-ee99e58bc8d5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cc510cb9a4a79f977cb6c9721921833441df23c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345520"
---
# <a name="pidlidnonsendableto-canonical-property"></a>Каноническое свойство PidLidNonSendableTo

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список всех неисходимых участников, которые также являются требуемыми участниками.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidNonSendableTo  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008536  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Собрания  <br/> |
   
## <a name="remarks"></a>Примечания

Значением для каждого участника является **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)адресной книги участника. Разделимые записи должны разделяться за осью с заосью, за которой следует пробел. Это свойство не требуется.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

