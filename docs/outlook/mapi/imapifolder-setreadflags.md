---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406915"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="b57bc-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="b57bc-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="b57bc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b57bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b57bc-105">Задает или очищает флаг MSGFLAG_READ в **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)свойства одного или более сообщений папки и управляет отправкой отчетов о считывке.</span><span class="sxs-lookup"><span data-stu-id="b57bc-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b57bc-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b57bc-106">Parameters</span></span>

<span data-ttu-id="b57bc-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="b57bc-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="b57bc-108">[in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения или сообщения, которые считывались флагами для набора или очистки.</span><span class="sxs-lookup"><span data-stu-id="b57bc-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="b57bc-109">Если  _для lpMsgList_ установлено NULL, для всех сообщений папки установлены или очищаются флаги чтения.</span><span class="sxs-lookup"><span data-stu-id="b57bc-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="b57bc-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b57bc-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="b57bc-111">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="b57bc-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="b57bc-112">Параметр _ulUIParam_ игнорируется, если флаг MESSAGE_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b57bc-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="b57bc-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="b57bc-113">_lpProgress_</span></span>
  
> <span data-ttu-id="b57bc-114">[in] Указатель на объект progress, отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="b57bc-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="b57bc-115">Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="b57bc-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="b57bc-116">Параметр  _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="b57bc-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="b57bc-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b57bc-117">_ulFlags_</span></span>
  
> <span data-ttu-id="b57bc-118">[in] Битмашка флагов, контролирующих настройку флага чтения сообщения и обработку отчетов о считывке.</span><span class="sxs-lookup"><span data-stu-id="b57bc-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="b57bc-119">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b57bc-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="b57bc-120">CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не следует отослать отчет о считыве.</span><span class="sxs-lookup"><span data-stu-id="b57bc-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="b57bc-121">CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и нечитаемый отчет не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="b57bc-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="b57bc-122">CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не следует отослать отчет о считыве.</span><span class="sxs-lookup"><span data-stu-id="b57bc-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="b57bc-123">GENERATE_RECEIPT_ONLY. Отчет о считыве должен быть отправлен, если он находится в ожидании, но не должно быть изменений в состоянии MSGFLAG_READ флага.</span><span class="sxs-lookup"><span data-stu-id="b57bc-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="b57bc-124">MAPI_DEFERRED_ERRORS: Позволяет **setReadFlags** успешно возвращаться, возможно, до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b57bc-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="b57bc-125">MESSAGE_DIALOG: отображает индикатор прогресса во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="b57bc-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="b57bc-126">SUPPRESS_RECEIPT: ожидающих чтения отчет должен быть отменен, если отчет о прочтя был запротезировали, и этот вызов изменяет состояние сообщения с непрочитанные для чтения.</span><span class="sxs-lookup"><span data-stu-id="b57bc-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="b57bc-127">Если этот вызов не изменит состояние сообщения, поставщик магазина сообщений может игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b57bc-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="b57bc-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b57bc-128">Return values</span></span>

<span data-ttu-id="b57bc-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="b57bc-129">S_OK</span></span> 
  
> <span data-ttu-id="b57bc-130">Флаг чтения указанного сообщения или сообщений был успешно задан или очищен.</span><span class="sxs-lookup"><span data-stu-id="b57bc-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="b57bc-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="b57bc-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="b57bc-132">Поставщик магазина сообщений не поддерживает подавление отчетов о считывке.</span><span class="sxs-lookup"><span data-stu-id="b57bc-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="b57bc-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b57bc-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b57bc-134">Одна из следующих несовместимых комбинаций флагов задана в параметре _ulFlags:_</span><span class="sxs-lookup"><span data-stu-id="b57bc-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="b57bc-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="b57bc-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="b57bc-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b57bc-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="b57bc-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b57bc-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="b57bc-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="b57bc-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="b57bc-139">Вызов удался, но не все сообщения были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="b57bc-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="b57bc-140">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="b57bc-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="b57bc-141">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="b57bc-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="b57bc-142">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="b57bc-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b57bc-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="b57bc-143">Remarks</span></span>

<span data-ttu-id="b57bc-144">Метод **IMAPIFolder::SetReadFlags** задает или очищает флаг MSGFLAG_READ  в PR_MESSAGE_FLAGS свойстве одного или более сообщений папки.</span><span class="sxs-lookup"><span data-stu-id="b57bc-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="b57bc-145">Установка флага MSGFLAG_READ означает сообщение как чтение, что не обязательно указывает на то, что получатель действительно прочитал сообщение.</span><span class="sxs-lookup"><span data-stu-id="b57bc-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="b57bc-146">**SetReadFlags** также управляет отправкой отчетов для чтения.</span><span class="sxs-lookup"><span data-stu-id="b57bc-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="b57bc-147">Флаг чтения не может быть изменен для следующих:</span><span class="sxs-lookup"><span data-stu-id="b57bc-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="b57bc-148">Сообщения, которые не существуют.</span><span class="sxs-lookup"><span data-stu-id="b57bc-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="b57bc-149">Сообщения, перенесенные в другое место.</span><span class="sxs-lookup"><span data-stu-id="b57bc-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="b57bc-150">Сообщения, открытые с разрешения на чтение и написание.</span><span class="sxs-lookup"><span data-stu-id="b57bc-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="b57bc-151">Сообщения, которые в настоящее время отправлены.</span><span class="sxs-lookup"><span data-stu-id="b57bc-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="b57bc-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="b57bc-152">Notes to implementers</span></span>

<span data-ttu-id="b57bc-153">Вы можете принять решение не поддерживать отправку отчетов о считыве и запрос на подавление отчетов о считыве.</span><span class="sxs-lookup"><span data-stu-id="b57bc-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="b57bc-154">Чтобы не подавлять отчет о прочтение, MAPI_E_NO_SUPPRESS **когда setReadFlags** SUPPRESS_RECEIPT в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="b57bc-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="b57bc-155">Когда  _параметр lpMsgList_ указывает на несколько сообщений, выполните операцию максимально полной для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="b57bc-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="b57bc-156">Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="b57bc-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="b57bc-157">Если ни один из флагов не задан в  _параметре ulFlags,_ применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="b57bc-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="b57bc-158">Если MSGFLAG_READ уже установлен, ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="b57bc-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="b57bc-159">Если MSGFLAG_READ не установлено, установите его немедленно и отправьте все  ожидающих отчеты о прочтение, если PR_READ_RECEIPT_REQUESTED[(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)свойство установлено.</span><span class="sxs-lookup"><span data-stu-id="b57bc-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="b57bc-160">При SUPPRESS_RECEIPT флаге применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="b57bc-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="b57bc-161">Если MSGFLAG_READ уже установлен, ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="b57bc-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="b57bc-162">Если MSGFLAG_READ не установлено, установите его и отмените все ожидающих отчеты о прочтевом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b57bc-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="b57bc-163">Когда за установлен CLEAR_READ_FLAG флаг, MSGFLAG_READ флаг в свойстве PR_MESSAGE_FLAGS сообщения и не **отправляйте** отчеты о считыве.</span><span class="sxs-lookup"><span data-stu-id="b57bc-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="b57bc-164">Когда установлен GENERATE_RECEIPT_ONLY флаг, отправьте все ожидающих отчеты о прочтевом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b57bc-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="b57bc-165">Не устанавливай и не MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="b57bc-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="b57bc-166">Когда установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, установите PR_READ_RECEIPT_REQUESTED  false, если он установлен, и не отправьте отчет о прочтителье.</span><span class="sxs-lookup"><span data-stu-id="b57bc-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b57bc-167">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b57bc-167">Notes to callers</span></span>

<span data-ttu-id="b57bc-168">Ожидайте этих значений возврата в следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="b57bc-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="b57bc-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="b57bc-169">**Condition**</span></span>|<span data-ttu-id="b57bc-170">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="b57bc-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b57bc-171">**SetReadFlags** успешно обработал каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="b57bc-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="b57bc-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="b57bc-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="b57bc-173">**SetReadFlags** не удалось успешно обработать каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="b57bc-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="b57bc-174">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b57bc-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="b57bc-175">**SetReadFlags** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="b57bc-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="b57bc-176">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b57bc-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="b57bc-177">Если **SetReadFlags** не удается выполнить, не думайте, что работа не была сделана.</span><span class="sxs-lookup"><span data-stu-id="b57bc-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="b57bc-178">**SetReadFlags,** возможно, удалось установить или очистить флаг MSGFLAG_READ для одного или более сообщений, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b57bc-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b57bc-179">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b57bc-179">MFCMAPI reference</span></span>

<span data-ttu-id="b57bc-180">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b57bc-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b57bc-181">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b57bc-181">**File**</span></span>|<span data-ttu-id="b57bc-182">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b57bc-182">**Function**</span></span>|<span data-ttu-id="b57bc-183">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b57bc-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b57bc-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b57bc-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="b57bc-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="b57bc-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="b57bc-186">MFCMAPI использует метод **IMAPIFolder::SetReadFlags,** чтобы вручную установить состояние чтения указанных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b57bc-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b57bc-187">См. также</span><span class="sxs-lookup"><span data-stu-id="b57bc-187">See also</span></span>

- [<span data-ttu-id="b57bc-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="b57bc-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="b57bc-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="b57bc-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="b57bc-190">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="b57bc-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="b57bc-191">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="b57bc-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="b57bc-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="b57bc-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="b57bc-193">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="b57bc-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="b57bc-194">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="b57bc-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

