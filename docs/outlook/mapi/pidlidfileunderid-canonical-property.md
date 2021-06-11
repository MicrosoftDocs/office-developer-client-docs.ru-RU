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
  
Указывает, как создавать и перекомплектовывать значение свойства[dispidFileUnder (PidLidFileUnder)](pidlidfileunder-canonical-property.md)при изменении других свойств имен контактов. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidFileUnderId  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008006  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство отсутствует или задавалось значение, не описанное в таблице ниже или [в [MS-OXOCNTC],](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)приложение может выбрать свою собственную логику, чтобы изменить значение **dispidFileUnder** по мере изменения других свойств имен контактов. 
  
В следующей таблице нотация используется для указания <PropertyName> "значение PropertyName". Например, если значение свойства **PR_SURNAME** [(PidTagSurname)](pidtagsurname-canonical-property.md)— "Smith", а значение свойства **PR_GIVEN_NAME** [(PidTagGivenName)](pidtaggivenname-canonical-property.md)— "Ben", то "" указывает строку <PidTagGivenName> <PidTagSurname> "Ben Smith". В таблице "\r" указывается символ возврата перевозки, "\n" указывает символ ленты строки и представляет <space> символ пространства.
  
|**Значение свойства **dispidFileUnderId****|**Описание свойства **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |Пустой PT_UNICODE.  <br/> |
|0x00003001  <br/> |" \< PidTagDisplayName \> "  <br/> |
|0x00003A06  <br/> |" \< PidTagGivenName \> "  <br/> |
|0x00003A11  <br/> |" \< PidTagSurname \> "  <br/> |
|0x00003A16  <br/> |" \< PidTagCompanyName \> "  <br/> |
|0x00008017  <br/> |" \< PidTagSurname \> , пространство \< \> \< PidTagGivenName пространство \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008018  <br/> |" \< PidTagCompanyName \>\r\n\< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008019  <br/> |" \< PidTagSurname \> , пространство \< \> \< PidTagGivenName пространство \> \< \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008030  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008031  <br/> |" \< Пространство PidTagSurname \> \< \> \< PidTagGivenName \> \< пространство \> \< PidTagMiddleName \> "  <br/> |
|0x00008032  <br/> |" \< PidTagCompanyName \>\r\n\< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008033  <br/> |" \< Пространство PidTagCompanyName \>\r\nПространства \< \> \< \> \< PidTagGivenName \> \< \> \< PidTagGivenName \> "  <br/> |
|0x00008034  <br/> |" \< Пространство PidTagSurname \> \< PidTagGivenName \> \< \> \< PidTagMiddleName \>\r\n\< PidTagCompanyName" \>  <br/> |
|0x00008035  <br/> |" \< Пространство PidTagSurname \> \< Пространство \> \< PidTagGivenName \> \< \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008036  <br/> |" \< Пространство PidTagSurname \> \< Пространство \> \< PidTagGivenName Пространство \> \< \> \< PidTagMiddleName пространство \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008037  <br/> |" \< Пространство PidTagGivenName \> \< Пространство \> \< PidTagMiddleName пространство \> \< \> \< PidTagSurname пространство \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008038  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagGeneration \> "  <br/> |
|0xfffffffd  <br/> |Указывает, что при отображении контакта приложение должно попытаться использовать текущее значение **dispidFileUnder** и других свойств контактов для поиска "наилучшего совпадения" для **dispidFileUnderId** с одним из предыдущих значений в этой таблице.  <br/> |
|0xfffffffe  <br/> |Указывает, что при отображении контакта приложение должно выбрать соответствующие значения по умолчанию (в соответствии с языковым языком) для **dispidFileUnderId** и обновить **dispidFileUnder,** чтобы соответствовать выбору.  <br/> |
|0xffffffff  <br/> |**dispidFileUnder** — это предоставляемая пользователем PT_UNICODE и не должна меняться при смене другого свойства имени контакта.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

