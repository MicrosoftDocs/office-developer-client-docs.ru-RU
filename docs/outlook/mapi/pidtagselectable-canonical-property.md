---
title: Каноническое свойство PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d376a5219125866f467be01709a6a611ed8d47f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576423"
---
# <a name="pidtagselectable-canonical-property"></a>Каноническое свойство PidTagSelectable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если запись в таблице одноразовых можно выбирать. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SELECTABLE  <br/> |
|Идентификатор:  <br/> |0x3609  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Контейнер адресной книги  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется в основном для визуального форматирования одноразовых таблицы. Шаблоны могут быть сгруппированы, создав запись, указывающую заголовка для группы. Назначить этому свойству значение FALSE для заголовка гарантирует, что пользователь может выбрать только фактическая шаблонов в группе, а не в этой записи заголовка. 
  
Это свойство применяется только к одноразовых таблицы, не для таблицы иерархии адресной книги. 
  
MAPI позволяет поставщика адресных книг для группировки визуально с двумя способами. Во-первых определенные строки могут работать в качестве заголовков, не упустив ни одного. Во-вторых доступно для выбора элементов можно отступ относительно их заголовки с помощью свойства **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)). Это свойство используется в таких группировки для указания ли этот элемент можно выбрать из списка для создания указывает адрес. Например если клиент имеет несколько шаблонов для создания адресов факсов, его можно они отображаются следующим образом: 
  
Шаблоны ФАКСОВ (глубина 0, не выбирается)
  
 Локальный (глубина 1, доступно для выбора) 
  
 Звонок из США (глубина 1, доступно для выбора) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для шаблонов адресной книги.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Каноническое свойство PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

