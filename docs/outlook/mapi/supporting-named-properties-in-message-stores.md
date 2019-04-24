---
title: ��������� ����������� ������� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 7e33c49d1ed211abf70e04a8bd3c06ca62e88572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349646"
---
# <a name="supporting-named-properties-in-message-stores"></a><span data-ttu-id="6ac4a-103">��������� ����������� ������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="6ac4a-103">Supporting Named Properties in Message Stores</span></span>

  
  
<span data-ttu-id="6ac4a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ac4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ac4a-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [����������� ����� ������� MAPI](defining-new-mapi-properties.md) and [��������� ����������� �������](supporting-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6ac4a-p101">Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).</span></span>
  
<span data-ttu-id="6ac4a-p102">����������� ��������� ��������� �����������, ������� ������������ ������������� ������� ������� ������ ������������� ��� ���� �������� � ��������� ��������� � ������. ��� ����� ��� ������������. ��-������ ����� ����������� �������� �������������, ���� �� ���������� ������ ��� ������������. ��-������ ���� ��� ������� � ��������� ��������� ������������ �� ������� �������������, ���������� ���������� �������������, ��� ��� �������������� ������� �� ��������� � ��������� ��������� ���������� ��������� �� ����� ����������� ��������. ��� ��������� ���������� ����������� ��� ����������� �������� ��� ����������� ������� � �� ������������� �����.</span><span class="sxs-lookup"><span data-stu-id="6ac4a-p102">Most message store providers that support named properties use a single mapping signature for all objects in the message store. This has two benefits. First, it is simpler to implement mapping signatures if there is only one to keep track of. Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property. This enables client applications to display columns for named properties in their folder view interface.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ac4a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="6ac4a-118">See also</span></span>



[<span data-ttu-id="6ac4a-119">Включение сообщений в хранилищах сообщений</span><span class="sxs-lookup"><span data-stu-id="6ac4a-119">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

