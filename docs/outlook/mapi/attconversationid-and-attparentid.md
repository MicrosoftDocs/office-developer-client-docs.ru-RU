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
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="adda8-103">attConversationID и attParentID</span><span class="sxs-lookup"><span data-stu-id="adda8-103">attConversationID and attParentID</span></span>

<span data-ttu-id="adda8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adda8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adda8-105">Windows для рабочих групп 3.1 почты беседы ключ — это строка текста.</span><span class="sxs-lookup"><span data-stu-id="adda8-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="adda8-106">Эквивалент MAPI — это двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="adda8-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="adda8-107">Для обеспечения обратной совместимости, реализация TNEF преобразует двоичные данные в текст и добавляет конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="adda8-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="adda8-108">Соответствующих свойств в MAPI для которой сопоставляются эти атрибуты TNEF, PR_CONVERSATION_KEY и PR_PARENT_KEY, являются устаревшими в Microsoft Exchange Server: использование **PR_CONVERSATION_KEY**, [PidTagConversationKey каноническое Свойство](pidtagconversationkey-canonical-property.md), сохраняется в Outlook, только для обнаружения **IPM. MessageManager** сообщения.</span><span class="sxs-lookup"><span data-stu-id="adda8-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="adda8-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="adda8-109">Remarks</span></span>

<span data-ttu-id="adda8-110">В противном случае — устаревший перед **PR_CONVERSATION_INDEX**, [Свойство каноническое PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic каноническое является ли данное свойство **PR_CONVERSATION_KEY** Свойство](pidtagconversationtopic-canonical-property.md), который следует использовать.</span><span class="sxs-lookup"><span data-stu-id="adda8-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="adda8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="adda8-111">See also</span></span>

- [<span data-ttu-id="adda8-112">Поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="adda8-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="adda8-113">����������� ����� MAPI</span><span class="sxs-lookup"><span data-stu-id="adda8-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

