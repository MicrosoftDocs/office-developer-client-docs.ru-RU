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
ms.openlocfilehash: 2fd3e66e3171c677465a533ede3001cd0b28c8aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808075"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID и attParentID

**Относится к**: Outlook 
  
Windows для рабочих групп 3.1 почты беседы ключ — это строка текста. Эквивалент MAPI — это двоичное значение. Для обеспечения обратной совместимости, реализация TNEF преобразует двоичные данные в текст и добавляет конечный символ null.
  
> [!NOTE]
> Соответствующих свойств в MAPI для которой сопоставляются эти атрибуты TNEF, PR_CONVERSATION_KEY и PR_PARENT_KEY, являются устаревшими в Microsoft Exchange Server: использование **PR_CONVERSATION_KEY**, [PidTagConversationKey каноническое Свойство](pidtagconversationkey-canonical-property.md), сохраняется в Outlook, только для обнаружения **IPM. MessageManager** сообщения. 
  
## <a name="remarks"></a>Замечания

В противном случае — устаревший перед **PR_CONVERSATION_INDEX**, [Свойство каноническое PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic каноническое является ли данное свойство **PR_CONVERSATION_KEY** Свойство](pidtagconversationtopic-canonical-property.md), который следует использовать.
  
## <a name="see-also"></a>См. также

- [Поддерево IPM](ipm-subtree.md)
- [����������� ����� MAPI](mapi-special-folders.md)

