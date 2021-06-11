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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412536"
---
# <a name="mapi-view-folders"></a><span data-ttu-id="f4138-103">�������� ����� MAPI</span><span class="sxs-lookup"><span data-stu-id="f4138-103">MAPI View Folders</span></span>

  
  
<span data-ttu-id="f4138-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4138-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4138-p101">�������� ����� � ��������, ���������� ��������� �������� ��� ����������� �������������� ������� ����������� ������� ��� ���������� ����� ����������� ����� � ��� ��������� (IPM). �������� ����� ��������� � �������� ����� ��� �������� ��������� � ����� �������, �� ����� � ��������� ����������� ����������. �� ��� ��������� ��������� �������� � ���� ������������� �����; ������ �������� ���������, ������� ��������� ��� ������ � �������� ��������� ��������� �� ��������� ��� ������ ���������� �������� ��.</span><span class="sxs-lookup"><span data-stu-id="f4138-p101">View folders are root folders that contain associated information to define alternative display layouts for the contents of interpersonal message (IPM) folders. View folders reside under the root for the message store and, therefore, are not visible in the typical client application. Not every message store includes view folders; only message stores that are configured to work as the default message store for the session must include them.</span></span>  
  
<span data-ttu-id="f4138-108">MAPI ������������ ��� ������������� �����:</span><span class="sxs-lookup"><span data-stu-id="f4138-108">MAPI supports two view folders:</span></span>
  
- <span data-ttu-id="f4138-109">���������������� � ����� ����� ������������� �������� �������������, ������� �������� ������������ ��� �������� ��������� � ����� �������������� ����� ������������ �������, ������� ������������ ������ � ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="f4138-109">Common — The common view folder contains views that are standard for the message store and can be used by any user of a client that accesses the message store.</span></span> <span data-ttu-id="f4138-110">Идентификатор входа для общей папки представления хранится в  свойстве[PR_COMMON_VIEWS_ENTRYID (PidTagCommonViewsEntryId).](pidtagcommonviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f4138-110">The entry identifier for the common view folder is stored in the store's **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="f4138-111">������ � ����� ������ ������������� �������� �������������, ������� ���������� � ����������� ������������.</span><span class="sxs-lookup"><span data-stu-id="f4138-111">Personal — The personal view folder contains views that are defined by a particular user.</span></span> <span data-ttu-id="f4138-112">MAPI определяет **свойство PR_VIEWS_ENTRYID** [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)для удержания идентификатора входа в папку личного представления.</span><span class="sxs-lookup"><span data-stu-id="f4138-112">MAPI defines the **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)) property for holding the entry identifier of the personal view folder.</span></span> <span data-ttu-id="f4138-113">������������� ������ �������������, � �������, ���� ������������ ����� ��������� � ������ ���������, ��������������� �� ����������� � ������ ������ ��������� ���� � ����������� ����; ������ ������������ ����� ��������� � ��� �� ������, ��������������� �� ����, ����, ����������� � ������ ���������.</span><span class="sxs-lookup"><span data-stu-id="f4138-113">Using personal views, for example, one user could look at a group of messages sorted by sender, listing only the message subject and receipt date; another user could look at the same group sorted by date, listing the subject, sender, and message size.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4138-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f4138-114">See also</span></span>



[<span data-ttu-id="f4138-115">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="f4138-115">MAPI Folders</span></span>](mapi-folders.md)

