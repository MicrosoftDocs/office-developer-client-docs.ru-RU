---
title: имапифолдеркопимессажес
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
# <a name="imapifoldercopymessages"></a><span data-ttu-id="f2cf7-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="f2cf7-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="f2cf7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2cf7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2cf7-105">Копирует или перемещает одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f2cf7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2cf7-106">Parameters</span></span>

 <span data-ttu-id="f2cf7-107">_лпмсглист_</span><span class="sxs-lookup"><span data-stu-id="f2cf7-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="f2cf7-108">возврата Указатель на массив структур [ентрилист](entrylist.md) , идентифицирующий сообщение или сообщения, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="f2cf7-109">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="f2cf7-109">_lpInterface_</span></span>
  
> <span data-ttu-id="f2cf7-110">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к папке назначения, на которую указывает параметр _лпдестфолдер_ .</span><span class="sxs-lookup"><span data-stu-id="f2cf7-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="f2cf7-111">При передаче значения NULL поставщику услуг возвращается интерфейс стандартных папок, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="f2cf7-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="f2cf7-112">Клиенты должны передавать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-112">Clients must pass NULL.</span></span> <span data-ttu-id="f2cf7-113">Другие абоненты могут задать для параметра _лпинтерфаце_ значение IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="f2cf7-114">_лпдестфолдер_</span><span class="sxs-lookup"><span data-stu-id="f2cf7-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="f2cf7-115">возврата Указатель на открытую папку для получения скопированных или перемещенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="f2cf7-116">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="f2cf7-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="f2cf7-117">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="f2cf7-118">Параметр _улуипарам_ игнорируется, если клиент не устанавливает флаг MESSAGE_DIALOG в параметре _ulFlags_ и передает значение NULL в параметр _лппрогресс_ .</span><span class="sxs-lookup"><span data-stu-id="f2cf7-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="f2cf7-119">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="f2cf7-119">_lpProgress_</span></span>
  
> <span data-ttu-id="f2cf7-120">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f2cf7-121">Если в _лппрогресс_передается значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f2cf7-122">Параметр _лппрогресс_ игнорируется, если не установлен флаг MESSAGE_DIALOG в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="f2cf7-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f2cf7-123">_ulFlags_</span></span>
  
> <span data-ttu-id="f2cf7-124">возврата Битовая маска флагов, определяющих, как выполняется операция копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="f2cf7-125">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f2cf7-125">The following flags can be set:</span></span>
    
<span data-ttu-id="f2cf7-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="f2cf7-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="f2cf7-127">Информирует поставщика хранилища сообщений о немедленном возврате MAPI_E_DECLINE_COPY, если он реализует метод **IMAPIFolder:: копимессажес** , вызывая метод [Имаписуппорт::D окопито](imapisupport-docopyto.md) или [имаписуппорт::D окопипропс](imapisupport-docopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f2cf7-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="f2cf7-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f2cf7-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="f2cf7-129">Отображает индикатор хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="f2cf7-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="f2cf7-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="f2cf7-131">Вместо копирования необходимо переместить сообщение или сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="f2cf7-132">Если MESSAGE_MOVE не заданы, сообщения копируются.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2cf7-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2cf7-133">Return value</span></span>

<span data-ttu-id="f2cf7-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2cf7-134">S_OK</span></span> 
  
> <span data-ttu-id="f2cf7-135">Сообщение или сообщения были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="f2cf7-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="f2cf7-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="f2cf7-137">Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызывающий абонент передал флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="f2cf7-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f2cf7-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="f2cf7-139">Вызов выполнен успешно, но не все записи были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="f2cf7-140">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f2cf7-141">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="f2cf7-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f2cf7-142">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f2cf7-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2cf7-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2cf7-143">Remarks</span></span>

<span data-ttu-id="f2cf7-144">Метод **IMAPIFolder:: копимессажес** копирует или перемещает сообщения в другую папку.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="f2cf7-145">Сообщения, открытые с разрешением на чтение и запись, можно перемещать или копировать.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f2cf7-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f2cf7-146">Notes to implementers</span></span>

<span data-ttu-id="f2cf7-147">Если вы копируете сообщения в другое хранилище сообщений, не используя метод [имаписуппорт:: копимессажес](imapisupport-copymessages.md) , сначала необходимо вызвать [IMAPIFolder:: сетреадфлагс](imapifolder-setreadflags.md) с установленным флагом GENERATE_RECEIPT_ONLY.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="f2cf7-148">Принимающее хранилище сообщений не несет ответственности за создание отчетов о прочтении для скопированных или перемещенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="f2cf7-149">При вызове **имаписуппорт:: копимессажес** для реализации **IMAPIFolder:: копимессажес**, не вызывайте **сетреадфлагс**; Интерфейс MAPI выполнит его вызов.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="f2cf7-150">Ваша реализация может перемещать или копировать сообщения в любом порядке и создавать отчеты о состоянии чтения в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="f2cf7-151">То есть вы можете завершить копирование сообщений до создания любого из отчетов о состоянии чтения или отправить отчеты до того, как ваша реализация начнет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="f2cf7-152">Тем не менее, необходимо отправить отчеты о прочтении для всех сообщений, которые будут скопированы, независимо от того, успешно ли выполнено копирование.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="f2cf7-153">Если операция копирования или перемещения содержит более одного сообщения, выполните операцию как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="f2cf7-154">Не прекращайте выполнение операции преждевременно, если не произойдет сбой, который выходит за рамки элемента управления, например, не хватает памяти, не хватает места на диске или повреждено хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="f2cf7-155">Постарайтесь поддерживать идентификаторы записей в операциях перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="f2cf7-156">Кроме того, необходимо сохранить идентификаторы записей, хотя это необязательно.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="f2cf7-157">Отправлять уведомления при перемещении или копировании сообщений, чтобы клиенты фореварнед, что их вызовы к сообщениям " [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) " могут привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="f2cf7-158">Не включайте состояние сообщения в операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="f2cf7-159">Перемещение или копирование состояния сообщения существенно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f2cf7-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f2cf7-160">Notes to callers</span></span>

<span data-ttu-id="f2cf7-161">Используйте **IMAPIFolder:: копимессажес** для заполнения папок результатов поиска, где сообщения часто группируются по родительской папке.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="f2cf7-162">Эти возвращаемые значения следует ожидать при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="f2cf7-163">**Условие**</span><span class="sxs-lookup"><span data-stu-id="f2cf7-163">**Condition**</span></span>|<span data-ttu-id="f2cf7-164">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="f2cf7-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2cf7-165">**IMAPIFolder:: копимессажес** успешно копирует или перемещает каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="f2cf7-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2cf7-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="f2cf7-167">**IMAPIFolder:: копимессажес** не удалось успешно скопировать или переместить каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="f2cf7-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f2cf7-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="f2cf7-169">**IMAPIFolder:: копимессажес** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="f2cf7-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="f2cf7-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="f2cf7-171">Когда **IMAPIFolder:: копимессажес** не удается выполнить, не следует предполагать, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="f2cf7-172">**IMAPIFolder:: копимессажес** могли скопировать или переместить одно или несколько сообщений, прежде чем возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="f2cf7-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2cf7-173">См. также</span><span class="sxs-lookup"><span data-stu-id="f2cf7-173">See also</span></span>



[<span data-ttu-id="f2cf7-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f2cf7-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

