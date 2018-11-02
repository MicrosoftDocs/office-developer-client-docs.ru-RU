---
title: �������� ����� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1936ec2-bf8a-4242-a41d-64d26b813bd0
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 3a89588294f07dca97fb48e56d2cde890c3f80ae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568821"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="caf17-103">�������� ����� MAPI</span><span class="sxs-lookup"><span data-stu-id="caf17-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="caf17-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caf17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caf17-p101">�������� ����� � ��������, ���������� ��������� �������� ��� ����������� �������������� ������� ����������� ������� ��� ���������� ����� ����������� ����� � ��� ��������� (IPM). �������� ����� ��������� � �������� ����� ��� �������� ��������� � ����� �������, �� ����� � ��������� ����������� ����������. �� ��� ��������� ��������� �������� � ���� ������������� �����; ������ �������� ���������, ������� ��������� ��� ������ � �������� ��������� ��������� �� ��������� ��� ������ ���������� �������� ��.</span><span class="sxs-lookup"><span data-stu-id="caf17-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="caf17-108">MAPI ������������ ��� ������������� �����:</span><span class="sxs-lookup"><span data-stu-id="caf17-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="caf17-109">���������������� � ����� ����� ������������� �������� �������������, ������� �������� ������������ ��� �������� ��������� � ����� �������������� ����� ������������ �������, ������� ������������ ������ � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="caf17-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="caf17-110">Идентификатор записи для общих папок представления хранится в свойстве **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) хранилища.</span><span class="sxs-lookup"><span data-stu-id="caf17-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="caf17-111">������ � ����� ������ ������������� �������� �������������, ������� ���������� � ����������� ������������.</span><span class="sxs-lookup"><span data-stu-id="caf17-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="caf17-112">MAPI определяет свойство **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) для хранения идентификатор записи папки, в личном представлении.</span><span class="sxs-lookup"><span data-stu-id="caf17-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="caf17-113">������������� ������ �������������, � �������, ���� ������������ ����� ��������� � ������ ���������, ��������������� �� ����������� � ������ ������ ��������� ���� � ����������� ����; ������ ������������ ����� ��������� � ��� �� ������, ��������������� �� ����, ����, ����������� � ������ ���������.</span><span class="sxs-lookup"><span data-stu-id="caf17-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="caf17-114">��. �����</span><span class="sxs-lookup"><span data-stu-id="caf17-114">See also</span></span>



[<span data-ttu-id="caf17-115">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="caf17-115">MAPI Folders</span></span>](mapi-folders.md)

