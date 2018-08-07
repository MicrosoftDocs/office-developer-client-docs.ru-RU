---
title: Каноническое свойство PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4dde93bbec2594804ab18a3ee4eb3e116a57e528
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811291"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Каноническое свойство PidTagJunkIncludeContacts

  
  
**Относится к**: Outlook 
  
Указывает, рассматриваются ли адреса электронной почты из контактов в папке контактов специально по отношению к фильтра нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Идентификатор:  <br/> |0x6100  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Нежелательной почты  <br/> |
   
## <a name="remarks"></a>Замечания

Если задано значение «0x00000001», эти адреса электронной почты необходимо заполнить части адреса электронной почты для связи «надежные» ограничении правило нежелательной электронной почты таким образом, чтобы сообщения от этих адресов обрабатывается как «не является нежелательным». Если задано значение «0x00000000», адреса электронной почты из папки "Контакты" не добавляются в правило нежелательной электронной почты, а раздел правило должно быть значение NULL.
  
Если это свойство со значением «0x00000001» и, если добавлены контакт имеет адреса электронной почты, которые еще не включены в разделе надежные контакты правило нежелательной электронной почты, нужные адреса электронной почты необходимо добавить ограничения. Если это свойство является «0x00000000», никаких действий не требуется.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
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

