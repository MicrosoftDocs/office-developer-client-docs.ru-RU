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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, как создавать и перекомпомировать значение свойства **dispidFileUnder** ([PidLidFileUnder)](pidlidfileunder-canonical-property.md)при изменении других свойств имени контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidFileUnderId  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008006  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство отсутствует или имеет значение, не подробное в приведенной ниже таблице или [[MS-OXOCNTC],](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)приложение может выбрать собственную логику, чтобы отменить значение **dispidFileUnder** по мере изменения других свойств имени контакта. 
  
В следующей таблице используется нотация для указания <PropertyName> значения PropertyName. Например, если свойство **PR_SURNAME** ([PidTagSurname)](pidtagsurname-canonical-property.md)имеет значение "Smith", а значение свойства **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) — "Ben", то " указывает строку <PidTagGivenName> <PidTagSurname> "Ben Smith". В таблице "\r" указывает символ возврата каретки, "\n" указывает символ канала строки и представляет <space> пробел.
  
|**Значение свойства **dispidFileUnderId****|**Описание свойства **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |Пустое PT_UNICODE.  <br/> |
|0x00003001  <br/> |" \< PidTagDisplayName \> "  <br/> |
|0x00003A06  <br/> |" \< PidTagGivenName \> "  <br/> |
|0x00003A11  <br/> |" \< PidTagSurname \> "  <br/> |
|0x00003A16  <br/> |" \< PidTagCompanyName \> "  <br/> |
|0x00008017  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008018  <br/> |" \< PidTagCompanyName \> \r\n \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008019  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> \r\n \< PidTagCompanyName \> "  <br/> |
|0x00008030  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName" \>  <br/> |
|0x00008031  <br/> |" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008032  <br/> |" \< PidTagCompanyName \> \r\n \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName" \>  <br/> |
|0x00008033  <br/> |" \< PidTagCompanyName \> \r\n \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName" \>  <br/> |
|0x00008034  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \r\n \< PidTagCompanyName" \>  <br/> |
|0x00008035  <br/> |" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \r\n \< PidTagCompanyName \> "  <br/> |
|0x00008036  <br/> |" \< PidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName space \> \< \> \< PidTagGeneration" \>  <br/> |
|0x00008037  <br/> |" \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagSurname space \> \< \> \< PidTagGeneration" \>  <br/> |
|0x00008038  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagGeneration" \>  <br/> |
|0xfffffffd  <br/> |Указывает, что при отображении контакта приложение должно попытаться использовать текущее значение **dispidFileUnder** и другие свойства контакта, чтобы найти "наилучшее соответствие" **для dispidFileUnderId** одному из предыдущих значений в этой таблице.  <br/> |
|0xfffffffe  <br/> |Указывает, что при отображении контакта приложение должно выбрать соответствующие значения по умолчанию (в соответствии с языковым стандартом) **для dispidFileUnderId** и обновить **dispidFileUnder** в соответствии с выбором.  <br/> |
|0xffffffff  <br/> |**dispidFileUnder** предоставляется пользователем PT_UNICODE и не должен быть изменен при смене другого свойства имени контакта.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

