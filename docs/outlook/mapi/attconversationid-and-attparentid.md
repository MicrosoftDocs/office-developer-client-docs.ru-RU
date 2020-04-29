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
# <a name="attconversationid-and-attparentid"></a><span data-ttu-id="017b6-103">attConversationID и attParentID</span><span class="sxs-lookup"><span data-stu-id="017b6-103">attConversationID and attParentID</span></span>

<span data-ttu-id="017b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="017b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="017b6-105">Ключ беседы Windows для рабочих групп 3,1 представляет собой текстовую строку.</span><span class="sxs-lookup"><span data-stu-id="017b6-105">The Windows for Workgroups 3.1 Mail conversation key is a text string.</span></span> <span data-ttu-id="017b6-106">Эквивалент MAPI является двоичным значением.</span><span class="sxs-lookup"><span data-stu-id="017b6-106">The MAPI equivalent is a binary value.</span></span> <span data-ttu-id="017b6-107">Для обеспечения обратной совместимости реализация формата TNEF преобразует двоичные данные в текст и добавляет завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="017b6-107">To provide backward compatibility, the TNEF implementation converts the binary data to text and adds a terminating null character.</span></span>
  
> [!NOTE]
> <span data-ttu-id="017b6-108">Соответствующие свойства MAPI, которым сопоставлены эти атрибуты TNEF, PR_CONVERSATION_KEY и PR_PARENT_KEY, не поддерживаются в Microsoft Exchange Server: использование **PR_CONVERSATION_KEY**, [каноническое свойство PidTagConversationKey](pidtagconversationkey-canonical-property.md), только в Outlook, для поиска **IPM. Сообщения Мессажеманажер** .</span><span class="sxs-lookup"><span data-stu-id="017b6-108">The corresponding properties in MAPI to which these TNEF attributes are mapped, PR_CONVERSATION_KEY and PR_PARENT_KEY, have been deprecated in Microsoft Exchange Server: Use of **PR_CONVERSATION_KEY**, the [PidTagConversationKey Canonical Property](pidtagconversationkey-canonical-property.md), persists in Outlook only, for locating **IPM.MessageManager** messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="017b6-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="017b6-109">Remarks</span></span>

<span data-ttu-id="017b6-110">Свойство **PR_CONVERSATION_KEY** — это значение, не являющееся устаревшим прекурсор **PR_CONVERSATION_INDEX**, [каноническое свойство](pidtagconversationindex-canonical-property.md) и **PR_CONVERSATION_TOPIC**, [каноническое свойство PidTagConversationTopic](pidtagconversationtopic-canonical-property.md), которое следует использовать вместо этого.</span><span class="sxs-lookup"><span data-stu-id="017b6-110">The **PR_CONVERSATION_KEY** property is the otherwise obsolete precursor of the **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Canonical Property](pidtagconversationindex-canonical-property.md) and **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic Canonical Property](pidtagconversationtopic-canonical-property.md), which should be used instead.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="017b6-111">См. также</span><span class="sxs-lookup"><span data-stu-id="017b6-111">See also</span></span>

- [<span data-ttu-id="017b6-112">Поддерево IPM</span><span class="sxs-lookup"><span data-stu-id="017b6-112">IPM Subtree</span></span>](ipm-subtree.md)
- [<span data-ttu-id="017b6-113">Специальные папки MAPI</span><span class="sxs-lookup"><span data-stu-id="017b6-113">MAPI Special Folders</span></span>](mapi-special-folders.md)

