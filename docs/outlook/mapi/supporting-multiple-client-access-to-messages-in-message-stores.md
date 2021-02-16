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
ms.openlocfilehash: 40bed9ccbe8073c8e9ea5176c9d4be8fe642b52d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439865"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a><span data-ttu-id="d2ab0-103">��������� ���������� ����������� ������� � ���������� � �������� ���������</span><span class="sxs-lookup"><span data-stu-id="d2ab0-103">Supporting Multiple Client Access to Messages in Message Stores</span></span>

  
  
<span data-ttu-id="d2ab0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2ab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2ab0-p101">���������� ����������� ��� ���������� ���������� ����������, ����� ������������ ������� ������� ���������. ��������� ��� ������������� ������� ��� ������������ ����� ������ ����������� ��������� ��������� �� �����. ��� �� ����� ���� ���������� ���������� ��������� ��������� � ��������� �� ���������, ���������� ���������, ������ ��������� ��������� �������:</span><span class="sxs-lookup"><span data-stu-id="d2ab0-p101">It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:</span></span>
  
- <span data-ttu-id="d2ab0-108">��������� ������ ����� ������ [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ���������� ������, ��� ���� �� ������ ������, ������������ �������� ���������.</span><span class="sxs-lookup"><span data-stu-id="d2ab0-108">Allow the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to proceed as if it were the only client that has the message open.</span></span> 
    
- <span data-ttu-id="d2ab0-109">�� ����������� **SaveChanges** ������ � ������ ���������� ���������� ���������� ��������� ��������� ������� �������� ��������� � ������� MAPI_E_OBJECT_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="d2ab0-109">On the subsequent **SaveChanges** calls by other clients, the message store provider should ignore the changes and return MAPI_E_OBJECT_CHANGED.</span></span> 
    
- <span data-ttu-id="d2ab0-p102">��������� ���������� ����������� ����������� �� ��� �������� MAPI_E_OBJECT_CHANGED ����� ������ **SaveChanges** ��� ��� � ������ FORCE_SAVE. ���� ���������� ���������� ������ ���, ��������� �������� ��������� ���������� �������� ���������� ��������� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="d2ab0-p102">Allow client applications to respond to a MAPI_E_OBJECT_CHANGED return code by calling **SaveChanges** again with the FORCE_SAVE flag. If a client application does this, the message store provider should replace the previous changes with the new ones.</span></span> 
    
<span data-ttu-id="d2ab0-112">����� ���� ��������� �������� ��������� ����� ������������ �������� � ����������� ���������, ������� ��������� ������������ ��������, ������� �� ������� �������� ���������, ���������� ��������� ��������� � ������ ����������� ��� ��������� ��������� � ������ �����.</span><span class="sxs-lookup"><span data-stu-id="d2ab0-112">Alternatively, the message store provider can detect the conflict and present an interface that enables the user to choose whether to keep the original message, overwrite the original message with the new changes, or save the new changes to another location.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2ab0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d2ab0-113">See also</span></span>



[<span data-ttu-id="d2ab0-114">Включение сообщений в хранилищах сообщений</span><span class="sxs-lookup"><span data-stu-id="d2ab0-114">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

