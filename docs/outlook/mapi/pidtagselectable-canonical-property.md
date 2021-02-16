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
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359019"
---
# <a name="pidtagselectable-canonical-property"></a>Каноническое свойство PidTagSelectable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит true, если можно выбрать запись в одностолбной таблице. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SELECTABLE  <br/> |
|Идентификатор:  <br/> |0x3609  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Контейнер адресной книги  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство в основном используется для визуального форматирования одностолбной таблицы. Шаблоны можно сгруппить, создав запись, которая указывает заголовок для группы. Установка для этого свойства false для заголовка гарантирует, что пользователь может выбрать только фактические шаблоны в группе, а не эту запись заголовка. 
  
Это свойство применяется только к одностолковой таблице, а не к таблице иерархии адресной книги. 
  
MAPI позволяет поставщику адресной книги визуально группировать элементы двумя способами. Во-первых, некоторые строки могут работать в качестве заголовков, не выбирая их. Во-вторых, элементы, которые можно выбрать, могут быть отступы относительно их заголовков с помощью свойства **PR_DEPTH** ([PidTagDepth).](pidtagdepth-canonical-property.md) Это свойство используется в такой группировке, чтобы указать, можно ли выбрать этот элемент из списка, чтобы создать разовой адрес. Например, если клиент имеет несколько шаблонов для создания факс-адресов, он может отображать их следующим образом: 
  
Шаблоны факсов (глубина 0, не выбирается)
  
 Локальный (глубина 1, можно выбрать) 
  
 Long-distance (depth 1, selectable) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для шаблонов адресных книг.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Каноническое свойство PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

