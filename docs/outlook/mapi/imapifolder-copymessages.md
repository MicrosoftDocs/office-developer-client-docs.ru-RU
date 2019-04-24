---
title: Имапифолдеркопимессажес
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280129"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="340f5-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="340f5-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="340f5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="340f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="340f5-105">Копирует или перемещает одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="340f5-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="340f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="340f5-106">Parameters</span></span>

 <span data-ttu-id="340f5-107">_Лпмсглист_</span><span class="sxs-lookup"><span data-stu-id="340f5-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="340f5-108">возврата Указатель на массив структур [ентрилист](entrylist.md) , идентифицирующий сообщение или сообщения, которые необходимо скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="340f5-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="340f5-109">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="340f5-109">_lpInterface_</span></span>
  
> <span data-ttu-id="340f5-110">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к папке назначения, на которую указывает параметр _лпдестфолдер_ .</span><span class="sxs-lookup"><span data-stu-id="340f5-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="340f5-111">При передаче значения NULL поставщику услуг возвращается интерфейс стандартных папок, [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="340f5-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="340f5-112">Клиенты должны передавать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="340f5-112">Clients must pass NULL.</span></span> <span data-ttu-id="340f5-113">Другие абоненты могут задать для параметра _лпинтерфаце_ значение Иид_иункновн, Иид_имапипроп, Иид_имапиконтаинер или иид_имапифолдер.</span><span class="sxs-lookup"><span data-stu-id="340f5-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="340f5-114">_Лпдестфолдер_</span><span class="sxs-lookup"><span data-stu-id="340f5-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="340f5-115">возврата Указатель на открытую папку для получения скопированных или перемещенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="340f5-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="340f5-116">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="340f5-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="340f5-117">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="340f5-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="340f5-118">Параметр _улуипарам_ игнорируется, если клиент не устанавливает флаг мессаже_диалог в параметре _ulFlags_ и не передает значение NULL в параметре _лппрогресс_ .</span><span class="sxs-lookup"><span data-stu-id="340f5-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="340f5-119">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="340f5-119">_lpProgress_</span></span>
  
> <span data-ttu-id="340f5-120">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="340f5-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="340f5-121">Если в _лппрогресс_переДАЕТСЯ значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="340f5-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="340f5-122">Параметр _лппрогресс_ игнорируется, если не установлен флаг Мессаже_диалог в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="340f5-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="340f5-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="340f5-123">_ulFlags_</span></span>
  
> <span data-ttu-id="340f5-124">возврата Битовая маска флагов, определяющих, как выполняется операция копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="340f5-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="340f5-125">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="340f5-125">The following flags can be set:</span></span>
    
<span data-ttu-id="340f5-126">МАПИ_ДЕКЛИНЕ_ОК</span><span class="sxs-lookup"><span data-stu-id="340f5-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="340f5-127">Информирует поставщика хранилища сообщений о том, что он немедленно возвращает МАПИ_Е_ДЕКЛИНЕ_КОПИ, если он реализует **IMAPIFolder:: копимессажес** , вызывая метод [Имаписуппорт::D окопито](imapisupport-docopyto.md) или [имаписуппорт::D окопипропс](imapisupport-docopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="340f5-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="340f5-128">МЕССАЖЕ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="340f5-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="340f5-129">Отображает индикатор хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="340f5-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="340f5-130">МЕССАЖЕ_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="340f5-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="340f5-131">Вместо копирования необходимо переместить сообщение или сообщения.</span><span class="sxs-lookup"><span data-stu-id="340f5-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="340f5-132">Если МЕССАЖЕ_МОВЕ не задано, сообщения копируются.</span><span class="sxs-lookup"><span data-stu-id="340f5-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="340f5-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="340f5-133">Return value</span></span>

<span data-ttu-id="340f5-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="340f5-134">S_OK</span></span> 
  
> <span data-ttu-id="340f5-135">Сообщение или сообщения были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="340f5-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="340f5-136">МАПИ_Е_ДЕКЛИНЕ_КОПИ</span><span class="sxs-lookup"><span data-stu-id="340f5-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="340f5-137">Поставщик реализует этот метод, вызывая метод объекта support, и вызывающий абонент передал флаг МАПИ_ДЕКЛИНЕ_ОК.</span><span class="sxs-lookup"><span data-stu-id="340f5-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="340f5-138">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="340f5-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="340f5-139">Вызов выполнен успешно, но не все записи были успешно скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="340f5-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="340f5-140">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="340f5-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="340f5-141">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="340f5-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="340f5-142">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="340f5-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="340f5-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="340f5-143">Remarks</span></span>

