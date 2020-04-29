---
title: Сортировка и категоризация
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 853c48e4-ef5b-49da-b281-f72784c598ce
description: 'Дата последнего изменения: 08 ноября 2011 г.'
ms.openlocfilehash: 8a5a07cdeb7f000c9a7da24dbea1a42a6f9fc185
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418486"
---
# <a name="sorting-and-categorization"></a>Сортировка и категоризация

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сортировка таблицы помещает строки в порядке, который имеет смысл для его просмотра. Например, одно средство просмотра может предпочесть просмотр таблицы содержимого папки, отсортированной по теме сообщения, чтобы все цепочки беседы собрались, а другое средство просмотра могло бы отсортировать сообщения по имени отправителя. Только что созданная таблица не обязательно сортируется в определенном порядке. 
  
Существует два типа сортировки:
  
- Стандартная сортировка
    
- Сортировка по категориям 
    
При стандартной сортировке все строки отображаются в плоском списке с использованием одного или нескольких столбцов в качестве ключа сортировки. При сортировке по категориям строки отображаются в иерархическом порядке с одним или несколькими столбцами в качестве ключа сортировки. В каждой категории имеется специальная строка заголовков, содержащая следующие столбцы.
  
- Столбец или столбцы, составляющие ключ сортировки
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
Под строкой заголовков отображаются все строки таблицы, содержащие столбцы со значениями, соответствующими ключу сортировки. Эти строки называются конечными строками. Конечные строки содержат все столбцы в наборе столбцов за исключением столбцов ключа сортировки. 
  
Таблицы содержимого папок часто поддерживают сортировку по категориям в дополнение к стандартной сортировке. В таблицах содержимого контейнеров адресных книг обычно поддерживается только стандартная сортировка. 
  
Категория может иметь два состояния: свернуто и развернуто. Когда Категория находится в свернутом состоянии, возвращается только строка заголовка из [IMAPITable:: QueryRows](imapitable-queryrows.md). Если категория находится в развернутом состоянии, возвращаются все строки, связанные с категорией. Сюда входят строки заголовков и конечные строки. 
  
Каждая категория в представлении таблицы может быть развернута или свернута независимо друг от друга. То есть не все категории должны находиться в одном и том же состоянии одновременно; Некоторые категории могут быть свернуты, в то время как другие развернуты. 
  
Пользователь в таблице, классифицированной по категориям, определяет, как она отображается. Один из распространенных вариантов — использовать элемент управления, входящий в состав Windows SDK, который называется элементом управления TreeView. Элементы управления TreeView — это списки, которые поддерживают информацию в древовидной структуре. Строки заголовка для категорий в развернутом состоянии помечаются знаком минус, а строки заголовка для категорий в свернутом состоянии помечаются знаком "плюс". Расширенные категории отображаются с конечными строками, расположенными под строками заголовков. 
  
Чтобы свернуть и развернуть категорию, в клиентском приложении или поставщике услуг используются следующие методы [IMAPITable: IUnknown](imapitableiunknown.md) : 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Дополнительные сведения о сортировке обсуждений можно найти в следующих разделах:
  
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

