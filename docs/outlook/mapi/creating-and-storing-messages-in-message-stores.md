---
title: �������� � �������� ��������� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 32cfae36fb519654c1fb92d2f3b688c966f9288f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808239"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="b100c-103">�������� � �������� ��������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="b100c-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="b100c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b100c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b100c-p101">��� ���������� ��������� ���������, ������� � ��������� ��������� � ������� �������� �������� ������ ������� ������� �������� �������� ������. ��� ������� ���������� ������ �������� ���, ����� ��������� �������� ��������� � �� ��������.</span><span class="sxs-lookup"><span data-stu-id="b100c-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="b100c-p102">������� ��������� ���������� ������� ����� ���������, ��������� ������ ������� ��������� � ����������� �������� ��� ���������. ������ ���� ������� ����� ����� � ������������ �� [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) ����������. ����� ����� ���������� ���������� �������� ����� �������������� �������� � �������� [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="b100c-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="b100c-110">���� ��������� �������� ���������� ��������� ���������, ������� �������� ��������, ��������� ������ �������� �� ������� ��������� � ��������� �� �� ������� �������� ��������, ����� �������, ��� ��� ����� ���� ��������� ������������� ��� �������� ��������� ����� ������� ������.</span><span class="sxs-lookup"><span data-stu-id="b100c-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="b100c-p103">MAPI ���������, ��� � ��������� �� [IMessage](imessageimapiprop.md) ���������� �������� ����������, ��� ��������, ��� ���������, ��������� � ��� �� ���������� ����������� �� ������ ������ [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ������� ���������. ��� ���������� ����� ��������� �������� ���������� ��������� ���������. ������ ��� ��������; ������ ������, ��������� ������� � ������ �� ����� �� ��������� � ��� ����� ������������� ������� �������� �������� ��� ������ **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="b100c-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="b100c-114">��������� �������� �� ��������� ������� ����� ����������� ��������� ��� ���������� ����������, �� ��������� � ����� **SaveChanges** ��������� �������:</span><span class="sxs-lookup"><span data-stu-id="b100c-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="b100c-115">��������� �������� ������ ���� ������/������ ����� **SaveChanges** ������, �� ������ ��� ������ �����.</span><span class="sxs-lookup"><span data-stu-id="b100c-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="b100c-116">Например, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) имеет значение изначально клиентским приложением, которое создает сообщение (и поэтому чтение и запись), но не может быть изменен после первого вызова **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="b100c-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="b100c-p105">��������� �������� ����� ����������� ��������� � ��������� �����, � ������� ��� ��������� �, � ����� ������ **IMAPIFolder**. �������� �������� **PR_MESSAGE_FLAGS** ������� � �����, ������������ ��� ������ [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="b100c-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="b100c-119">��������� �������� �� ����� ���� ��������, ���� �� ����� ������ **SaveChanges** � ������ ���.</span><span class="sxs-lookup"><span data-stu-id="b100c-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="b100c-120">Например свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) могут быть недоступны до вызова метода **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="b100c-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="b100c-121">��������� �������� ����� ����� ����������� ��������� � ������� ���������� ������� ���������.</span><span class="sxs-lookup"><span data-stu-id="b100c-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="b100c-122">Например свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) обычно является производным от свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в поставщиков хранилища сообщений, которые поддерживают сообщений в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="b100c-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="b100c-123">��������� �������� ������������ ����� ������ ���� �������, ��������� � �������� ���������.</span><span class="sxs-lookup"><span data-stu-id="b100c-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="b100c-124">Например свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) требуется на папки и объекты, а также сообщения хранения объектов сообщений.</span><span class="sxs-lookup"><span data-stu-id="b100c-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="b100c-125">��� ��������������� �� ���������� ��������� ���������, ����� ����������� ���������� ��������� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="b100c-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b100c-126">��. �����</span><span class="sxs-lookup"><span data-stu-id="b100c-126">See also</span></span>



[<span data-ttu-id="b100c-127">���������� ��������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="b100c-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