<span data-ttu-id="340f5-144">Метод **IMAPIFolder:: копимессажес** копирует или перемещает сообщения в другую папку.</span><span class="sxs-lookup"><span data-stu-id="340f5-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="340f5-145">Сообщения, открытые с разрешением на чтение и запись, можно перемещать или копировать.</span><span class="sxs-lookup"><span data-stu-id="340f5-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="340f5-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="340f5-146">Notes to implementers</span></span>

<span data-ttu-id="340f5-147">Если вы копируете сообщения в другое хранилище сообщений, не используя метод [имаписуппорт:: копимессажес](imapisupport-copymessages.md) , сначала необходимо вызвать [IMAPIFolder:: сетреадфлагс](imapifolder-setreadflags.md) с установленным флагом женерате_рецеипт_онли.</span><span class="sxs-lookup"><span data-stu-id="340f5-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="340f5-148">Принимающее хранилище сообщений не несет ответственности за создание отчетов о прочтении для скопированных или перемещенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="340f5-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="340f5-149">При вызове **имаписуппорт:: копимессажес** для реализации **IMAPIFolder:: копимессажес**, не вызывайте **сетреадфлагс**; ИНТЕРФЕЙС MAPI выполнит его вызов.</span><span class="sxs-lookup"><span data-stu-id="340f5-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="340f5-150">Ваша реализация может перемещать или копировать сообщения в любом порядке и создавать отчеты о состоянии чтения в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="340f5-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="340f5-151">То есть вы можете завершить копирование сообщений до создания любого из отчетов о состоянии чтения или отправить отчеты до того, как ваша реализация начнет операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="340f5-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="340f5-152">Тем не менее, необходимо отправить отчеты о прочтении для всех сообщений, которые будут скопированы, независимо от того, успешно ли выполнено копирование.</span><span class="sxs-lookup"><span data-stu-id="340f5-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="340f5-153">Если операция копирования или перемещения содержит более одного сообщения, выполните операцию как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="340f5-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="340f5-154">Не прекращайте выполнение операции преждевременно, если не произойдет сбой, который выходит за рамки элемента управления, например, не хватает памяти, не хватает места на диске или повреждено хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="340f5-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="340f5-155">ПоСтарайтесь поддерживать идентификаторы записей в операциях перемещения или копирования.</span><span class="sxs-lookup"><span data-stu-id="340f5-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="340f5-156">Кроме того, необходимо сохранить идентификаторы записей, хотя это необязательно.</span><span class="sxs-lookup"><span data-stu-id="340f5-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="340f5-157">Отправлять уведомления при перемещении или копировании сообщений, чтобы клиенты фореварнед, что их вызовы к сообщениям " [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) " могут привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="340f5-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="340f5-158">Не включайте состояние сообщения в операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="340f5-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="340f5-159">Перемещение или копирование состояния сообщения существенно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="340f5-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="340f5-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="340f5-160">Notes to callers</span></span>

<span data-ttu-id="340f5-161">Используйте **IMAPIFolder:: копимессажес** для заполнения папок результатов поиска, где сообщения часто группируются по родительской папке.</span><span class="sxs-lookup"><span data-stu-id="340f5-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="340f5-162">Эти возвращаемые значения следует ожидать при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="340f5-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="340f5-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="340f5-163">**Condition**</span></span>|<span data-ttu-id="340f5-164">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="340f5-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="340f5-165">**IMAPIFolder:: копимессажес** успешно копирует или перемещает каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="340f5-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="340f5-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="340f5-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="340f5-167">**IMAPIFolder:: копимессажес** не удалось успешно скопировать или переместить каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="340f5-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="340f5-168">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="340f5-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="340f5-169">**IMAPIFolder:: копимессажес** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="340f5-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="340f5-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="340f5-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="340f5-171">Когда **IMAPIFolder:: копимессажес** не удается выполнить, не следует предполагать, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="340f5-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="340f5-172">**IMAPIFolder:: копимессажес** могли скопировать или переместить одно или несколько сообщений, прежде чем возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="340f5-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="340f5-173">См. также</span><span class="sxs-lookup"><span data-stu-id="340f5-173">See also</span></span>



[<span data-ttu-id="340f5-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="340f5-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

