---
title: �������������� ������� � ������ � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 0e7b479931b6b2b00dd3927133187fe058b4c6e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808396"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="0cb62-103">�������������� ������� � ������ � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="0cb62-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="0cb62-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0cb62-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0cb62-p101">������ ��������� �������� ��������� ���������� ����������� �������� ������ ���������� [IMAPIFolder](imapifolderimapicontainer.md) ��� ���������� ����������. ������������� ����� �������� ������ � ��������� ��� ���������; ��� ������������� ������ � ������, ������� ����� ������ ������������ ��� ���������� ��������� ���������. ����� ����, ����� �������� ������ ����� ������������ ��� �������� �� ��������� �������� ����� ��� ���������������� �������� ��������� � ��� ����� �� ������� ������ ������������ ������. ���������� ��������� ��������� ����� ���������� ����������� ��������� IPM � ����� �����, ������������ ��� �������� ��������� IPM � �� ���������� ����������.</span><span class="sxs-lookup"><span data-stu-id="0cb62-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="0cb62-p102">���������� ���������� ����� ������� ����� �������� ������, ������ ����� [IMsgStore::OpenEntry](imsgstore-openentry.md) � 0 �� NULL ����������  _cbEntryId_ �  _lpEntryId_, ��������������. ��� �� �����, � ����������� ������� ���������� ���������� �������� � ����� �����, ���������� IPM ���������.</span><span class="sxs-lookup"><span data-stu-id="0cb62-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="0cb62-111">����� �������� ������ �����, ������������� � ��������� ��������� IPM ����� ������, ����������� ��������� ���������:</span><span class="sxs-lookup"><span data-stu-id="0cb62-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="0cb62-112">����������� ����� MAPI ��� ������ ������ [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) .</span><span class="sxs-lookup"><span data-stu-id="0cb62-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="0cb62-113">Используйте полученный в результате указатель базы данных сообщений для вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) для свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0cb62-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="0cb62-114">�������� ����� [IMsgStore::OpenEntry](imsgstore-openentry.md) � ��������������� ������ ��� ��������� ��������� **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="0cb62-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="0cb62-115">�������� ����� [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) ��� ��������� ������� ���������� �����.</span><span class="sxs-lookup"><span data-stu-id="0cb62-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="0cb62-116">�������� ����� [IMAPITable::QueryRows](imapitable-queryrows.md) � ������ ����� � ����� �������� ������.</span><span class="sxs-lookup"><span data-stu-id="0cb62-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="0cb62-p103">MAPI ������� ���������� ��� ����� ��� ������� � ������ �������� ����� � ��������� �������� � ��������� ���������. **IMAPIFolder**� ��� ������������� ���������� [IMAPIContainer](imapicontainerimapiprop.md)�������� ������, ������� ������ ������������� ���������� ��������� ��������� ��� ���������� ����� � ��������� ��������� � �������� �� ������� ������� ��� ������ � ����������.</span><span class="sxs-lookup"><span data-stu-id="0cb62-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0cb62-119">��. �����</span><span class="sxs-lookup"><span data-stu-id="0cb62-119">See also</span></span>



[<span data-ttu-id="0cb62-120">���������� ����� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="0cb62-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

