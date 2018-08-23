---
title: ����� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 21b738424b27d3d89d8de84c8c9ff2ff86dd945b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564089"
---
# <a name="mapi-folders"></a><span data-ttu-id="c95d1-103">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="c95d1-103">MAPI Folders</span></span>

  
  
<span data-ttu-id="c95d1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c95d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c95d1-p101">����� � ��� ������� MAPI, ������� ������������ � �������� ��������� ����� ����������� ��� ���������. ������������ ������������ ����� ����� ��������� ��������� � ������ �����. ����� ��������� ��� ����������� � ������ � �����������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-p101">Folders are MAPI objects that serve as the basic unit of organization for messages. Arranged hierarchically, folders can contain messages and other folders. Folders make it easier to locate and work with messages.</span></span>
  
<span data-ttu-id="c95d1-p102">����� ����������� ��������� [IMAPIFolder](imapifolderimapicontainer.md) , ������� �������� ����������� �� ���������� **IUnknown** ����� [IMAPIContainer](imapicontainerimapiprop.md) � [IMAPIProp](imapipropiunknown.md) ����������. ������� ���������� **IMAPIFolder** ��������, ����������� � �������� ��������� � �����, ����� �������� � ������ ��������� ��������� ��� ���������� ��� ������� ������ ������ ���� ��� ���������. �������� �� ��, ��� ����������� ��������� ��������� ���������� ��� ��������� ��� ������ � **IMAPIFolder**, ��������� ������ ������������� ������� ���������, ����� ������������� �������� ����������� ��������� ���������. MAPI ��������� ������������ �������� ����������� ��������� ��������� ��� ������ ��������� ����� ������� ������� ����� � ���������� [IMAPISupport](imapisupportiunknown.md) . ��������, ������ ���� ����� ������������� ����������� ������ ����������� ����������� ��������� ��������� ����� ������� ������ ����������� � ������� ��������� � �������� �� �� ����������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-p102">Folders implement the [IMAPIFolder](imapifolderimapicontainer.md) interface, which indirectly inherits from the **IUnknown** interface through the [IMAPIContainer](imapicontainerimapiprop.md) and [IMAPIProp](imapipropiunknown.md) interfaces. Clients use **IMAPIFolder** to create, copy, and delete messages and folders, to retrieve and set message status, and to set or clear the read flag for a message. Although message store providers are required to support all the methods in **IMAPIFolder**, some methods introduce a level of complexity that message store providers might want to avoid. MAPI saves message store providers some work by implementing some of the more complex folder functionality in the [IMAPISupport](imapisupportiunknown.md) interface. Rather than implementing their own copy methods, for example, message store providers can call the copy methods in the support object and get the same results.</span></span> 
  
<span data-ttu-id="c95d1-113">���������� ��� ���� �����.</span><span class="sxs-lookup"><span data-stu-id="c95d1-113">There are three kinds of folders:</span></span>
  
- <span data-ttu-id="c95d1-114">�������� �����.</span><span class="sxs-lookup"><span data-stu-id="c95d1-114">Root folders.</span></span>
    
- <span data-ttu-id="c95d1-115">������������� �����.</span><span class="sxs-lookup"><span data-stu-id="c95d1-115">Generic folders.</span></span>
    
- <span data-ttu-id="c95d1-116">����� ������</span><span class="sxs-lookup"><span data-stu-id="c95d1-116">Search folders.</span></span>
    
<span data-ttu-id="c95d1-p103">������ ��������� ��������� ����� �� ������� ���� � �������� �����. � �������� ����� ������������ � ������� ����� �������� � �������� ��������� � ������ �����. �������� ����� �� ������� ���������, �����������, ������������� ��� ������. ���������� ������ ���� �������� ����� ��� ������� ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-p103">Every message store has at least a root folder. The root folder appears at the top of the hierarchy and contains messages and other folders. Root folders cannot be moved, copied, renamed, or deleted. There is only one root folder for each message store.</span></span>
  
<span data-ttu-id="c95d1-p104">����������� ����� � �������������. ��� � �������� ����� ������������� ����� �������� ��������� � ������ �����. � ������� �� �������� ����� �� ����� ����������, ����������, ������������� � �������. ������������� ����� ����� ���� ������� � �������� ����� ��� ������ ������������� �����. ����� ������ ������� ����� ����� � ������ �����, ����� ����� ���������� ��������� ����� ��� ��������� �����. �����, � ������� ����������� ����� ����� ���������� ������������ ����� ����� �����. ������������� �����, ������� ����� ���� � �� �� ����� ������������� ���������� �����. ������������� ������� � ��-����� ����� ��� ����� ����� ���������� �����, � ����������� �� ��������� ��������� ���������. ���������� ��������� ���������, ������� ������� ����� ��� �������� �������� ������ MAPI_E_COLLISION ��� ������� ������� ������� ��� ����� � ��� �� ������ � �� ������������ ���������� �����.</span><span class="sxs-lookup"><span data-stu-id="c95d1-p104">Most other folders are generic folders. Like root folders, generic folders contain messages and other folders. Unlike root folders, they can be moved, copied, renamed, and deleted. Generic folders can be created in the root folder or other generic folders. When a client creates a generic folder in another folder, the new folder is called a subfolder, or child folder. The folder in which the new folder is placed is referred to as the parent folder of the new folder. Generic folders that have the same parent folder are called sibling folders. Both sibling and non-sibling folders may or may not have unique names, depending on the message store provider. Message store providers that require sibling folders to have unique names return the error value MAPI_E_COLLISION when a client attempts to create two folders with the same name in the same parent.</span></span> 
  
