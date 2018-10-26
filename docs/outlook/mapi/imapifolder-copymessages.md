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
ms.openlocfilehash: e253aa6a701d565fbc61e8a0e0a6388f7199c000
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593265"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="01f01-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="01f01-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="01f01-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01f01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01f01-105">Копирование или перемещение одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="01f01-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="01f01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01f01-106">Parameters</span></span>

 <span data-ttu-id="01f01-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="01f01-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="01f01-108">[in] Указатель на массив структур [ENTRYLIST](entrylist.md) , чтобы указать сообщения или сообщения, чтобы скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="01f01-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="01f01-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="01f01-109">_lpInterface_</span></span>
  
> <span data-ttu-id="01f01-110">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к папке назначения, на который указывает параметр _lpDestFolder_ .</span><span class="sxs-lookup"><span data-stu-id="01f01-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="01f01-111">Передача значение NULL, приводит к поставщика услуг, возврат интерфейсе стандартные папки [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="01f01-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="01f01-112">Клиенты необходимо передать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="01f01-112">Clients must pass NULL.</span></span> <span data-ttu-id="01f01-113">Другие абонентов можно включить параметр _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="01f01-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="01f01-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="01f01-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="01f01-115">[in] Указатель открыть папку для получения копируемые или перемещения сообщений.</span><span class="sxs-lookup"><span data-stu-id="01f01-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="01f01-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="01f01-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="01f01-117">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="01f01-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="01f01-118">Параметр _ulUIParam_ игнорируется, если клиент устанавливает флаг MESSAGE_DIALOG с помощью параметра _ulFlags_ и передает значение NULL в параметре _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="01f01-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="01f01-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="01f01-119">_lpProgress_</span></span>
  
> <span data-ttu-id="01f01-120">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="01f01-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="01f01-121">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="01f01-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="01f01-122">Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="01f01-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="01f01-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="01f01-123">_ulFlags_</span></span>
  
> <span data-ttu-id="01f01-124">[in] Битовая маска флаги, который определяет, как выполнить операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="01f01-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="01f01-125">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="01f01-125">The following flags can be set:</span></span>
    
<span data-ttu-id="01f01-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="01f01-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="01f01-127">Информирует поставщика хранилища сообщений сразу же возвращает MAPI_E_DECLINE_COPY, если он реализует **IMAPIFolder::CopyMessages** путем вызова метода [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) или [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) объект поддержки.</span><span class="sxs-lookup"><span data-stu-id="01f01-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="01f01-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="01f01-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="01f01-129">Отображает индикатор выполнения, как операция продолжается.</span><span class="sxs-lookup"><span data-stu-id="01f01-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="01f01-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="01f01-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="01f01-131">Сообщения или сообщения должны быть перемещены, а не копируются.</span><span class="sxs-lookup"><span data-stu-id="01f01-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="01f01-132">Если MESSAGE_MOVE не задано, копируются сообщения.</span><span class="sxs-lookup"><span data-stu-id="01f01-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01f01-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01f01-133">Return value</span></span>

<span data-ttu-id="01f01-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="01f01-134">S_OK</span></span> 
  
> <span data-ttu-id="01f01-135">Сообщения или сообщения были успешно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="01f01-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="01f01-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="01f01-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="01f01-137">Поставщик реализует этот метод, вызвав метод объекта поддержки и вызывающего абонента, истекло флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="01f01-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="01f01-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="01f01-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="01f01-139">Вызов завершился успешно, но не все записи были успешно скопировать или переместить.</span><span class="sxs-lookup"><span data-stu-id="01f01-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="01f01-140">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="01f01-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="01f01-141">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="01f01-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="01f01-142">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="01f01-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01f01-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="01f01-143">Remarks</span></span>

<span data-ttu-id="01f01-144">Метод **IMAPIFolder::CopyMessages** копирование или перемещение сообщений в другую папку.</span><span class="sxs-lookup"><span data-stu-id="01f01-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="01f01-145">Сообщения, которые открываются с помощью чтения и записи разрешений можно переместить или скопировать.</span><span class="sxs-lookup"><span data-stu-id="01f01-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="01f01-146">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="01f01-146">Notes to implementers</span></span>

<span data-ttu-id="01f01-147">При копировании сообщения в другом хранилище сообщение без использования метода [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , сначала необходимо вызвать [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) с установленным флагом GENERATE_RECEIPT_ONLY.</span><span class="sxs-lookup"><span data-stu-id="01f01-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="01f01-148">Получение хранилища сообщений не отвечает за создание просмотра отчетов для копируемые или перемещения сообщений.</span><span class="sxs-lookup"><span data-stu-id="01f01-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="01f01-149">При вызове **IMAPISupport::CopyMessages** для реализации **IMAPIFolder::CopyMessages**не вызывайте **SetReadFlags**; Он будет называться MAPI.</span><span class="sxs-lookup"><span data-stu-id="01f01-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="01f01-150">Реализация может перемещение или копирование сообщения в любом порядке и создания отчетов о состоянии чтения в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="01f01-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="01f01-151">То есть можно завершить копирование сообщений перед созданием отчетов состояние чтения или отправлять отчеты до внедрения запускает операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="01f01-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="01f01-152">Тем не менее, прочитайте направляются отчеты для всех сообщений скопировать, независимо от того, является ли копирование выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="01f01-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="01f01-153">При операции копирования или перемещения включает в себя более одного сообщения, как можно выполните операцию.</span><span class="sxs-lookup"><span data-stu-id="01f01-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="01f01-154">Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="01f01-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="01f01-155">Попробуйте использовать идентификаторы записей в рамках операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="01f01-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="01f01-156">Также следует сохранить идентификаторы записей, несмотря на то, что он не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="01f01-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="01f01-157">Отправка уведомлений, если перемещение или копирование сообщений, чтобы клиенты являются forewarned, что их вызовы методов [IMAPIProp::SaveChanges](imapiprop-savechanges.md) эти сообщения могут завершиться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="01f01-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="01f01-158">Не включать состояния сообщения или операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="01f01-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="01f01-159">Перемещение и копирование состояния сообщения существенно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="01f01-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="01f01-160">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="01f01-160">Notes to callers</span></span>

<span data-ttu-id="01f01-161">Используйте **IMAPIFolder::CopyMessages** для заполнения папки результатов поиска, где сообщения часто сгруппированные по родительской папки.</span><span class="sxs-lookup"><span data-stu-id="01f01-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="01f01-162">Ожидается, что эти возвращаемые значения в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="01f01-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="01f01-163">**Условие**</span><span class="sxs-lookup"><span data-stu-id="01f01-163">**Condition**</span></span>|<span data-ttu-id="01f01-164">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="01f01-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="01f01-165">**IMAPIFolder::CopyMessages** успешно после копирования или перемещения каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="01f01-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="01f01-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="01f01-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="01f01-167">**IMAPIFolder::CopyMessages** не удалось успешно скопируйте или переместите каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="01f01-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="01f01-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="01f01-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="01f01-169">**IMAPIFolder::CopyMessages** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="01f01-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="01f01-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="01f01-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="01f01-171">При **IMAPIFolder::CopyMessages** не удается завершить, не предполагают, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="01f01-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="01f01-172">**IMAPIFolder::CopyMessages** мог для копирования или перемещения одного или нескольких сообщений перед ошибок.</span><span class="sxs-lookup"><span data-stu-id="01f01-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01f01-173">См. также</span><span class="sxs-lookup"><span data-stu-id="01f01-173">See also</span></span>



[<span data-ttu-id="01f01-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="01f01-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

