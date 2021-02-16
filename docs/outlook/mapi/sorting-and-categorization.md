---
title: Сортировка и классификация
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418486"
---
# <a name="sorting-and-categorization"></a>Сортировка и классификация

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сортировка таблицы помещает строки в порядке, который имеет смысл для ее просмотра. Например, один просматривает таблицу содержимого папки, отсортировать ее по теме сообщения, чтобы все цепочки беседы были вместе, а другому — отсортировать сообщения по имени отправитель. Вновь созданная таблица не обязательно сортируется в определенном порядке. 
  
Существует два типа сортировки:
  
- Стандартная сортировка
    
- Сортировка по категориям 
    
При стандартной сортировке все строки отображаются в плоском списке, используя один или несколько столбцов в качестве ключа сортировки. При сортировке по категориям строки отображаются иерархически с одним или более столбцов в качестве ключа сортировки. В каждой категории есть специальная строка заголовков, которая содержит следующие столбцы.
  
- Столбец или столбцы, которые составляют ключ сортировки
    
- **PR_CONTENT_COUNT** ([PidTagContentCount)](pidtagcontentcount-canonical-property.md)
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount)](pidtagcontentunreadcount-canonical-property.md)
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)
    
- **PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)
    
- **PR_ROW_TYPE** ([PidTagRowType)](pidtagrowtype-canonical-property.md) 
    
Под строкой заголовка имеются все строки из таблицы, содержащие столбцы со значениями, которые соответствуют ключу сортировки. Эти строки называются листовой строкой. Листовая строка содержит все столбцы в наборе столбцов без столбцов ключа сортировки. 
  
Таблицы содержимого папок часто поддерживают сортировку по категориям в дополнение к стандартной сортировке. Таблицы содержимого контейнеров адресной книги обычно поддерживают только стандартную сортировку. 
  
Категория может иметь два состояния: свернутые и расширенные. Если категория находится в свернутом состоянии, из [IMAPITable::QueryRows](imapitable-queryrows.md)возвращается только строка заголовка. Когда категория находится в расширенном состоянии, возвращаются все строки, связанные с этой категорией. Это относится к строкам заголовков и листовым строкам. 
  
Каждую категорию в представлении таблицы можно развернуть или свернуть независимо. То есть не все категории должны быть одновременно в одном состоянии; некоторые категории можно свернуть, а другие — развернуть. 
  
Пользователь классизированной таблицы решает, как она отображается. Один из распространенных вариантов — использовать в SDK Windows управление под названием treeview. Элементы управления Treeview — это списки, которые поддерживают информацию в древостройной структуре. Строки заголовков для категорий в расширенном состоянии помечаются знаком "минус", а строки заголовков для категорий в свернутом состоянии помечены знаком "плюс". Расширенные категории отображаются с отступами строк листов под строками заголовков. 
  
Чтобы свернуть и развернуть категорию, клиентскому приложению или поставщику услуг используются следующие методы [IMAPITable: IUnknown:](imapitableiunknown.md) 
  
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