<span data-ttu-id="c95d1-p105">����� ������ �������� ������ �� ���������, ������� ������������� ������ �������������� �������� �������. ��� ��� ����� ������ �������� ������, � �� ����������� ���������, ��� �������� ���������� ������ ��� ������. ��� �� ����� ��������� ������ ����� ��� ��������� ��� ����� ����������� ��� ����������� � ���. ��� �� ����� ����� ����� ���������, ��������� � ���; � ��� ���� ������ ����������, ����������� ��� ������������. ��������� ������� �� ����� ������, ���������� ��������� �� �����, ���������� ���������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-p105">A search folder contains links to messages that match a set of predefined criteria. Because search folders contain links rather than actual messages, they are in effect read-only. They cannot contain other folders or have messages or folders moved or copied into them. They cannot have new messages created in them; and they themselves cannot be moved, copied, or renamed. When a message is deleted from a search folder, it is actually deleted from the folder that contains the message.</span></span>
  
<span data-ttu-id="c95d1-135">Тип папки хранится в свойстве **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c95d1-135">Folder type is stored in the **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)) property.</span></span> <span data-ttu-id="c95d1-136">������ ����� ��� �������� ����� �������� FOLDER_GENERIC, FOLDER_ROOT ��� FOLDER_SEARCH, � ����������� �� ����.</span><span class="sxs-lookup"><span data-stu-id="c95d1-136">Every folder has this property set to either FOLDER_GENERIC, FOLDER_ROOT, or FOLDER_SEARCH, depending on its type.</span></span>
  
<span data-ttu-id="c95d1-137">������ ����� ���� ���� ������ �������������� � ���� ���� ������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-137">Every folder has one entry identifier and one record key.</span></span> <span data-ttu-id="c95d1-138">Идентификатор записи, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), используется клиентами и поставщиков услуг для откройте папку.</span><span class="sxs-lookup"><span data-stu-id="c95d1-138">The entry identifier, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), is used by clients and service providers to open the folder.</span></span> <span data-ttu-id="c95d1-139">Ключ записи, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) — это двоичное значение, которое используется для сравнения папки с другими папками.</span><span class="sxs-lookup"><span data-stu-id="c95d1-139">The record key, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), is a binary value that is used to compare the folder with other folders.</span></span> 
  
<span data-ttu-id="c95d1-p108">����� ����� ������ �������� ��� ������������� ��������� � ���� ����� � ��������� ���������. ���������� ��������� ��������:</span><span class="sxs-lookup"><span data-stu-id="c95d1-p108">A folder has other properties to identify related folders and the message store. The following properties are required:</span></span>
  
- <span data-ttu-id="c95d1-142">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c95d1-142">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c95d1-143">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c95d1-143">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c95d1-144">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c95d1-144">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>
    
<span data-ttu-id="c95d1-145">Свойство **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), который описывает тип операции, которые пользователь может выполнять поддержка некоторых папок.</span><span class="sxs-lookup"><span data-stu-id="c95d1-145">Some folders support the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property which describes the type of operations a user can perform.</span></span> <span data-ttu-id="c95d1-146">�������� ���� �� ���������� �������� **PR_ACCESS** � MAPI_ACCESS_DELETE, ��� ��������, ��� ����� ����� ���� �������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-146">For example, one of the valid settings for **PR_ACCESS** is MAPI_ACCESS_DELETE, which indicates that the folder can be removed.</span></span> <span data-ttu-id="c95d1-147">���� ��������, MAPI_ACCESS_MODIFY, ���������, ��� ����� ������ ���� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="c95d1-147">Another setting, MAPI_ACCESS_MODIFY, indicates that the folder should be modifiable.</span></span> 
  
<span data-ttu-id="c95d1-148">������ ������ �������� ����������� ����� � ������� ��������� [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="c95d1-148">For a complete list of required folder properties, see the [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c95d1-149">��. �����</span><span class="sxs-lookup"><span data-stu-id="c95d1-149">See also</span></span>



[<span data-ttu-id="c95d1-150">���������� ���������� MAPI</span><span class="sxs-lookup"><span data-stu-id="c95d1-150">MAPI Application Development</span></span>](mapi-application-development.md)

