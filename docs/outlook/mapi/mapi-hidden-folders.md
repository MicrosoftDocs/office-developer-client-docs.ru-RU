---
title: ����� MAPI �������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 70aeda8789665a3f35bf75f83f32a92dbeedc8de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589107"
---
# <a name="mapi-hidden-folders"></a><span data-ttu-id="06027-103">����� MAPI �������</span><span class="sxs-lookup"><span data-stu-id="06027-103">MAPI Hidden Folders</span></span>

  
  
<span data-ttu-id="06027-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06027-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06027-p101">������� ����� � ������������� ����������� �������� � �������� ����� ��������� ���������, � �� � �������� �������� ��������� ����������� ����� � ��� ��������� (IPM). ��� ��� ��� �� ����������� � ��������� IPM, ��� ������ ������ �� ������������ ����������� ��������� ���������. ������� ����� ������ �������� ��������, ����������� � ��������� ���������, �� ����� �������� ��� ������������. ������� ��������� ������� ����� ��� ��������, ��������, �������������� �������� ����� ����������� � ��������� ������ �������� �����.</span><span class="sxs-lookup"><span data-stu-id="06027-p101">Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree. Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider. Hidden folders typically contain information that is relevant to the message store but irrelevant to the user. Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.</span></span>
  
<span data-ttu-id="06027-p102">MAPI ������������, ��� ��� ������� ������ ����� ����������� �����������, ��������, ��������� � �������� ����� � ��������� IPM. ��������� �� ������ � ������� � ������ ��������� ��������� �������������. ��� �� ����� ��� ��������� ���������, ������� ����� ������������ � �������� ��������� �� ��������� �, ������� ����� ���������� � �������� ��������� ��������� ������ ������������ ������� �����.</span><span class="sxs-lookup"><span data-stu-id="06027-p102">MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree. Support for working with folders in other trees is considered optional. However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06027-112">��. �����</span><span class="sxs-lookup"><span data-stu-id="06027-112">See also</span></span>



[<span data-ttu-id="06027-113">����� MAPI</span><span class="sxs-lookup"><span data-stu-id="06027-113">MAPI Folders</span></span>](mapi-folders.md)

