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
ms.openlocfilehash: 22562e1177c9a649bc66b25b5e8e9e6ecc8e397c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812064"
---
# <a name="preprocessmessage"></a><span data-ttu-id="64d6d-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="64d6d-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="64d6d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64d6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64d6d-105">Определяет функцию, которая выполняет предварительную обработку содержимое сообщения или формат сообщения.</span><span class="sxs-lookup"><span data-stu-id="64d6d-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="64d6d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="64d6d-106">Header file:</span></span>  <br/> |<span data-ttu-id="64d6d-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="64d6d-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="64d6d-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="64d6d-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="64d6d-109">Поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="64d6d-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="64d6d-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="64d6d-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="64d6d-111">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="64d6d-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="64d6d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="64d6d-112">Parameters</span></span>

 <span data-ttu-id="64d6d-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="64d6d-113">_lpvSession_</span></span>
  
> <span data-ttu-id="64d6d-114">[in] Указатель для использования в сеансе.</span><span class="sxs-lookup"><span data-stu-id="64d6d-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="64d6d-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="64d6d-115">_lpMessage_</span></span>
  
> <span data-ttu-id="64d6d-116">[in] Указатель на сообщение, чтобы быть предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="64d6d-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="64d6d-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="64d6d-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="64d6d-118">[in] Указатель в адресную книгу, из которого пользователь должен выбрать получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="64d6d-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="64d6d-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="64d6d-119">_lpFolder_</span></span>
  
> <span data-ttu-id="64d6d-120">[in, out] Указатель на папку.</span><span class="sxs-lookup"><span data-stu-id="64d6d-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="64d6d-121">На входе параметр _lpFolder_ указывает на папку, содержащую сообщения, чтобы быть предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="64d6d-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="64d6d-122">На выходе _lpFolder_ указывает на папку, где размещен предварительной обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="64d6d-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="64d6d-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="64d6d-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="64d6d-124">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="64d6d-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="64d6d-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="64d6d-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="64d6d-126">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти там, где необходимо.</span><span class="sxs-lookup"><span data-stu-id="64d6d-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="64d6d-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="64d6d-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="64d6d-128">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="64d6d-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="64d6d-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="64d6d-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="64d6d-130">[out] Указатель на количество сообщений в массиве указывает параметр _lpppMessage_ .</span><span class="sxs-lookup"><span data-stu-id="64d6d-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="64d6d-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="64d6d-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="64d6d-132">[out] Указатель на указатель на массив указатели на предварительно или в противном случае создается сообщения.</span><span class="sxs-lookup"><span data-stu-id="64d6d-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="64d6d-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="64d6d-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="64d6d-134">[out] Указатель на необязательный возвращенные [ADRLIST](adrlist.md) структуру, список обнаруженных препроцессор получателей, для которых не удается доставить сообщение.</span><span class="sxs-lookup"><span data-stu-id="64d6d-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="64d6d-135">Дополнительные сведения о содержимом этого списка [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) см.</span><span class="sxs-lookup"><span data-stu-id="64d6d-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="64d6d-136">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="64d6d-136">Return value</span></span>

<span data-ttu-id="64d6d-137">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="64d6d-137">S_OK</span></span>
  
> <span data-ttu-id="64d6d-138">Содержимое сообщения были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="64d6d-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="64d6d-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="64d6d-139">Remarks</span></span>

<span data-ttu-id="64d6d-140">Препроцессор поставщика транспорта сообщений можно представить индикатор хода выполнения во время предварительной обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="64d6d-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="64d6d-141">Тем не менее он никогда не должно представлять диалоговое окно, требующее вмешательства пользователя во время предварительной обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="64d6d-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="64d6d-142">Когда препроцессор добавляет больших объемов данных в исходящее сообщение, рекомендуется придерживаться определенных процедур.</span><span class="sxs-lookup"><span data-stu-id="64d6d-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="64d6d-143">Этот тип сообщения могут храниться в хранилище сообщений на стороне сервера, вследствие чего препроцессор для доступа к удаленного хранилища продолжительное время.</span><span class="sxs-lookup"><span data-stu-id="64d6d-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="64d6d-144">Чтобы избежать этого, препроцессор должен иметь возможность, позволяющая его для хранения данных, который занимает большой объем пространства в хранилище локального сообщения и предоставить ссылку на этот локального хранилища в сообщении.</span><span class="sxs-lookup"><span data-stu-id="64d6d-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="64d6d-145">Не освобождать препроцессор какие-либо объекты, изначально переданных функции **PreprocessMessage** на основе.</span><span class="sxs-lookup"><span data-stu-id="64d6d-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="64d6d-146">Прежде чем диспетчер очереди MAPI можно вызвать функцию **PreprocessMessage** , поставщика транспорта необходимо зарегистрировать в вызове метода [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) функцию.</span><span class="sxs-lookup"><span data-stu-id="64d6d-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="64d6d-147">После вызова функции **PreprocessMessage** , диспетчер очереди не может продолжать работу отправки сообщения, пока не функция возвращает.</span><span class="sxs-lookup"><span data-stu-id="64d6d-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="64d6d-148">Диспетчер очереди MAPI несет ответственность за задачу отправка сообщений.</span><span class="sxs-lookup"><span data-stu-id="64d6d-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="64d6d-149">Это означает исходного сообщения никогда не переводится в массив указателей сообщение и вызвать методы **SubmitMessage** не требуется.</span><span class="sxs-lookup"><span data-stu-id="64d6d-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64d6d-150">См. также</span><span class="sxs-lookup"><span data-stu-id="64d6d-150">See also</span></span>



[<span data-ttu-id="64d6d-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="64d6d-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="64d6d-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="64d6d-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="64d6d-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="64d6d-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

