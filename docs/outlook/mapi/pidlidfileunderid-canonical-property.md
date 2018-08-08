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
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810367"
---
# <a name="pidlidfileunderid-canonical-property"></a>Каноническое свойство PidLidFileUnderId

  
  
**Относится к**: Outlook 
  
Указывает, как создать и подсчета значение свойства **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) при изменении свойства имени других контактов.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidFileUnderId  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008006  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Если это свойство отсутствует или задано значение не описано в следующей таблице или в [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), приложения можно выбрать собственную логику для подсчета значение **dispidFileUnder** как другие изменения свойств имя контакта. 
  
В следующей таблице, пометка <PropertyName> используется для указания «значение PropertyName». Например, если значение свойства **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) — «Егоров», а значение свойства **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) — «Бен», затем "<PidTagGivenName> <PidTagSurname>" указывает строку «Бен Егоров». В таблице «\r» указывает, возврат каретки, «\n» указывает символ перевода строки и <space> представляет пробел.
  
|**Значение свойства **dispidFileUnderId****|**Описание свойства **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |Пустой PT_UNICODE.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagGeneration\>"  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagSurname\>\<пространства\>\<PidTagGeneration\>"  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagGeneration\>"  <br/> |
|0xfffffffd  <br/> |Указывает, что при отображении контакт, приложение следует попытаться использовать текущее значение **dispidFileUnder** и другие свойства контакта для поиска «рекомендации» для **dispidFileUnderId** к одному из вышеуказанных значений в следующей таблице.  <br/> |
|0xFFFFFFFE  <br/> |Указывает, что при отображении контакт, приложения выберите соответствующие значения по умолчанию (в соответствии с языковой стандарт) для **dispidFileUnderId** и обновить **dispidFileUnder** в соответствии с выбором.  <br/> |
|0xFFFFFFFF  <br/> |**dispidFileUnder** — это PT_UNICODE предоставленного пользователем и не должно изменяться при изменении другого свойства имя контакта.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

