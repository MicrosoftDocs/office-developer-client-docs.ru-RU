---
title: ��������� ���������� ����������� ������� � ���������� � �������� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: f48fa1712b6e09e5a73f331228a811b4eb8d284d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812414"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="83f7b-103">��������� ���������� ����������� ������� � ���������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="83f7b-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="83f7b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83f7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83f7b-p101">���������� ����������� ��� ���������� ���������� ����������, ����� ������������ ������� ������� ���������. ��������� ��� ������������� ������� ��� ������������ ����� ������ ����������� ��������� ��������� �� �����. ��� �� ����� ���� ���������� ���������� ��������� ��������� � ��������� �� ���������, ���������� ���������, ������ ��������� ��������� �������:</span><span class="sxs-lookup"><span data-stu-id="83f7b-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="83f7b-108">��������� ������ ����� ������ [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ���������� ������, ��� ���� �� ������ ������, ������������ �������� ���������.</span><span class="sxs-lookup"><span data-stu-id="83f7b-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="83f7b-109">�� ����������� **SaveChanges** ������ � ������ ���������� ���������� ���������� ��������� ��������� ������� �������� ��������� � ������� MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="83f7b-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="83f7b-p102">��������� ���������� ����������� ����������� �� ��� �������� MAPI_E_OBJECT_CHANGED ����� ������ **SaveChanges** ��� ��� � ������ FORCE_SAVE. ���� ���������� ���������� ������ ���, ��������� �������� ��������� ���������� �������� ���������� ��������� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="83f7b-p102">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag. If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="83f7b-112">����� ���� ��������� �������� ��������� ����� ������������ �������� � ����������� ���������, ������� ��������� ������������ ��������, ������� �� ������� �������� ���������, ���������� ��������� ��������� � ������ ����������� ��� ��������� ��������� � ������ �����.</span><span class="sxs-lookup"><span data-stu-id="83f7b-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="83f7b-113">��. �����</span><span class="sxs-lookup"><span data-stu-id="83f7b-113">See also</span></span>



[<span data-ttu-id="83f7b-114">���������� ��������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="83f7b-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

