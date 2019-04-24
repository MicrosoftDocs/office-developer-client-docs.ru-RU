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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351382"
---
# <a name="preprocessmessage"></a><span data-ttu-id="4e584-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="4e584-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="4e584-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e584-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e584-105">Определяет функцию, которая предварительно обрабатывает содержимое сообщения или формат сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e584-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e584-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4e584-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e584-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="4e584-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="4e584-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4e584-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4e584-109">Поставщики транспорта</span><span class="sxs-lookup"><span data-stu-id="4e584-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="4e584-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="4e584-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4e584-111">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="4e584-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4e584-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e584-112">Parameters</span></span>

 <span data-ttu-id="4e584-113">_Лпвсессион_</span><span class="sxs-lookup"><span data-stu-id="4e584-113">_lpvSession_</span></span>
  
> <span data-ttu-id="4e584-114">возврата Указатель на сеанс, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="4e584-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="4e584-115">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="4e584-115">_lpMessage_</span></span>
  
> <span data-ttu-id="4e584-116">возврата Указатель на сообщение, которое необходимо обработать.</span><span class="sxs-lookup"><span data-stu-id="4e584-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="4e584-117">_Лпадрбук_</span><span class="sxs-lookup"><span data-stu-id="4e584-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="4e584-118">возврата Указатель на адресную книгу, из которой пользователь должен выбрать получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e584-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="4e584-119">_Лпфолдер_</span><span class="sxs-lookup"><span data-stu-id="4e584-119">_lpFolder_</span></span>
  
> <span data-ttu-id="4e584-120">[вход, выход] Указатель на папку.</span><span class="sxs-lookup"><span data-stu-id="4e584-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="4e584-121">Во входных данных параметр _лпфолдер_ указывает на папку, в которой содержатся сообщения, которые должны быть предварительно обработаны.</span><span class="sxs-lookup"><span data-stu-id="4e584-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="4e584-122">В выходных данных _лпфолдер_ указывает папку, в которой были размещены предварительно обработанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e584-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="4e584-123">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="4e584-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4e584-124">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="4e584-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="4e584-125">_Лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="4e584-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="4e584-126">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти там, где это необходимо.</span><span class="sxs-lookup"><span data-stu-id="4e584-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="4e584-127">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="4e584-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4e584-128">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="4e584-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="4e584-129">_Лпкаутбаунд_</span><span class="sxs-lookup"><span data-stu-id="4e584-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="4e584-130">вышли Указатель на число сообщений в массиве, на которое указывает параметр _лпппмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="4e584-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="4e584-131">_Лпппмессаже_</span><span class="sxs-lookup"><span data-stu-id="4e584-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="4e584-132">вышли Указатель на указатель на массив указателей, которые должны быть предварительно обработаны или были созданы другими сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4e584-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="4e584-133">_ЛппреЦиплист_</span><span class="sxs-lookup"><span data-stu-id="4e584-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="4e584-134">вышли Указатель на необязательную возвращенную структуру [ADRLIST](adrlist.md) , в которой перечисляются необнаруженные получатели, для которых сообщение не может быть доставлено.</span><span class="sxs-lookup"><span data-stu-id="4e584-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="4e584-135">Для получения дополнительных сведений о содержимом этого списка см метод [имаписуппорт:: статусреЦипс](imapisupport-statusrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="4e584-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e584-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e584-136">Return value</span></span>

<span data-ttu-id="4e584-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e584-137">S_OK</span></span>
  
> <span data-ttu-id="4e584-138">Содержимое сообщения было успешно обработано.</span><span class="sxs-lookup"><span data-stu-id="4e584-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e584-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e584-139">Remarks</span></span>

<span data-ttu-id="4e584-140">Предварительная обработка сообщений транспортного поставщика может показывать во время предварительной обработки сообщения индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e584-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="4e584-141">Тем не менее, не должно отображаться диалоговое окно, требующее взаимодействия с пользователем во время предварительной обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e584-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="4e584-142">Когда препроцессор добавляет большие объемы данных в исходящее сообщение, необходимо выполнить определенные процедуры.</span><span class="sxs-lookup"><span data-stu-id="4e584-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="4e584-143">Этот тип сообщения может храниться в хранилище сообщений на сервере, что привело к тому, что препроцессор получает доступ к удаленному хранилищу, длительное время.</span><span class="sxs-lookup"><span data-stu-id="4e584-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="4e584-144">Чтобы избежать этого, у предварительной обработки должен быть параметр, позволяющий хранить данные, которые занимают большое количество места в локальном хранилище сообщений, и предоставлять ссылку на это локальное хранилище в сообщении.</span><span class="sxs-lookup"><span data-stu-id="4e584-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="4e584-145">Предварительная обработка не должна освобождать объекты, изначально переданные в функцию на основе **препроцессмессаже** .</span><span class="sxs-lookup"><span data-stu-id="4e584-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="4e584-146">Прежде чем диспетчер очереди MAPI сможет вызвать функцию **препроцессмессаже** , поставщик транспорта должен зарегистрировать функцию в вызове метода [Имаписуппорт:: регистерпрепроцессор](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="4e584-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="4e584-147">После вызова функции **препроцессмессаже** Диспетчер очереди не может продолжить отправку сообщения, пока функция не вернет значение.</span><span class="sxs-lookup"><span data-stu-id="4e584-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="4e584-148">Диспетчер очереди MAPI владеет задачей отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="4e584-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="4e584-149">Это означает, что исходное сообщение никогда не помещается в массив указателей сообщений и что вызов методов **субмитмессаже** не требуется.</span><span class="sxs-lookup"><span data-stu-id="4e584-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e584-150">См. также</span><span class="sxs-lookup"><span data-stu-id="4e584-150">See also</span></span>



[<span data-ttu-id="4e584-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4e584-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="4e584-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="4e584-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="4e584-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e584-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

