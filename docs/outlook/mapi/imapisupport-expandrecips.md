---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411248"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="8c4b2-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="8c4b2-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="8c4b2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c4b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c4b2-105">Завершает список получателей сообщения, расширяя определенные списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8c4b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c4b2-106">Parameters</span></span>

 <span data-ttu-id="8c4b2-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="8c4b2-107">_lpMessage_</span></span>
  
> <span data-ttu-id="8c4b2-108">[in] Указатель на сообщение, для обработки в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="8c4b2-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8c4b2-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="8c4b2-110">[out] Указатель на битовуюmask флагов, которая управляет типом обработки, которая происходит.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="8c4b2-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="8c4b2-111">The following flags can be set:</span></span>
    
<span data-ttu-id="8c4b2-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="8c4b2-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="8c4b2-113">Перед его отправлением сообщение должно быть предварительно разобрано.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="8c4b2-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="8c4b2-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="8c4b2-115">Сообщение должно отправляться пулом MAPI (а не поставщиком транспорта, к которому тесно совмещение вызываемой службы).</span><span class="sxs-lookup"><span data-stu-id="8c4b2-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8c4b2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c4b2-116">Return value</span></span>

<span data-ttu-id="8c4b2-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="8c4b2-117">S_OK</span></span> 
  
> <span data-ttu-id="8c4b2-118">Список получателей сообщения успешно обработан.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c4b2-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c4b2-119">Remarks</span></span>

<span data-ttu-id="8c4b2-120">Метод **IMAPISupport::ExpandRecips** реализован для объектов поддержки поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="8c4b2-121">Поставщики store сообщений **звонят в ExpandRecips,** чтобы отправить запрос MAPI на выполнение следующих задач:</span><span class="sxs-lookup"><span data-stu-id="8c4b2-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="8c4b2-122">Разорите некоторые личные списки рассылки до получателей компонентов.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="8c4b2-123">Замените все отображаемые имена, которые были изменены, на исходные имена.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="8c4b2-124">Пометить все повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="8c4b2-125">Разрешите все одновключные адреса.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="8c4b2-126">Проверьте, требуется ли предварительной подготовке сообщения, и, если да, установите для флага, на который указывает  _lpulFlags,_ значение NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="8c4b2-127">**ExpandRecips** расширяет все списки рассылки с типом адреса обмена сообщениями MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8c4b2-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8c4b2-128">Notes to callers</span></span>

<span data-ttu-id="8c4b2-129">Всегда **вызывайте ExpandRecips** в рамках обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="8c4b2-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="8c4b2-130">Сделайте вызов **ExpandRecips** одним из первых вызовов в реализации метода [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="8c4b2-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c4b2-131">См. также</span><span class="sxs-lookup"><span data-stu-id="8c4b2-131">See also</span></span>



[<span data-ttu-id="8c4b2-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="8c4b2-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="8c4b2-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8c4b2-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

