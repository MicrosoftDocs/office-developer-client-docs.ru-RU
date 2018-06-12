---
title: IMAPIMessageSiteSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 694ee8b12b9918502e60c0c6ea92992cc1062945
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808983"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="f7afa-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="f7afa-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="f7afa-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7afa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7afa-105">Запросы в текущем сообщении очереди для доставки.</span><span class="sxs-lookup"><span data-stu-id="f7afa-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f7afa-106">���������</span><span class="sxs-lookup"><span data-stu-id="f7afa-106">Parameters</span></span>

 <span data-ttu-id="f7afa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7afa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f7afa-108">[in] Битовая маска флаги, который определяет, как отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="f7afa-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="f7afa-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f7afa-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f7afa-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="f7afa-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="f7afa-111">MAPI следует отправить сообщение даже в том случае, если не могут отправляться немедленно.</span><span class="sxs-lookup"><span data-stu-id="f7afa-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7afa-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f7afa-112">Return value</span></span>

<span data-ttu-id="f7afa-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f7afa-113">S_OK</span></span> 
  
> <span data-ttu-id="f7afa-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f7afa-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7afa-115">���������</span><span class="sxs-lookup"><span data-stu-id="f7afa-115">Remarks</span></span>

<span data-ttu-id="f7afa-116">Объекты формы вызовите метод **IMAPIMessageSite::SubmitMessage** для запроса, что сообщение добавляемых в очередь для доставки.</span><span class="sxs-lookup"><span data-stu-id="f7afa-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="f7afa-117">На сайте сообщения должны вызвать метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="f7afa-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="f7afa-118">Сообщение не требуется быть сохранен ранее, так как **SubmitMessage** необходимо вызвать сообщение сохраняется, если сообщение было изменено.</span><span class="sxs-lookup"><span data-stu-id="f7afa-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="f7afa-119">После возврата **SubmitMessage**формы необходимо проверить для текущего сообщения и затем закрыть самого, если не существует.</span><span class="sxs-lookup"><span data-stu-id="f7afa-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="f7afa-120">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f7afa-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f7afa-121">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f7afa-121">MFCMAPI reference</span></span>

<span data-ttu-id="f7afa-122">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f7afa-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f7afa-123">**����**</span><span class="sxs-lookup"><span data-stu-id="f7afa-123">**File**</span></span>|<span data-ttu-id="f7afa-124">**�������**</span><span class="sxs-lookup"><span data-stu-id="f7afa-124">**Function**</span></span>|<span data-ttu-id="f7afa-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f7afa-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f7afa-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="f7afa-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="f7afa-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="f7afa-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="f7afa-128">Mfcmapi (en) использует метод **IMAPIMessageSite::SubmitMessage** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="f7afa-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="f7afa-129">Во-первых он вызывает метод **IPersistMessage::HandsOffMessage** и вызывает **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="f7afa-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7afa-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f7afa-130">See also</span></span>



[<span data-ttu-id="f7afa-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="f7afa-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="f7afa-132">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7afa-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="f7afa-133">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f7afa-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f7afa-134">Интерфейсы формы MAPI</span><span class="sxs-lookup"><span data-stu-id="f7afa-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

