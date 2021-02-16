---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424457"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="921e2-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="921e2-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="921e2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="921e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="921e2-105">Копирует или перемещает одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="921e2-105">Copies or moves one or more messages.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="921e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="921e2-106">Parameters</span></span>

 <span data-ttu-id="921e2-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="921e2-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="921e2-108">[in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="921e2-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="921e2-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="921e2-109">_lpInterface_</span></span>
  
> <span data-ttu-id="921e2-110">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к папке назначения, на которую указывает параметр _lpDestFolder._</span><span class="sxs-lookup"><span data-stu-id="921e2-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="921e2-111">Передача NULL приводит к возвращению поставщиком службы стандартного интерфейса папки [IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="921e2-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="921e2-112">Клиенты должны передавать NULL.</span><span class="sxs-lookup"><span data-stu-id="921e2-112">Clients must pass NULL.</span></span> <span data-ttu-id="921e2-113">Другие вызыватели могут установить для  _параметра lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="921e2-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="921e2-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="921e2-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="921e2-115">[in] Указатель на открытую папку для получения скопированные или перемещенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="921e2-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="921e2-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="921e2-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="921e2-117">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span><span class="sxs-lookup"><span data-stu-id="921e2-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="921e2-118">Параметр _ulUIParam_ игнорируется, если клиент не устанавливает флаг MESSAGE_DIALOG в _параметре ulFlags_ и не передает NULL в _параметре lpProgress._</span><span class="sxs-lookup"><span data-stu-id="921e2-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="921e2-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="921e2-119">_lpProgress_</span></span>
  
> <span data-ttu-id="921e2-120">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="921e2-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="921e2-121">Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="921e2-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="921e2-122">Параметр _lpProgress_ игнорируется, если MESSAGE_DIALOG флага в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="921e2-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="921e2-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="921e2-123">_ulFlags_</span></span>
  
> <span data-ttu-id="921e2-124">[in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="921e2-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="921e2-125">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="921e2-125">The following flags can be set:</span></span>
    
<span data-ttu-id="921e2-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="921e2-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="921e2-127">Сообщает поставщику хранения сообщений о немедленном возвращении MAPI_E_DECLINE_COPY, если он реализует **метод IMAPIFolder::CopyMessages,** вызывая метод [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) или [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="921e2-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="921e2-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="921e2-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="921e2-129">Отображает индикатор хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="921e2-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="921e2-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="921e2-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="921e2-131">Вместо копирования сообщения или сообщения перемещаются.</span><span class="sxs-lookup"><span data-stu-id="921e2-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="921e2-132">Если MESSAGE_MOVE не установлен, сообщения копируется.</span><span class="sxs-lookup"><span data-stu-id="921e2-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="921e2-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="921e2-133">Return value</span></span>

<span data-ttu-id="921e2-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="921e2-134">S_OK</span></span> 
  
> <span data-ttu-id="921e2-135">Сообщения или сообщения успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="921e2-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="921e2-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="921e2-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="921e2-137">Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызываемая стороны передает флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="921e2-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="921e2-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="921e2-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="921e2-139">Вызов был успешным, но не все записи были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="921e2-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="921e2-140">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="921e2-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="921e2-141">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="921e2-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="921e2-142">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="921e2-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="921e2-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="921e2-143">Remarks</span></span>

<span data-ttu-id="921e2-144">Метод **IMAPIFolder::CopyMessages** копирует или перемещает сообщения в другую папку.</span><span class="sxs-lookup"><span data-stu-id="921e2-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="921e2-145">Сообщения, которые открываются с разрешением на чтение и записи, могут быть перемещены или скопированы.</span><span class="sxs-lookup"><span data-stu-id="921e2-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="921e2-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="921e2-146">Notes to implementers</span></span>

<span data-ttu-id="921e2-147">При копировании сообщений в другое хранилище сообщений без использования метода [IMAPISupport::CopyMessages](imapisupport-copymessages.md) необходимо сначала вызвать [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) с установленным флагом GENERATE_RECEIPT_ONLY.</span><span class="sxs-lookup"><span data-stu-id="921e2-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="921e2-148">Хранилище принимающих сообщений не отвечает за создание отчетов о прочтение скопированные или перемещенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="921e2-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="921e2-149">Если вы вызываете **IMAPISupport::CopyMessages** для реализации **IMAPIFolder::CopyMessages,** не **вызываем SetReadFlags;** MAPI будет вызывать его.</span><span class="sxs-lookup"><span data-stu-id="921e2-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="921e2-150">Реализация может перемещать или копировать сообщения в любом порядке и создавать отчеты о состоянии чтения в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="921e2-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="921e2-151">То есть вы можете завершить копирование сообщений перед созданием отчетов о состоянии чтения или отправить отчеты до того, как реализация начнет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="921e2-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="921e2-152">Однако для копирования всех сообщений следует отправлять отчеты о прочтеных сообщениях независимо от того, была ли копия успешной.</span><span class="sxs-lookup"><span data-stu-id="921e2-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="921e2-153">Если операция копирования или перемещения включает несколько сообщений, выполните операцию как можно точнее.</span><span class="sxs-lookup"><span data-stu-id="921e2-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="921e2-154">Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="921e2-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="921e2-155">Старайтесь поддерживать идентификаторы записей при операциях перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="921e2-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="921e2-156">Также следует сохранить идентификаторы записей, хотя это и не требуется.</span><span class="sxs-lookup"><span data-stu-id="921e2-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="921e2-157">Отправка уведомлений при перемещения или копировании сообщений таким образом, чтобы клиенты были предварительно уведомлены о том, что их вызовы методов [IMAPIProp::SaveChanges](imapiprop-savechanges.md) могут не удастся.</span><span class="sxs-lookup"><span data-stu-id="921e2-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="921e2-158">Не включаем состояние сообщения в операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="921e2-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="921e2-159">Перемещение или копирование состояния сообщения значительно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="921e2-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="921e2-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="921e2-160">Notes to callers</span></span>

<span data-ttu-id="921e2-161">Используйте **IMAPIFolder::CopyMessages** для заполнения папок результатов поиска, где сообщения часто группируют по родительской папке.</span><span class="sxs-lookup"><span data-stu-id="921e2-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="921e2-162">Эти возвращаемые значения следует ожидать при следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="921e2-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="921e2-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="921e2-163">**Condition**</span></span>|<span data-ttu-id="921e2-164">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="921e2-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="921e2-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span><span class="sxs-lookup"><span data-stu-id="921e2-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="921e2-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="921e2-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="921e2-167">**IMAPIFolder::CopyMessages** не удалось успешно скопировать или переместить каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="921e2-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="921e2-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="921e2-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="921e2-169">Не удалось завершить **IMAPIFolder::CopyMessages.**</span><span class="sxs-lookup"><span data-stu-id="921e2-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="921e2-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="921e2-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="921e2-171">Если **IMAPIFolder::CopyMessages** не удается завершить, не предполагать, что никаких работ не было сделано.</span><span class="sxs-lookup"><span data-stu-id="921e2-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="921e2-172">**Возможно, IMAPIFolder::CopyMessages** мог скопировать или переместить одно или несколько сообщений, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="921e2-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="921e2-173">См. также</span><span class="sxs-lookup"><span data-stu-id="921e2-173">See also</span></span>



[<span data-ttu-id="921e2-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="921e2-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

