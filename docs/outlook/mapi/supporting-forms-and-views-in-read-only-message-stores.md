---
title: ��������� ���� � ������������� � �������� ��������� ������ ��� ������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 52aebb53f2bc0e5af72f2da47b91ba2806d7f709
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563354"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a><span data-ttu-id="44017-103">��������� ���� � ������������� � �������� ��������� ������ ��� ������</span><span class="sxs-lookup"><span data-stu-id="44017-103">Supporting Forms and Views in Read-Only Message Stores</span></span>

  
  
<span data-ttu-id="44017-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44017-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44017-p101">���� ��������� ��������� ��������� ��������� ���������� ������ �� ������ � ������� �������� ��������, ���������� ���������� � ��������� ����� MAPI ����� ���������� ��������� ��������� ��������. � ��������� ������� ������ ��� ���������� ��� ��������� ������������� ������������� � ��������� ����� MAPI ����� ���������� ���������� ���� � �������� ��������� ���������� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="44017-p101">If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things. Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.</span></span>
  
<span data-ttu-id="44017-p102">��� ������ �������� ��������� ������ ��� ������, ����� ���� ���������. ���� ��� ���, ��������� �������� ��������� �� ������ ������������ ���������� ����������� ������� ������. ��� �� ����� ���� ����������� ��������� ��������� ������ ���� �������� ������ ��� ������, � ����� ������ ������������ � ���������������� ������� ������������� ��� �����, ��� ����� ���������� ��� ��������� ���������� ����������� �������.</span><span class="sxs-lookup"><span data-stu-id="44017-p102">For many read-only message stores, that may not be a problem. If that is the case, the message store provider does not need to support associated contents tables at all. However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.</span></span>
  
<span data-ttu-id="44017-p103">�������� ���������������� ��������� ��� �����, ��� ��� ������� � ��������� ����� MAPI �� ����� ���������� ������������� ��� ���� � ��������� ��������, ������������ ��� ���������� ��������� ��������� � ���� �� � ��������� ���������. ��� ��������, ��� ��������� ���������� ������� ��� ������, ������� �������� ������������� ��� ����� ����� �������������� � ��������� ��������� ��� ��� ��������, ������ ��� ��������� ��� MAPI ��������� ����-���� �������� � ���� ������. ����� ����� ������ ����������� ������� ��������� ���������� ��� ��������� ������������� ������������� � ������ ��� ��������� ����� MAPI ����������� ������� ���������� ����������� ��� ������� �����, ��������� �������� ��������� ��������������.</span><span class="sxs-lookup"><span data-stu-id="44017-p103">The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store. This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it. Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one.</span></span> 
  
<span data-ttu-id="44017-p104">��� ����������, ��� � �������� ��������� ���������� ���� ������� � ��������� ��� �������� ������ ��������� ��������� ������������, ��� ��������� ��������� ��������� ������ �������� �������� � ������� ����������� ���������, ��� ������� � MAPI ����� ������������� ���������� ��� ��������, ������������� � �����. ������ ��� ������� ����� �������� �� ������� � ��������� ����� MAPI ������������, ������� �� ����� ���� ������������� ����� �������� ��.</span><span class="sxs-lookup"><span data-stu-id="44017-p104">This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms. What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="44017-115">��. �����</span><span class="sxs-lookup"><span data-stu-id="44017-115">See also</span></span>



[<span data-ttu-id="44017-116">������ ��� ������ �������� ���������</span><span class="sxs-lookup"><span data-stu-id="44017-116">Read-Only Message Stores</span></span>](read-only-message-stores.md)

