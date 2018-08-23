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
ms.openlocfilehash: 12668cb87f21b56cd398a7b5375f6a4b40c65829
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581533"
---
# <a name="sorting-and-categorization"></a>Сортировка и классификация

 
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сортировка таблицы помещает строк в порядке, который имеет смысл для его просмотра. Например одно средство просмотра может выбрать для отображения в таблице содержимое папки, упорядоченные по теме сообщения, чтобы все потоки беседы вместе, в то время как другой средство просмотра может оказаться сообщения, отсортированные по имени отправителя. Вновь созданный экземпляр таблицы не обязательно отсортированы в любом порядке. 
  
Существует два типа сортировки.
  
- Стандартный сортировки
    
- Сортировка по категориям 
    
С помощью стандартных сортировка все строки, отображаются в плоский список, используя один или несколько столбцов в качестве ключа сортировки. С сортировкой по категориям, строки отображаются иерархически с одной или нескольких столбцах как ключ сортировки. В рамках каждой категории имеется строка специальные заголовка, который содержит следующие столбцы.
  
- Столбец или столбцы, которые составляют ключ сортировки
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))
    
- **PR_ROW_TYPE** ([PidTagRowType](pidtagrowtype-canonical-property.md)) 
    
С отступом под строкой заголовка — это все строки из таблицы, содержащие столбцы с помощью значения, которые соответствуют ключ сортировки. Эти строки вызываются конечные строки. Конечные строки содержит все столбцы в столбце значение минус столбцы. 
  
В таблицах содержимое папок, которые часто поддерживает Сортировка по категориям Помимо стандартных сортировки. В таблицах содержимое из адресной книги контейнеров обычно поддерживает только стандартных сортировка. 
  
Категория имеет два состояния: свертывать и развертывать. Когда категории в свернутом состоянии, [IMAPITable::QueryRows](imapitable-queryrows.md)возвращается только строку заголовков. Когда категории в развернутом состоянии, возвращаются все строки, относящиеся к категории. Этот компонент включает строку заголовка и конечные строки. 
  
Каждой категории в представлении таблицы можно разворачивать и сворачивать независимо друг от друга. То есть не все категории необходимо в том состоянии в то же время; Некоторые категории можно свернуть в то время как другие пользователи развертываются. 
  
Пользователь форматирование таблицы решает, как оно отображается. Один общий параметр — с помощью элемента управления, предоставляемого в пакете SDK Windows, элемент управления treeview. Элементы управления TreeView, списков, сведения о поддержке в древовидной структуре. Заголовок строки для категорий в развернутом состоянии помечены со знаком минус во время строки заголовка для категорий в свернутом состоянии помечаются знак плюс. Расширенное категории отображаются с отступом строки заголовка конечные строки. 
  
Чтобы свернуть и разверните категорию, клиентское приложение или поставщик услуг использует следующие [IMAPITable: IUnknown](imapitableiunknown.md) методов: 
  
- [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md)
    
- [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [IMAPITable::CollapseRow](imapitable-collapserow.md)
    
Дополнительные сведения о сортировке потоков беседы в следующих разделах:
  
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

