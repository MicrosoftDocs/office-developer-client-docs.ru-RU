---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437247"
---
# <a name="preprocessmessage"></a><span data-ttu-id="9d3d1-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="9d3d1-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="9d3d1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d3d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d3d1-105">Определяет функцию, которая предварительно обучает содержимое сообщения или его формат.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d3d1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9d3d1-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d3d1-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="9d3d1-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="9d3d1-108">Определяемая функция, реализованная в:</span><span class="sxs-lookup"><span data-stu-id="9d3d1-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="9d3d1-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="9d3d1-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="9d3d1-110">Определяемая функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="9d3d1-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="9d3d1-111">MapI spooler</span><span class="sxs-lookup"><span data-stu-id="9d3d1-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="9d3d1-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d3d1-112">Parameters</span></span>

 <span data-ttu-id="9d3d1-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-113">_lpvSession_</span></span>
  
> <span data-ttu-id="9d3d1-114">[in] Указатель на используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="9d3d1-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-115">_lpMessage_</span></span>
  
> <span data-ttu-id="9d3d1-116">[in] Указатель на сообщение для предварительной подготовки.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="9d3d1-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="9d3d1-118">[in] Указатель на адресную книгу, из которой пользователь должен выбрать получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="9d3d1-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-119">_lpFolder_</span></span>
  
> <span data-ttu-id="9d3d1-120">[in, out] Указатель на папку.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="9d3d1-121">При вводе  _параметр lpFolder_ указывает на папку, содержаную сообщения для предварительной подготовки.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="9d3d1-122">При выходе  _lpFolder_ указывает на папку, в которой были размещены предварительно пропроцессные сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="9d3d1-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="9d3d1-124">[in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="9d3d1-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="9d3d1-126">[in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая при необходимости используется для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="9d3d1-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="9d3d1-128">[in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="9d3d1-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="9d3d1-130">[out] Указатель на количество сообщений в массиве, на которое указывает параметр _lpppMessage._</span><span class="sxs-lookup"><span data-stu-id="9d3d1-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="9d3d1-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="9d3d1-132">[out] Указатель на указатель на массив указателей для предварительной подготовки или других сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="9d3d1-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="9d3d1-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="9d3d1-134">[out] Указатель на необязательные возвращаемые [структуры ADRLIST,](adrlist.md) перечисляя предварительно обнаруженных получателей, для которых сообщение не может быть недоставка.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="9d3d1-135">Дополнительные сведения о содержимом этого списка см. в методе [IMAPISupport::StatusRecips.](imapisupport-statusrecips.md)</span><span class="sxs-lookup"><span data-stu-id="9d3d1-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d3d1-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d3d1-136">Return value</span></span>

<span data-ttu-id="9d3d1-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d3d1-137">S_OK</span></span>
  
> <span data-ttu-id="9d3d1-138">Содержимое сообщений было успешно предварительно обоблюдно.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d3d1-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d3d1-139">Remarks</span></span>

<span data-ttu-id="9d3d1-140">Препроцессор сообщения поставщика транспорта может представить индикатор хода выполнения во время предварительной подготовки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="9d3d1-141">Однако в нем никогда не должно присутствовать диалоговое окно, требующее взаимодействия с пользователем во время предварительной подготовки сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="9d3d1-142">Если препроцессор добавляет большие объемы данных в исходящие сообщения, следует следовать определенным процедурам.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="9d3d1-143">Сообщения такого типа могут храниться в серверном хранилище сообщений, что приводит к отнимаемой времени процедуре, которая занимает много времени у препроцессора.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="9d3d1-144">Чтобы избежать этого, предпроцессор должен иметь возможность хранить данные, которые занимает большой объем места в локальном хранилище сообщений, и предоставлять ссылку на это локальное хранилище в сообщении.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="9d3d1-145">Препроцессор не должен освободить какие-либо объекты, изначально переданные функции на основе **PreprocessMessage.**</span><span class="sxs-lookup"><span data-stu-id="9d3d1-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="9d3d1-146">Прежде чем пулер MAPI может вызвать функцию **PreprocessMessage,** поставщик транспорта должен зарегистрировать эту функцию в вызове метода [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md)</span><span class="sxs-lookup"><span data-stu-id="9d3d1-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="9d3d1-147">После вызова **функции PreprocessMessage** пул не сможет продолжить отправку сообщения, пока функция не вернется.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="9d3d1-148">Задача отправки сообщений принадлежит пулу MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="9d3d1-149">Это означает, что исходное сообщение никогда не помещается в массив указателей сообщений, а вызов методов **SubmitMessage** никогда не требуется.</span><span class="sxs-lookup"><span data-stu-id="9d3d1-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d3d1-150">См. также</span><span class="sxs-lookup"><span data-stu-id="9d3d1-150">See also</span></span>



[<span data-ttu-id="9d3d1-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9d3d1-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="9d3d1-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9d3d1-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="9d3d1-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d3d1-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

