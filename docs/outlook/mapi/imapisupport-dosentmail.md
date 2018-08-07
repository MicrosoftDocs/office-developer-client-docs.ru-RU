---
title: IMAPISupportDoSentMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoSentMail
api_type:
- COM
ms.assetid: 4bb65c2a-9926-42da-9161-47836e8de40a
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 2bded946a1fc7d7ab181d3953defa24e247c003c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809133"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="4ad31-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="4ad31-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="4ad31-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ad31-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ad31-105">������������ ������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="4ad31-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="4ad31-106">���������</span><span class="sxs-lookup"><span data-stu-id="4ad31-106">Parameters</span></span>

 <span data-ttu-id="4ad31-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ad31-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4ad31-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="4ad31-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4ad31-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="4ad31-109">_lpMessage_</span></span>
  
> <span data-ttu-id="4ad31-110">[in] ��������� �� ��������� ���������, ��� �������� ����� ������ ��������� � �����, ��������������� ��� �������� ������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="4ad31-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ad31-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4ad31-111">Return value</span></span>

<span data-ttu-id="4ad31-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4ad31-112">S_OK</span></span> 
  
> <span data-ttu-id="4ad31-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4ad31-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ad31-114">���������</span><span class="sxs-lookup"><span data-stu-id="4ad31-114">Remarks</span></span>

<span data-ttu-id="4ad31-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="4ad31-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="4ad31-118">**DoSentMail** ��������� ��������� ������:</span><span class="sxs-lookup"><span data-stu-id="4ad31-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="4ad31-119">Проверяет сообщения для свойства **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)), чтобы определить, нужно ли удалять после отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ad31-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="4ad31-120">���������� ������������ ����� �������������.</span><span class="sxs-lookup"><span data-stu-id="4ad31-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="4ad31-121">���������� ��������� ��� ������ ����������� ������� ��� �����, ������������ ���������� ���������.</span><span class="sxs-lookup"><span data-stu-id="4ad31-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="4ad31-122">���������� ��������� � ����� "������������", ����� "���������", ��� � ������ �����.</span><span class="sxs-lookup"><span data-stu-id="4ad31-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="4ad31-123">����������� ���������.</span><span class="sxs-lookup"><span data-stu-id="4ad31-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ad31-124">��. �����</span><span class="sxs-lookup"><span data-stu-id="4ad31-124">See also</span></span>



[<span data-ttu-id="4ad31-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="4ad31-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="4ad31-126">������������ �������� PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="4ad31-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="4ad31-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4ad31-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

