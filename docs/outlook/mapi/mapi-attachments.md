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
ms.openlocfilehash: 90fbec8b61499f383228823d69b041a21199a22e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417835"
---
# <a name="mapi-attachments"></a><span data-ttu-id="a4244-103">�������� MAPI</span><span class="sxs-lookup"><span data-stu-id="a4244-103">MAPI Attachments</span></span>

  
  
<span data-ttu-id="a4244-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4244-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4244-105">��������� ���������� ��������� ��������� �������������� �������� ��� ����� � ����������� ��������� ���������� � ���� ������, ������� OLE, ��������� ��� �������� ������.</span><span class="sxs-lookup"><span data-stu-id="a4244-105">Some message store providers enable clients to associate added information in the form of files, OLE objects, messages, or binary data with messages.</span></span> <span data-ttu-id="a4244-106">��� �������������� ��������, ���������� �������� ���������.</span><span class="sxs-lookup"><span data-stu-id="a4244-106">This added information is called a message's attachment.</span></span> <span data-ttu-id="a4244-107">��� ��� �������� ���������, ������������ � �������� ������ ����� ���� ���������, ��� ��������������� ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="a4244-107">Because attachments are created, maintained, and accessed only through their messages, they are considered message subobjects.</span></span> <span data-ttu-id="a4244-108">������ ����, ������������� ������ ��� �������, �������� ����� ���������������� �����, ��������� ��� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="a4244-108">Rather than having an entry identifier for access, attachments have a sequential number known as an attachment number.</span></span> <span data-ttu-id="a4244-109">��� ����� ���������� ���������� �������� � ���������, �� �� ����������� � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="a4244-109">This number uniquely identifies the attachment within its message, but not necessarily within the message store.</span></span> <span data-ttu-id="a4244-110">��� ������ ��������� ����� ��������� ��������� �������� � ���������� ������� ��������.</span><span class="sxs-lookup"><span data-stu-id="a4244-110">Two different messages can have different attachments with the same attachment number.</span></span> <span data-ttu-id="a4244-111">Номера вложений допустимы только в том случае, если оно открыто и хранится в свойстве **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a4244-111">Attachment numbers are only valid as long as the message is open and are stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="a4244-p102">��� ������� � ������� ���������� ��� ���� �������� ���������, ������� �������� ��� �������� � �������. � ������� �������� �������� ��������, ������� ������� ����� ������������ ��� ������� � �������� ��������, ����� ��� ���� ����� �������� � ���� ������. ������� ����� ��������� ������� �������� �:</span><span class="sxs-lookup"><span data-stu-id="a4244-p102">To access summary information about all of a message's attachments, clients retrieve its attachment table. The attachment table includes information that clients can use to access an attachment directly, such as its attachment number and record key. Clients can retrieve an attachment table by:</span></span>
  
- <span data-ttu-id="a4244-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span><span class="sxs-lookup"><span data-stu-id="a4244-p103">Calling **IMessage::GetAttachmentTable**. For more information, see [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).</span></span>
    
- <span data-ttu-id="a4244-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a4244-p104">Calling **IMAPIProp::OpenProperty**. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="a4244-119">Message store providers are expected to support both of these approaches.</span><span class="sxs-lookup"><span data-stu-id="a4244-119">Message store providers are expected to support both of these approaches.</span></span> <span data-ttu-id="a4244-120">Для подхода **опенпроперти** требуется, чтобы вызывающий оператор указал иид_имапитабле в качестве идентификатора интерфейса и \*\*пр_мессаже_аттачментс\*\* ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) в качестве тега свойства.</span><span class="sxs-lookup"><span data-stu-id="a4244-120">The **OpenProperty** approach requires that the caller specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) as the property tag.</span></span> <span data-ttu-id="a4244-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span><span class="sxs-lookup"><span data-stu-id="a4244-121">**PR_MESSAGE_ATTACHMENTS** is a table object property that represents a message's attachment table.</span></span> <span data-ttu-id="a4244-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span><span class="sxs-lookup"><span data-stu-id="a4244-122">Message store providers are required to set **PR_MESSAGE_ATTACHMENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method.</span></span> <span data-ttu-id="a4244-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span><span class="sxs-lookup"><span data-stu-id="a4244-123">For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).</span></span>
  
 <span data-ttu-id="a4244-124">����� ������������ **PR_MESSAGE_ATTACHMENTS**:</span><span class="sxs-lookup"><span data-stu-id="a4244-124">**PR_MESSAGE_ATTACHMENTS** can be used:</span></span> 
  
- <span data-ttu-id="a4244-125">� ������� **IMAPIProp::OpenProperty** ��� ������� � �������� ��� ���������� �������.</span><span class="sxs-lookup"><span data-stu-id="a4244-125">With **IMAPIProp::OpenProperty** to access an attachment or recipient table.</span></span> 
    
- <span data-ttu-id="a4244-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span><span class="sxs-lookup"><span data-stu-id="a4244-p106">With **IMAPIProp::CopyTo** or **IMAPIProp::CopyProps** to exclude or include attachments when copying. For more information, see [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMAPIProp::CopyProps](imapiprop-copyprops.md).</span></span>
    
- <span data-ttu-id="a4244-128">� �������� ����������� ��������� �������, ����� �������, ��� ����������� �������� ������� ��������� � ��������.</span><span class="sxs-lookup"><span data-stu-id="a4244-128">In a subobject restriction to indicate that the child restriction should apply to attachments.</span></span>
    
<span data-ttu-id="a4244-129">For more information, see [������� ��������](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a4244-129">For more information, see [Attachment Tables](attachment-tables.md).</span></span>
  

