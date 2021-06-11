---
title: Каноническое свойство PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348442"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Каноническое свойство PidLidAddressBookProviderArrayType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние электронных адресов контакта и представляет набор битных флагов.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidABPArrayType  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008029  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

Значение свойства **dispidABPArrayType** должно быть сочетанием флагов, которые указывают состояние контактного объекта. Отдельные флаги указаны в следующей таблице. Если это свойство заданной, необходимо также задать свойство **dispidABPEmailList** [(PidLidAddressBookProviderEmailList).](pidlidaddressbookprovideremaillist-canonical-property.md) Эти два свойства должны синхронизироваться друг с другом. Например, если **dispidABPArrayType** имеет бит "0x00000001 набор", одно из значений **dispidABPEmailList** должно быть "0x00000000". 
  
|**Bit**|**Описание**|
|:-----|:-----|
|0x00000001  <br/> |Email1 определяется для контакта.  <br/> |
|0x00000002  <br/> |Email2 определяется для контакта.  <br/> |
|0x00000004  <br/> |Email3 определяется для контакта.  <br/> |
|0x00000008  <br/> |Для контакта определяется бизнес-факс.  <br/> |
|0x00000010  <br/> |Для контакта определяется домашний факс.  <br/> |
|0x00000020  <br/> |Для контакта определяется первичный факс.  <br/> |
   
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

