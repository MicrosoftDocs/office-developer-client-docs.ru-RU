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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393091"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Каноническое свойство PidLidAddressBookProviderArrayType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает состояние контакта электронных адресов и представляет набор битовых флагов.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidABPArrayType  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008029  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Замечания

Значение свойства **dispidABPArrayType** должно быть сочетание флаги, определяющие состояние объекта контакта. В следующей таблице указаны отдельные флаги. Если задано это свойство, свойство **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) необходимо установить, а также. Эти два свойства должны быть синхронизируется друг с другом. К примеру Если **dispidABPArrayType** разрядная «0x00000001 set», одно из значений **dispidABPEmailList** значения «0x00000000». 
  
|**Бит**|**Описание**|
|:-----|:-----|
|0x00000001  <br/> |Email1 определяется для этого контакта.  <br/> |
|0x00000002  <br/> |Почта2: определяется для этого контакта.  <br/> |
|0x00000004  <br/> |Почта3: определяется для этого контакта.  <br/> |
|0x00000008  <br/> |Рабочий факс определяется для этого контакта.  <br/> |
|0x00000010  <br/> |Домашняя страница факса определяется для этого контакта.  <br/> |
|0x00000020  <br/> |Основной факс определяется для этого контакта.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

