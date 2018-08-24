---
title: �������� ��������� �� ���������
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576913"
---
# <a name="default-message-stores"></a><span data-ttu-id="4c69d-103">�������� ��������� �� ���������</span><span class="sxs-lookup"><span data-stu-id="4c69d-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="4c69d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c69d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c69d-p101">��������� ��������� �� ��������� � ��� ��������, ���������� ���������� ����� ������������ ��� ������ ����������, ������ ������� ������ �����������. ���������� ��������� �������������� ������� ��� ����������� ��������� ���������, ������� ���������� �������������, ���� ��������� �������� ��������� ��� ������������� � �������� ��������� ��������� �� ���������. ��� �������� ��������� �������:</span><span class="sxs-lookup"><span data-stu-id="4c69d-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="4c69d-108">���������� ����������� �����: ����� "��������", "���������" � ����������� ������.</span><span class="sxs-lookup"><span data-stu-id="4c69d-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="4c69d-109">�������������� ������ � nonread �������.</span><span class="sxs-lookup"><span data-stu-id="4c69d-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="4c69d-110">���������� �������� � ��������� ���������, ������������.</span><span class="sxs-lookup"><span data-stu-id="4c69d-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="4c69d-111">���������� �� �������� ��������� � ������� ������� ������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="4c69d-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="4c69d-112">��������� ����������� � ��������� �������� �������.</span><span class="sxs-lookup"><span data-stu-id="4c69d-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="4c69d-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span><span class="sxs-lookup"><span data-stu-id="4c69d-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="4c69d-p102">Supporting associated contents tables. For more information, see [���������� �������](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4c69d-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="4c69d-116">��������� ����������� �� ������� MAPI, ����� ��������� � ������� ��������� ���������.</span><span class="sxs-lookup"><span data-stu-id="4c69d-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4c69d-117">��. �����</span><span class="sxs-lookup"><span data-stu-id="4c69d-117">See also</span></span>



[<span data-ttu-id="4c69d-118">���������� ���������� ��������� ��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="4c69d-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

