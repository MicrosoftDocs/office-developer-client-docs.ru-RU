---
title: Каноническое свойство PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810111"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Каноническое свойство PidLidAddressBookProviderEmailList

  
  
**Относится к**: Outlook 
  
Указывает, какие свойства электронный адрес, заданные для контакта. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidABPEmailList  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008028  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Каждое значение PT_LONG в это свойство должно быть уникальным в свойстве и должна соответствовать одному из значений в таблице ниже. Если задано это свойство, необходимо также установить свойство **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)). Эти два свойства должны быть синхронизируется друг с другом. Например если выполняется одно из значений в **dispidABPEmailList** «0x00000000», а затем **dispidABPArrayType** необходимо разрядная «0x00000001» установить. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Email1 определяется для этого контакта.  <br/> |
|0x00000001  <br/> |Почта2: определяется для этого контакта.  <br/> |
|0x00000002  <br/> |Почта3: определяется для этого контакта.  <br/> |
|0x00000003  <br/> |Рабочий факс определяется для этого контакта.  <br/> |
|0x00000004  <br/> |Домашняя страница факса определяется для этого контакта.  <br/> |
|0x00000005  <br/> |Основной факс определяется для этого контакта.  <br/> |
   
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

