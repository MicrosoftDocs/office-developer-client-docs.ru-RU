---
title: имаписуппортекспандреЦипс
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
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="e6d71-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="e6d71-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="e6d71-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6d71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6d71-105">Завершает список получателей сообщения, развертывая определенные списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="e6d71-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e6d71-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6d71-106">Parameters</span></span>

 <span data-ttu-id="e6d71-107">_лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="e6d71-107">_lpMessage_</span></span>
  
> <span data-ttu-id="e6d71-108">возврата Указатель на сообщение, для которого будет обрабатываться список получателей.</span><span class="sxs-lookup"><span data-stu-id="e6d71-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="e6d71-109">_лпулфлагс_</span><span class="sxs-lookup"><span data-stu-id="e6d71-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="e6d71-110">вышли Указатель на битовую маску флагов, определяющих тип выполняемой обработки.</span><span class="sxs-lookup"><span data-stu-id="e6d71-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="e6d71-111">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e6d71-111">The following flags can be set:</span></span>
    
<span data-ttu-id="e6d71-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="e6d71-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="e6d71-113">Перед отправкой сообщения необходимо предварительно обработать его.</span><span class="sxs-lookup"><span data-stu-id="e6d71-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="e6d71-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="e6d71-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="e6d71-115">Диспетчер очереди MAPI (вместо транспортного поставщика, которому вызывающий абонент тесно связан) должен отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="e6d71-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6d71-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6d71-116">Return value</span></span>

<span data-ttu-id="e6d71-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6d71-117">S_OK</span></span> 
  
> <span data-ttu-id="e6d71-118">Список получателей сообщения успешно обработан.</span><span class="sxs-lookup"><span data-stu-id="e6d71-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6d71-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6d71-119">Remarks</span></span>

<span data-ttu-id="e6d71-120">Метод **имаписуппорт:: експандреЦипс** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e6d71-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="e6d71-121">Поставщики хранилищ сообщений вызывают **експандреЦипс** , чтобы запросить MAPI для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="e6d71-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="e6d71-122">Разворачивание определенных личных списков рассылки для получателей их компонентов.</span><span class="sxs-lookup"><span data-stu-id="e6d71-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="e6d71-123">Замените все отображаемые имена, которые были изменены исходными именами.</span><span class="sxs-lookup"><span data-stu-id="e6d71-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="e6d71-124">Пометьте все повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="e6d71-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="e6d71-125">Разрешите все одноразовые адреса.</span><span class="sxs-lookup"><span data-stu-id="e6d71-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="e6d71-126">Убедитесь, что для сообщения требуется предварительная обработка, и, если это так, установите флаг, указывающий на _лпулфлагс_ , на NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="e6d71-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="e6d71-127">**ЕкспандреЦипс** развертывает все списки рассылки, которые имеют тип адреса обмена сообщениями мапипдл.</span><span class="sxs-lookup"><span data-stu-id="e6d71-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6d71-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e6d71-128">Notes to callers</span></span>

<span data-ttu-id="e6d71-129">Всегда вызывайте **експандреЦипс** в процессе обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6d71-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="e6d71-130">Выполните вызов **експандреЦипс** одного из первых вызовов в реализации метода [iMessage:: субмитмессаже](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="e6d71-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6d71-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e6d71-131">See also</span></span>



[<span data-ttu-id="e6d71-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="e6d71-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="e6d71-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6d71-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

