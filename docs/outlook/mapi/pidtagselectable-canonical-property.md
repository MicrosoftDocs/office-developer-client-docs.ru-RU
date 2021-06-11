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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит TRUE, если можно выбрать запись в разовой таблице. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SELECTABLE  <br/> |
|Идентификатор:  <br/> |0x3609  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Контейнер адресной книги  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется в основном для визуального форматирования разовой таблицы. Шаблоны можно сгруппить, создав запись, которая указывает заголовок для группы. Настройка этого свойства false для заголовка гарантирует, что пользователь может выбрать только фактические шаблоны в группе, а не эту запись заголовка. 
  
Это свойство применяется только к разовой таблице, а не к таблице иерархии адресных книг. 
  
MAPI позволяет поставщику адресных книг визуально группировать элементы двумя средствами. Во-первых, некоторые строки могут функционировать в качестве заголовков, будучи неизбираемыми. Во-вторых, выбранные элементы могут быть отступлены по отношению к их заголовкам с помощью **свойства PR_DEPTH** [(PidTagDepth).](pidtagdepth-canonical-property.md) Это свойство используется в такой группировке, чтобы указать, можно ли выбрать этот элемент из списка для создания разового адреса. Например, если клиент имеет несколько шаблонов для создания факсимили, он может отображать их следующим образом: 
  
Шаблоны ФАКС (глубина 0, не выбрана)
  
 Локальный (глубина 1, выбор) 
  
 Междугородние (глубина 1, выборка) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для шаблонов адресной книги.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Каноническое свойство PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

