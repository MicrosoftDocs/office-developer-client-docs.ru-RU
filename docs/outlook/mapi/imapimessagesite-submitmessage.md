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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417030"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="0764b-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0764b-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="0764b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0764b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0764b-105">Запрашивает, чтобы текущее сообщение было в очереди для доставки.</span><span class="sxs-lookup"><span data-stu-id="0764b-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0764b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0764b-106">Parameters</span></span>

 <span data-ttu-id="0764b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0764b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0764b-108">[in] Битоваяmas флагов, которая управляет отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="0764b-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="0764b-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0764b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0764b-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="0764b-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="0764b-111">MAPI должен отправить сообщение, даже если оно может быть отправлено не сразу.</span><span class="sxs-lookup"><span data-stu-id="0764b-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0764b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0764b-112">Return value</span></span>

<span data-ttu-id="0764b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0764b-113">S_OK</span></span> 
  
> <span data-ttu-id="0764b-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0764b-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0764b-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="0764b-115">Remarks</span></span>

<span data-ttu-id="0764b-116">Объекты форм вызовите метод **IMAPIMessageSite::SubmitMessage,** чтобы запросить доставку сообщения в очереди.</span><span class="sxs-lookup"><span data-stu-id="0764b-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="0764b-117">Перед отправкой сообщения сайт сообщения должен вызвать метод [IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md)</span><span class="sxs-lookup"><span data-stu-id="0764b-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="0764b-118">Сообщение не требуется ранее сохранено, так как **SubmitMessage** должен привести к его сэкономлению, если сообщение было изменено.</span><span class="sxs-lookup"><span data-stu-id="0764b-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="0764b-119">После возврата **SubmitMessage** форма должна проверить текущее сообщение и затем отклоняться, если нет.</span><span class="sxs-lookup"><span data-stu-id="0764b-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="0764b-120">Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="0764b-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0764b-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0764b-121">MFCMAPI reference</span></span>

<span data-ttu-id="0764b-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0764b-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0764b-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0764b-123">**File**</span></span>|<span data-ttu-id="0764b-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0764b-124">**Function**</span></span>|<span data-ttu-id="0764b-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0764b-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0764b-126">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="0764b-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="0764b-127">CMyMAPIFormViewer::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="0764b-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="0764b-128">MFCMAPI использует метод **IMAPIMessageSite::SubmitMessage** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="0764b-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="0764b-129">Сначала вызывается метод **IPersistMessage::HandsOffMessage,** а затем **— SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="0764b-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0764b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0764b-130">See also</span></span>



[<span data-ttu-id="0764b-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="0764b-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="0764b-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0764b-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="0764b-133">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="0764b-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0764b-134">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="0764b-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

