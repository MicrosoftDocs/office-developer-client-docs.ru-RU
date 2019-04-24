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
  
Содержит значение TRUE, если можно выбрать запись в таблице "одноразовый". 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕЛЕКТАБЛЕ  <br/> |
|Идентификатор:  <br/> |0x3609  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Контейнер адресной книги  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется в основном для визуального форматирования одноразовой таблицы. Шаблоны можно группировать, создавая запись, которая указывает заголовок для группы. Если задать для этого свойства значение FALSE для заголовка, пользователь сможет выбрать только шаблоны в группе, а не запись заголовка. 
  
Это свойство применяется только к одноразовой таблице, а не к таблице иерархий адресной книги. 
  
MAPI позволяет поставщику адресных книг группировать элементы в визуальном виде с двумя способами. Во – первых, определенные строки могут работать в качестве заголовков, не выделять их. Во-вторых, доступные для выбора элементы могут относиться к своим заголовкам с помощью свойства **пр_депс** ([PidTagDepth](pidtagdepth-canonical-property.md)). Это свойство используется в такой группе, чтобы указать, можно ли выбрать этот элемент из списка для создания одноразового адреса. Например, если у клиента есть несколько шаблонов для создания адресов факса, они могут отображаться следующим образом: 
  
Шаблоны факсов (глубина 0, Невыбираемая)
  
 Local (глубина 1, выбираемая) 
  
 Междугородный (глубина 1, выбираемая) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОАБКТ]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для шаблонов адресных книг.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)
  
[Каноническое свойство PidTagFolderType](pidtagfoldertype-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

