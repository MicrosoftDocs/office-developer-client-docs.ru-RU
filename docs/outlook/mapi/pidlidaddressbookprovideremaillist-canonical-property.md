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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, какие свойства электронных адресов для контакта задаются. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидабпемаиллист  <br/> |
|Набор свойств:  <br/> |Псетид_аддресс  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008028  <br/> |
|Тип данных:  <br/> |ПТ_МВ_ЛОНГ  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Каждое значение ПТ_ЛОНГ в этом свойстве должно быть уникальным в свойстве и должно быть равно одному из значений в следующей таблице. Если это свойство задано, также должно быть задано свойство **диспидабпаррайтипе** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)). Эти два свойства должны поддерживать синхронизацию друг с другом. Например, если одно из значений в **диспидабпемаиллист** имеет значение "0x00000000", то **диспидабпаррайтипе** должен иметь бит "0x00000001". 
  
|**Value**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Для контакта определено значение Email1.  <br/> |
|0x00000001  <br/> |Для контакта определено значение Email2.  <br/> |
|0x00000002  <br/> |Для контакта определено значение Email3.  <br/> |
|0x00000003  <br/> |Для контакта определен рабочий Факс.  <br/> |
|0x00000004  <br/> |Для контакта определен домашний Факс.  <br/> |
|0x00000005  <br/> |Для контакта определен основной Факс.  <br/> |
   
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

