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
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348484"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Каноническое свойство PidLidAddressBookProviderEmailList

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, какие свойства электронных адресов заданы для контакта. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidABPEmailList  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008028  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Каждое PT_LONG этого свойства должно быть уникальным в свойстве и должно иметь одно из значений в следующей таблице. Если за установлено это свойство, необходимо также установить свойство **dispidABPArrayType** ([PidLidAddressBookProviderArrayType).](pidlidaddressbookproviderarraytype-canonical-property.md) Эти два свойства должны синхронизироваться друг с другом. Например, если одно из значений **в dispidABPEmailList** — "0x00000000", то **dispidABPArrayType** должен иметь бит "0x00000001". 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Для контакта определена электронная почта 1.  <br/> |
|0x00000001  <br/> |Для контакта определена электронная почта 2.  <br/> |
|0x00000002  <br/> |Для контакта определена электронная почта 3.  <br/> |
|0x00000003  <br/> |Для контакта определена деловая факсимиловая связь.  <br/> |
|0x00000004  <br/> |Для контакта определена домашняя факсимиловая связь.  <br/> |
|0x00000005  <br/> |Основной факс определяется для контакта.  <br/> |
   
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

