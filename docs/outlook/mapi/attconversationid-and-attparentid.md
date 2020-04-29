---
title: attConversationID и attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Дата последнего изменения: 12 марта 2013 г.'
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410051"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID и attParentID

**Относится к**: Outlook 2013 | Outlook 2016 
  
Ключ беседы Windows для рабочих групп 3,1 представляет собой текстовую строку. Эквивалент MAPI является двоичным значением. Для обеспечения обратной совместимости реализация формата TNEF преобразует двоичные данные в текст и добавляет завершающий символ null.
  
> [!NOTE]
> Соответствующие свойства MAPI, которым сопоставлены эти атрибуты TNEF, PR_CONVERSATION_KEY и PR_PARENT_KEY, не поддерживаются в Microsoft Exchange Server: использование **PR_CONVERSATION_KEY**, [каноническое свойство PidTagConversationKey](pidtagconversationkey-canonical-property.md), только в Outlook, для поиска **IPM. Сообщения Мессажеманажер** . 
  
## <a name="remarks"></a>Примечания

Свойство **PR_CONVERSATION_KEY** — это значение, не являющееся устаревшим прекурсор **PR_CONVERSATION_INDEX**, [каноническое свойство](pidtagconversationindex-canonical-property.md) и **PR_CONVERSATION_TOPIC**, [каноническое свойство PidTagConversationTopic](pidtagconversationtopic-canonical-property.md), которое следует использовать вместо этого.
  
## <a name="see-also"></a>См. также

- [Поддерево IPM](ipm-subtree.md)
- [Специальные папки MAPI](mapi-special-folders.md)

