---
title: attConversationID и attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Последнее изменение: 12 марта 2013 г.'
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582716"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID и attParentID

**Область применения**: Outlook 2013 | Outlook 2016 
  
Windows для рабочих групп 3.1 почты беседы ключ — это строка текста. Эквивалент MAPI — это двоичное значение. Для обеспечения обратной совместимости, реализация TNEF преобразует двоичные данные в текст и добавляет конечный символ null.
  
> [!NOTE]
> Соответствующих свойств в MAPI для которой сопоставляются эти атрибуты TNEF, PR_CONVERSATION_KEY и PR_PARENT_KEY, являются устаревшими в Microsoft Exchange Server: использование **PR_CONVERSATION_KEY**, [PidTagConversationKey каноническое Свойство](pidtagconversationkey-canonical-property.md), сохраняется в Outlook, только для обнаружения **IPM. MessageManager** сообщения. 
  
## <a name="remarks"></a>Замечания

В противном случае — устаревший перед **PR_CONVERSATION_INDEX**, [Свойство каноническое PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic каноническое является ли данное свойство **PR_CONVERSATION_KEY** Свойство](pidtagconversationtopic-canonical-property.md), который следует использовать.
  
## <a name="see-also"></a>См. также

- [Поддерева IPM](ipm-subtree.md)
- [����������� ����� MAPI](mapi-special-folders.md)

