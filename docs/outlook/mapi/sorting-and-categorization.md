---
title: Сортировка и классификация
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Последнее изменение: 08 ноября 2011 г.'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418486"
---
# <a name="sorting-and-categorization"></a>Сортировка и классификация

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сортировка таблицы помещает строки в порядок, который имеет смысл для его зрителя. Например, один зритель может предпочесть видеть таблицу содержимого папки, отсортировали по теме сообщения, чтобы все потоки беседы были вместе, а другой зритель мог потребовать отсортировать сообщения по имени отправитель. Вновь созданная таблица не обязательно сортируется в любом конкретном порядке. 
  
Существует два типа сортировки:
  
- Стандартная сортировка
    
- Сортировка по категориям 
    
При стандартной сортировке все строки отображаются в плоском списке, используя один или несколько столбцов в качестве ключа сортировки. При сортировке категорий строки отображаются иерархически с одним или более столбцами в качестве ключа сортировки. В каждой категории имеется специальная строка заголовка, которая содержит следующие столбцы.
  
- Столбец или столбцы, которые составляют ключ сортировки
    
- **PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)
    
- **PR_CONTENT_UNREAD** [(PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)
    
- **PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)
    
- **PR_DEPTH** [(PidTagDepth)](pidtagdepth-canonical-property.md)
    
- **PR_ROW_TYPE** [(PidTagRowType)](pidtagrowtype-canonical-property.md) 
    
В строке заголовка находятся все строки из таблицы, содержащие столбцы со значениями, которые соответствуют ключу сортировки. Эти строки называются строками листа. Строки Leaf содержат все столбцы в наборе столбцов минус столбцы ключей сортировки. 
  
Таблицы содержимого папок часто поддерживают сортировку по категориям в дополнение к стандартной сортировке. Таблицы содержимого контейнеров адресной книги обычно поддерживают только стандартную сортировку. 
  
Категория может иметь два состояния: рухнувшего и расширенного. Если категория находится в состоянии коллапса, из [IMAPITable::QueryRows](imapitable-queryrows.md)возвращается только строка заголовка. Когда категория находится в расширенном состоянии, возвращаются все строки, связанные с этой категорией. Это включает строки заголовка и листовые строки. 
  
Каждая категория в представлении таблицы может быть расширена или разрушена самостоятельно. То есть не все категории должны быть в одном и том же состоянии одновременно; некоторые категории могут быть свернуты, а другие расширены. 
  
Пользователь классифицируются таблицы решает, как она отображается. Одним из распространенных вариантов является использование управления, предоставленного в Windows SDK, называемом управлением treeview. Элементы управления Treeview — это поля списков, которые поддерживают сведения в структуре, похожей на дерево. Строки заголовков для категорий в расширенном состоянии отмечены знаком минус, а строки заголовка для категорий в состоянии обрушения отмечены знаком плюс. Расширенные категории отображаются с отступными строками листа под строками заголовков. 
  
Чтобы свернуть и расширить категорию, клиентские приложения или поставщики услуг используют следующие методы [IMAPITable: IUnknown:](imapitableiunknown.md) 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Дополнительные сведения о сортировке потоков беседы см. в следующих темах:
  
- [SSortOrder](ssortorder.md)
    
- [Каноническое свойство PidTagSubject](pidtagsubject-canonical-property.md)
    
- [Каноническое свойство PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)
    
- [Каноническое свойство PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
    
- [Каноническое свойство PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)
    
- [Каноническое свойство PidTagConversationIndex](pidtagconversationindex-canonical-property.md)
    
- [ScCreateConversationIndex](sccreateconversationindex.md)
    
- [Сортировка таблиц после установки столбцов и ограничений](sorting-tables-after-setting-columns-and-restrictions.md)
    
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

