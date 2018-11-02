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
ms.openlocfilehash: 379fdc47f35fb183dd0bf551e421422abb106c0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591013"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="6c786-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="6c786-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="6c786-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c786-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c786-105">Завершает список получателей сообщения, возможность расширения списков рассылок определенного.</span><span class="sxs-lookup"><span data-stu-id="6c786-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6c786-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c786-106">Parameters</span></span>

 <span data-ttu-id="6c786-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="6c786-107">_lpMessage_</span></span>
  
> <span data-ttu-id="6c786-108">[in] Указатель на сообщение, содержащее список получателей для обработки.</span><span class="sxs-lookup"><span data-stu-id="6c786-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="6c786-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c786-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="6c786-110">[out] Указатель на битовую маску флагов, определяющее тип действия, выполняемые.</span><span class="sxs-lookup"><span data-stu-id="6c786-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="6c786-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="6c786-111">The following flags can be set:</span></span>
    
<span data-ttu-id="6c786-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="6c786-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="6c786-113">Должна быть предварительно перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="6c786-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="6c786-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="6c786-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="6c786-115">Диспетчер очереди MAPI (а не поставщика транспорта, к которому тесно связан вызывающего абонента) необходимо отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="6c786-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6c786-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c786-116">Return value</span></span>

<span data-ttu-id="6c786-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c786-117">S_OK</span></span> 
  
> <span data-ttu-id="6c786-118">Список получателей сообщения успешно обработан.</span><span class="sxs-lookup"><span data-stu-id="6c786-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c786-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c786-119">Remarks</span></span>

<span data-ttu-id="6c786-120">Метод **IMAPISupport::ExpandRecips** реализуется для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c786-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="6c786-121">Поставщики хранилища сообщений вызова **ExpandRecips** запроса MAPI для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="6c786-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="6c786-122">Разверните узел определенные списки рассылки их компонент получателям.</span><span class="sxs-lookup"><span data-stu-id="6c786-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="6c786-123">Замените все отображаемые имена, которые были изменены исходные имена.</span><span class="sxs-lookup"><span data-stu-id="6c786-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="6c786-124">Пометьте все дублированные записи.</span><span class="sxs-lookup"><span data-stu-id="6c786-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="6c786-125">Устраните все одноразовых адреса.</span><span class="sxs-lookup"><span data-stu-id="6c786-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="6c786-126">Проверьте ли сообщение должно предварительной обработки и если это так, необходимо задать флаг, на который указывает _lpulFlags_ для NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="6c786-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="6c786-127">**ExpandRecips** развертывание списков рассылки, обмена мгновенными сообщениями тип адреса MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="6c786-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6c786-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6c786-128">Notes to callers</span></span>

<span data-ttu-id="6c786-129">Всегда вызывайте **ExpandRecips** как часть вашей обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c786-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="6c786-130">Позвоните **ExpandRecips** один первого вызовов в реализации метода [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="6c786-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c786-131">См. также</span><span class="sxs-lookup"><span data-stu-id="6c786-131">See also</span></span>



[<span data-ttu-id="6c786-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="6c786-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="6c786-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c786-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

