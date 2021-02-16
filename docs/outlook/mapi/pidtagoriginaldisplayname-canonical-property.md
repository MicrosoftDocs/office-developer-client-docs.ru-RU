---
title: Каноническое свойство PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355610"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a>Каноническое свойство PidTagOriginalDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит исходное отображаемое имя записи, скопированной из адресной книги в личную адресную книгу или другую доступную для записи адресную книгу.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3A13  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства содержат сведения об исходном источнике скопированной записи.
  
В непрочитанном отчете эти свойства содержат копию отображаемого имени исходного получателя сообщения, для которого создается отчет. Если исходный получатель входит в список рассылки, отображаемая имя списка рассылки сохраняется в отчете.
  
Клиентские приложения могут использовать эти свойства для предотвращения изменения или "спуфинга" записей, предоставляя неиспользоваемую копию отображаемого имени для сравнения.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

