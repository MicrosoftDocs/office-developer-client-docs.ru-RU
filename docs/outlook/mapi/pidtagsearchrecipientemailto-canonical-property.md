---
title: Каноническое свойство PidTagSearchRecipientEmailTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358921"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>Каноническое свойство PidTagSearchRecipientEmailTo

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит строку Юникод, запрашиваемую в списке адресов электронной почты или отображает имена получателей, адресованных в строке **To** сообщений в магазине. 
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|Идентификатор:  <br/> |0x0EA6  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

> [!NOTE]
> Этот тег ограничения MAPI, используемый при поиске адресов электронной почты или отображаемых имен, на которые отправляется сообщение, может не быть определен в загружаемом файле загона, который у вас есть в настоящее время. Его можно добавить в код, используя следующее значение: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Microsoft Exchange Server протоколы.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Указывает свойства и операции для управления конфигурацией списка папки поиска.
    
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

