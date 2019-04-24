---
title: Каноническое свойство PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355708"
---
# <a name="pidlidfileunderid-canonical-property"></a>Каноническое свойство PidLidFileUnderId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, как создать и повторно вычислить значение свойства **диспидфилеундер** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) при изменении других свойств имени контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидфилеундерид  <br/> |
|Набор свойств:  <br/> |Псетид_аддресс  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008006  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство отсутствует или для него задано значение, не подробное в таблице ниже или в [[MS-оксокнтк]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), приложение может выбрать собственную логику для повторного вычисления значения **диспидфилеундер** в качестве другого свойства имени контакта. 
  
В следующей таблице приведена нотация <PropertyName> , в которой указывается значение PropertyName. Например, если значение свойства **пр_сурнаме** ([PidTagSurname](pidtagsurname-canonical-property.md)) — "Smith", а значение свойства **пр_гивен_наме** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) — "Бен", то "<PidTagGivenName> <PidTagSurname>" указывает строку "Бен Smith". В таблице "\r" указывает символ возврата каретки, "\n" определяет символ перевода строки и <space> представляет символ пробела.
  
|**Значение свойства **диспидфилеундерид****|**Описание свойства **диспидфилеундер****|
|:-----|:-----|
|0x00000000  <br/> |Пустой ПТ_УНИКОДЕ.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\>Space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<\>PidTagGivenName\<Space\>PidTagMiddleName\>"\<  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>PidTagMiddleName\>"\<\>\<  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>PidTagMiddleName\>"\<\>\<  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>Space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<Space\>\<\>PidTagGivenName Space\>PidTagMiddleName \r\n PidTagCompanyName"\<\>\<\>\<  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<Space\>\>\>PidTagGivenName\>Space PidTagMiddleName\>Space\>PidTagGeneration\<"\<\<\<\<  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<Space\>\>\>PidTagMiddleName\>Space PidTagSurname\>Space\>PidTagGeneration\<"\<\<\<\<  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>Space\>PidTagMiddleName\>Space\>PidTagGeneration"\<\<\<\<  <br/> |
|0xfffffffd  <br/> |Указывает, что при отображении контакта приложение должно попытаться использовать текущее значение **диспидфилеундер** и другие свойства контакта, чтобы найти "наилучшее значение" для **диспидфилеундерид** к одному из предыдущих значений в этой таблице.  <br/> |
|0xFFFFFFFE  <br/> |Указывает, что при отображении контакта приложение должно выбрать соответствующие значения по умолчанию (в соответствии с языковым стандартом языка) для **диспидфилеундерид** и обновить **диспидфилеундер** в соответствии с выбором.  <br/> |
|равен  <br/> |**диспидфилеундер** — это предоставленный пользователем пт_уникоде, и его не следует изменять при изменении другого свойства имени контакта.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

