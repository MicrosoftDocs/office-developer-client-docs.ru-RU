---
title: ����� ������ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: c1d7f67458852319587d98831d031b2c3a131871
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400903"
---
# <a name="mapi-search-folders"></a><span data-ttu-id="273ad-103">����� ������ MAPI</span><span class="sxs-lookup"><span data-stu-id="273ad-103">MAPI Search Folders</span></span>

  
  
<span data-ttu-id="273ad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="273ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="273ad-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria�� rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span><span class="sxs-lookup"><span data-stu-id="273ad-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria — rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span></span> 
  
 <span data-ttu-id="273ad-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span><span class="sxs-lookup"><span data-stu-id="273ad-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span></span> <span data-ttu-id="273ad-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span><span class="sxs-lookup"><span data-stu-id="273ad-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span></span> <span data-ttu-id="273ad-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span><span class="sxs-lookup"><span data-stu-id="273ad-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span></span> <span data-ttu-id="273ad-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span><span class="sxs-lookup"><span data-stu-id="273ad-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span></span> <span data-ttu-id="273ad-115">Тем не менее для результатов поиска папок, свойство **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) указывает идентификатор записи к папке, где находится связанный сообщение.</span><span class="sxs-lookup"><span data-stu-id="273ad-115">However, for search-results folders, the **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property specifies the entry identifier of the folder where the linked message resides.</span></span> <span data-ttu-id="273ad-116">Search-results folders are not considered parent folders.</span><span class="sxs-lookup"><span data-stu-id="273ad-116">Search-results folders are not considered parent folders.</span></span>
  
<span data-ttu-id="273ad-117">���������� ������ ����� ����� ��������� �����������:</span><span class="sxs-lookup"><span data-stu-id="273ad-117">Search-results folders have the following limits:</span></span>
  
- <span data-ttu-id="273ad-p103">����������� ������ **SetSearchCriteria**�������� ������������ ��������, ��� ���������� ����� ����������� ������ ����� ���� ��������. �������������� �������� � ���������� **SetSearchCriteria**����� � ������ ���� ������ ���������� [260322: ��� ��� ����� ������ � ������� ������ SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).</span><span class="sxs-lookup"><span data-stu-id="273ad-p103">The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**. For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](https://go.microsoft.com/fwlink/?LinkId=123603).</span></span>
    
- <span data-ttu-id="273ad-120">������ ���������� ��������� � ���������� � ���������� ������ �����.</span><span class="sxs-lookup"><span data-stu-id="273ad-120">Messages cannot be moved or copied into search-results folders.</span></span>
    
- <span data-ttu-id="273ad-121">�� ����� ��������� ��������� ����� ����������� ������.</span><span class="sxs-lookup"><span data-stu-id="273ad-121">Search-results folders cannot contain subfolders.</span></span> 
    
- <span data-ttu-id="273ad-122">������� �� ������� ������� ����� ����������� ������ ���� ������.</span><span class="sxs-lookup"><span data-stu-id="273ad-122">Clients cannot make a search-results folder the subject of a search.</span></span>
    
<span data-ttu-id="273ad-p104">��� ��������, ������ ��� ��������� ������� ����� ����������� ������ � ����������� ��� ��� �������� ���������. ��������� ����� ������� �� ����� ����������� ������, ���������� ��������� �� ����� "��������". ��� �� ����� ������ � ����� ����� ���������� ������ �� ��������� ������� �� ��������� ������; ��� �������� � ����� �����, �������������.</span><span class="sxs-lookup"><span data-stu-id="273ad-p104">It is possible, however, to modify the properties of a search-results folder and use it to delete a message. When a message is deleted from a search-results folder, it is actually deleted from the real folder. However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="273ad-126">��. �����</span><span class="sxs-lookup"><span data-stu-id="273ad-126">See also</span></span>



[<span data-ttu-id="273ad-127">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="273ad-127">MAPI Folders</span></span>](mapi-folders.md)

