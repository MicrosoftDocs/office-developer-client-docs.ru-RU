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
  
Ключ беседы почты Windows для workgroups 3.1 является текстовой строкой. Эквивалент MAPI — это двоичное значение. Для обеспечения обратной совместимости реализация TNEF преобразует двоичные данные в текст и добавляет завершающий символ null.
  
> [!NOTE]
> Соответствующие свойства в MAPI, с которыми связываются эти атрибуты TNEF, PR_CONVERSATION_KEY и PR_PARENT_KEY, были неподдержаты в Microsoft Exchange Server: использование **PR_CONVERSATION_KEY**, каноническое свойство [PidTagConversationKey](pidtagconversationkey-canonical-property.md), сохраняется только в Outlook для locating **IPM. Сообщения MessageManager.** 
  
## <a name="remarks"></a>Примечания

Свойство **PR_CONVERSATION_KEY** является устаревшим предшествует каноническому свойству **PR_CONVERSATION_INDEX,** [PidTagConversationIndex и](pidtagconversationindex-canonical-property.md) **PR_CONVERSATION_TOPIC,** [PidTagConversationTopic,](pidtagconversationtopic-canonical-property.md)которое следует использовать.
  
## <a name="see-also"></a>См. также

- [Подtree IPM](ipm-subtree.md)
- [Специальные папки MAPI](mapi-special-folders.md)

