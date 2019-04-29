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
> Соответствующие свойства MAPI, которым сопоставляются эти атрибуты TNEF, ПР_КОНВЕРСАТИОН_КЭЙ и ПР_ПАРЕНТ_КЭЙ, не рекомендуются в Microsoft Exchange Server: использование **пр_конверсатион_кэй**, [PidTagConversationKey каноническое свойство Свойство](pidtagconversationkey-canonical-property.md)хранится только в Outlook, для поиска **IPM. Сообщения Мессажеманажер** . 
  
## <a name="remarks"></a>Примечания

Свойство **пр_конверсатион_кэй** является устаревшей версией прекурсор для канонического свойства **Пр_конверсатион_индекс**, [PidTagConversationIndex канонического свойства](pidtagconversationindex-canonical-property.md) и **пр_конверсатион_топик**, [PidTagConversationTopic канонического ](pidtagconversationtopic-canonical-property.md), Которое следует использовать вместо этого свойства.
  
## <a name="see-also"></a>См. также

- [Поддерево IPM](ipm-subtree.md)
- [Специальные папки MAPI](mapi-special-folders.md)

