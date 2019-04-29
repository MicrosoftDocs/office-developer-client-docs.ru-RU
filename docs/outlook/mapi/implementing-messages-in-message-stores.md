---
title: ���������� ��������� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 223dfa2ac990875e98e876ab491bf09caf63e874
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416645"
---
# <a name="implementing-messages-in-message-stores"></a><span data-ttu-id="e25cc-103">���������� ��������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="e25cc-103">Implementing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="e25cc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e25cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e25cc-p101">The [IMessage: IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span><span class="sxs-lookup"><span data-stu-id="e25cc-p101">The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Clients use the **IMAPIProp** methods to access the contents of a message. The **IMessage** interface supplies additional methods for manipulating messages (for example, adding attachments or modifying the recipients of a message). The methods in the **IMessage** interface modify attributes of messages that are not stored directly in the message's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e25cc-109">См. также</span><span class="sxs-lookup"><span data-stu-id="e25cc-109">See also</span></span>



[<span data-ttu-id="e25cc-110">���������� ��������� ���������</span><span class="sxs-lookup"><span data-stu-id="e25cc-110">Message Store Features</span></span>](message-store-features.md)

