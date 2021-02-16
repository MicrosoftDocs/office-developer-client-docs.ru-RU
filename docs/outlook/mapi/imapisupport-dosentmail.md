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
ms.openlocfilehash: 8289b8dd2e0ab3c760e77a37b821d2fe74e4abe9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423953"
---
# <a name="imapisupportdosentmail"></a><span data-ttu-id="08109-103">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="08109-103">IMAPISupport::DoSentMail</span></span>

  
  
<span data-ttu-id="08109-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08109-105">������������ ������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="08109-105">Processes a sent message.</span></span>
  
```cpp
HRESULT DoSentMail(
  ULONG ulFlags,
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="08109-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08109-106">Parameters</span></span>

 <span data-ttu-id="08109-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="08109-107">_ulFlags_</span></span>
  
> <span data-ttu-id="08109-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="08109-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="08109-109">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="08109-109">_lpMessage_</span></span>
  
> <span data-ttu-id="08109-110">[in] ��������� �� ��������� ���������, ��� �������� ����� ������ ��������� � �����, ��������������� ��� �������� ������������ ���������.</span><span class="sxs-lookup"><span data-stu-id="08109-110">[in] A pointer to the open message for which a message should be generated in the folder designated to hold sent items.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="08109-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08109-111">Return value</span></span>

<span data-ttu-id="08109-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="08109-112">S_OK</span></span> 
  
> <span data-ttu-id="08109-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="08109-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08109-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="08109-114">Remarks</span></span>

<span data-ttu-id="08109-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span><span class="sxs-lookup"><span data-stu-id="08109-p101">The **IMAPISupport::DoSentMail** method is implemented for message store provider support objects. Message store providers call **DoSentMail** from their implementation of the [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method, which is called by the MAPI spooler when it has finished processing a message. **FinishedMsg** unlocks the message, ensures that the message's reference count is 1, and calls **DoSentMail**.</span></span>
  
 <span data-ttu-id="08109-118">**DoSentMail** ��������� ��������� ������:</span><span class="sxs-lookup"><span data-stu-id="08109-118">**DoSentMail** performs the following tasks:</span></span> 
  
- <span data-ttu-id="08109-119">Проверяет сообщение на наличие **свойства PR_DELETE_AFTER_SUBMIT** [(PidTagDeleteAfterSubmit),](pidtagdeleteaftersubmit-canonical-property.md)чтобы определить, следует ли удалять сообщение после отправки.</span><span class="sxs-lookup"><span data-stu-id="08109-119">Checks the message for the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to determine whether the message should be deleted after sending.</span></span>
    
- <span data-ttu-id="08109-120">���������� ������������ ����� �������������.</span><span class="sxs-lookup"><span data-stu-id="08109-120">Determines the location of the Sent Items folder.</span></span>
    
- <span data-ttu-id="08109-121">���������� ��������� ��� ������ ����������� ������� ��� �����, ������������ ���������� ���������.</span><span class="sxs-lookup"><span data-stu-id="08109-121">Initiates message hook processing for any hooks set on the Sent Items folder.</span></span>
    
- <span data-ttu-id="08109-122">���������� ��������� � ����� "������������", ����� "���������", ��� � ������ �����.</span><span class="sxs-lookup"><span data-stu-id="08109-122">Moves the message to the Sent Items folder, Deleted Items folder, or to another folder.</span></span>
    
- <span data-ttu-id="08109-123">����������� ���������.</span><span class="sxs-lookup"><span data-stu-id="08109-123">Releases the message.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08109-124">См. также</span><span class="sxs-lookup"><span data-stu-id="08109-124">See also</span></span>



[<span data-ttu-id="08109-125">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="08109-125">IMsgStore::FinishedMsg</span></span>](imsgstore-finishedmsg.md)
  
[<span data-ttu-id="08109-126">������������ �������� PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="08109-126">PidTagDeleteAfterSubmit Canonical Property</span></span>](pidtagdeleteaftersubmit-canonical-property.md)
  
[<span data-ttu-id="08109-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="08109-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

