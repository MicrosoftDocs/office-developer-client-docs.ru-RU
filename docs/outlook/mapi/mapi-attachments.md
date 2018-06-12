---
title: �������� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6e6c6ad9-1e07-4234-a5ef-18020d7ce468
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: c6538f8fef7d8ccb87b6e6d9d2b9c68779ca8582
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809711"
---
# <a name="mapi-attachments"></a><span data-ttu-id="d7c3d-103">�������� MAPI</span><span class="sxs-lookup"><span data-stu-id="d7c3d-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="d7c3d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7c3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7c3d-105">��������� ���������� ��������� ��������� �������������� �������� ��� ����� � ����������� ��������� ���������� � ���� ������, ������� OLE, ��������� ��� �������� ������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="d7c3d-106">��� �������������� ��������, ���������� �������� ���������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="d7c3d-107">��� ��� �������� ���������, ������������ � �������� ������ ����� ���� ���������, ��� ��������������� ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="d7c3d-108">������ ����, ������������� ������ ��� �������, �������� ����� ���������������� �����, ��������� ��� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="d7c3d-109">��� ����� ���������� ���������� �������� � ���������, �� �� ����������� � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="d7c3d-110">��� ������ ��������� ����� ��������� ��������� �������� � ���������� ������� ��������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="d7c3d-111">Номера вложения действительны только, пока сообщение открыто и сохраняются в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7c3d-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d7c3d-p102">��� ������� � ������� ���������� ��� ���� �������� ���������, ������� �������� ��� �������� � �������. � ������� �������� �������� ��������, ������� ������� ����� ������������ ��� ������� � �������� ��������, ����� ��� ���� ����� �������� � ���� ������. ������� ����� ��������� ������� �������� �:</span><span class="sxs-lookup"><span data-stu-id="d7c3d-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="d7c3d-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3d-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="d7c3d-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3d-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="d7c3d-119">Message store providers are expected to support both of these approaches.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="d7c3d-120">Подход **OpenProperty** требуется указать, что вызывающего IID_IMAPITable как идентификатор интерфейса и **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) как тега свойства.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="d7c3d-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="d7c3d-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="d7c3d-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3d-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="d7c3d-124">����� ������������ **PR_MESSAGE_ATTACHMENTS**:</span><span class="sxs-lookup"><span data-stu-id="d7c3d-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="d7c3d-125">� ������� **IMAPIProp::OpenProperty** ��� ������� � �������� ��� ���������� �������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="d7c3d-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3d-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="d7c3d-128">� �������� ����������� ��������� �������, ����� �������, ��� ����������� �������� ������� ��������� � ��������.</span><span class="sxs-lookup"><span data-stu-id="d7c3d-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="d7c3d-129">For more information, see [������� ��������](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d7c3d-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

