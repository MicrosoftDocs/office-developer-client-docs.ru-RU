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
ms.openlocfilehash: ca9e5138d3ded13dfe33037f75e43ef1098f3c2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357339"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="74fb2-103">�������� ����� MAPI</span><span class="sxs-lookup"><span data-stu-id="74fb2-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="74fb2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74fb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74fb2-p101">�������� ����� � ��������, ���������� ��������� �������� ��� ����������� �������������� ������� ����������� ������� ��� ���������� ����� ����������� ����� � ��� ��������� (IPM). �������� ����� ��������� � �������� ����� ��� �������� ��������� � ����� �������, �� ����� � ��������� ����������� ����������. �� ��� ��������� ��������� �������� � ���� ������������� �����; ������ �������� ���������, ������� ��������� ��� ������ � �������� ��������� ��������� �� ��������� ��� ������ ���������� �������� ��.</span><span class="sxs-lookup"><span data-stu-id="74fb2-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="74fb2-108">MAPI ������������ ��� ������������� �����:</span><span class="sxs-lookup"><span data-stu-id="74fb2-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="74fb2-109">���������������� � ����� ����� ������������� �������� �������������, ������� �������� ������������ ��� �������� ��������� � ����� �������������� ����� ������������ �������, ������� ������������ ������ � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="74fb2-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="74fb2-110">Идентификатор записи для папки общего представления хранится в свойстве **пр_коммон_виевс_ентрид** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) хранилища.</span><span class="sxs-lookup"><span data-stu-id="74fb2-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="74fb2-111">������ � ����� ������ ������������� �������� �������������, ������� ���������� � ����������� ������������.</span><span class="sxs-lookup"><span data-stu-id="74fb2-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="74fb2-112">MAPI определяет свойство **пр_виевс_ентрид** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) для хранения идентификатора записи для папки личного представления.</span><span class="sxs-lookup"><span data-stu-id="74fb2-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="74fb2-113">������������� ������ �������������, � �������, ���� ������������ ����� ��������� � ������ ���������, ��������������� �� ����������� � ������ ������ ��������� ���� � ����������� ����; ������ ������������ ����� ��������� � ��� �� ������, ��������������� �� ����, ����, ����������� � ������ ���������.</span><span class="sxs-lookup"><span data-stu-id="74fb2-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74fb2-114">См. также</span><span class="sxs-lookup"><span data-stu-id="74fb2-114">See also</span></span>



[<span data-ttu-id="74fb2-115">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="74fb2-115">MAPI Folders</span></span>](mapi-folders.md)

