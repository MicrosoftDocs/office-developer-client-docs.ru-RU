---
title: ������������ �����
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 7f1dd7a23bbd643b496b7634b6ad0230c806585f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398607"
---
# <a name="tracking-conversations"></a><span data-ttu-id="15696-103">������������ �����</span><span class="sxs-lookup"><span data-stu-id="15696-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="15696-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15696-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15696-p101">������������ ��������� �������� ���� ������� �� ���������. ������� ������� ���������� ��� ��������, ������� �������� ��� ������������ ������:</span><span class="sxs-lookup"><span data-stu-id="15696-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="15696-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="15696-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="15696-108">**PR_CONVERSATION_TOPIC** � ��� ��������������� ���� ���������, ���� ��� �������� �����.</span><span class="sxs-lookup"><span data-stu-id="15696-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="15696-109">Этому свойству присвоено значение свойства **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) сообщение.</span><span class="sxs-lookup"><span data-stu-id="15696-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="15696-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="15696-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="15696-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span><span class="sxs-lookup"><span data-stu-id="15696-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="15696-p104">**ScCreateConversationIndex** ������� �������� ������� ������ ��� ���� ��������� ���������. **ScCreateConversationIndex** ��������� ������ ��� ���� ���������, ������� �������� 22 ����� � �����, � ����� �� ���� ��� ��������� �������� ��������� ������� 5 ����.</span><span class="sxs-lookup"><span data-stu-id="15696-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="15696-116">��������� ����� ������� �� 22 �����, ��������� �� ���� ������:</span><span class="sxs-lookup"><span data-stu-id="15696-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="15696-p105">���� ��������������� ������. ��� �������� ����� 1.</span><span class="sxs-lookup"><span data-stu-id="15696-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="15696-119">���� ���� ��� ������� ��������� ����� ������������� � ������ [FILETIME](filetime.md) ���������.</span><span class="sxs-lookup"><span data-stu-id="15696-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="15696-120">����������� ���� ���������� ���������� ������������� ��� [������������� GUID](guid.md)� ������.</span><span class="sxs-lookup"><span data-stu-id="15696-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="15696-121">������ ���� �������� ������� �� 5 ������, ��������� ��������� �������:</span><span class="sxs-lookup"><span data-stu-id="15696-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="15696-p106">���� ���, ���������� ���, ������� ������������ �������� ����� �������� ������� � �������, ���������� � ����� �������� �����������. ���� ��� ����� ����� �������� 0, ���� ������� ������, ���.02 ������� � ������, ��� ��� ���� � 1, ���� �������� �� ��������� ����� ������� � ������, ��� 56 ���.</span><span class="sxs-lookup"><span data-stu-id="15696-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="15696-p107">30 ���� ���, ���������� �������� ����� �������� ������� � ����� � ����� ��������� � �������� **FILETIME**. ��� ����� ����� �������� ��������� � ������� ������ �� ���� ���������, � ����������� �� ������� ����. ���� ���� ��� ����� ����, **ScCreateConversationIndex** ������� ������� 15 ��� � ������ 18 �������� ������. ���� ���� ���, ������� ������� ������� 10 ��� � ������ 23 �����.</span><span class="sxs-lookup"><span data-stu-id="15696-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="15696-127">������ ����, ���������� ��������� �����, ����������� ��� ������ ������� Win32 [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="15696-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="15696-128">������ ����, ���������� ����������� ������, ������� ���� �� ����� ��������� �����.</span><span class="sxs-lookup"><span data-stu-id="15696-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="15696-129">���� ������� ������� �������� ������ ��������� �������, ���������� ��������� ������������:</span><span class="sxs-lookup"><span data-stu-id="15696-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="15696-130">�������� �������� � ������� ������ ������������ ����������. � ������� ������� � ������� UTC, � �� �������� �������.</span><span class="sxs-lookup"><span data-stu-id="15696-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="15696-131">������ ������ ������ ��������� �� �� �� �����.</span><span class="sxs-lookup"><span data-stu-id="15696-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="15696-132">���������� ������ �� ���� � ��� �� ���� ���������.</span><span class="sxs-lookup"><span data-stu-id="15696-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="15696-133">��������� ������ ������ � ������ �����, ������������ ��� ����������� ������������� ������ �������.</span><span class="sxs-lookup"><span data-stu-id="15696-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="15696-134">��� ���������� ���������� �� ����������, ����� ��������� ��������������� �� ������, ���������� �� **PR_CONVERSATION_TOPIC** ������ � ����� �� **PR_CONVERSATION_INDEX**.</span><span class="sxs-lookup"><span data-stu-id="15696-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="15696-135">Чтобы представить результаты сортировки, присвойте свойству **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) 0 для сообщений с индексом беседы, который является 22 байта в длину.</span><span class="sxs-lookup"><span data-stu-id="15696-135">To present the results of the sort, set the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="15696-136">����� ��� ������ 5-�������� ����������� ������ � �����, ����������� �������� �������� **PR_DEPTH** �� 1.</span><span class="sxs-lookup"><span data-stu-id="15696-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="15696-137">������ PR_ORIGINAL ������� ����� ����� �������������� ��� ������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="15696-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="15696-138">������� ��� �������� ��� ���������� �������� ��� ���������������� ��������� ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="15696-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="15696-139">��� �������� PR_ORIGINAL �������� ���������������.</span><span class="sxs-lookup"><span data-stu-id="15696-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="15696-140">Если вы не задано явно, например, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), поставщика хранилища сообщений можно использовать значение по умолчанию, или значение **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) свойство.</span><span class="sxs-lookup"><span data-stu-id="15696-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="15696-141">Аналогичным образом Если не установлен **PR_ORIGINAL_AUTHOR_NAME** или **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), эти свойства можно по умолчанию значения **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и **PR_ CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) свойства соответственно.</span><span class="sxs-lookup"><span data-stu-id="15696-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

