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
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="9d648-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="9d648-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="9d648-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d648-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d648-105">Задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)одного или более сообщений папки и управляет отправкой отчетов о прочтенных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="9d648-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9d648-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d648-106">Parameters</span></span>

<span data-ttu-id="9d648-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="9d648-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="9d648-108">[in] Указатель на массив структур [ENTRYLIST,](entrylist.md) которые определяют сообщения с флагами чтения, которые необходимо установить или очистить.</span><span class="sxs-lookup"><span data-stu-id="9d648-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="9d648-109">Если  _для lpMsgList_ установлено NULL, флаги чтения для всех сообщений папки устанавливаются или очищаются.</span><span class="sxs-lookup"><span data-stu-id="9d648-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="9d648-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9d648-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="9d648-111">[in] Handle to the parent window of the progress indicator.</span><span class="sxs-lookup"><span data-stu-id="9d648-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="9d648-112">Параметр _ulUIParam_ игнорируется, если MESSAGE_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="9d648-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="9d648-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9d648-113">_lpProgress_</span></span>
  
> <span data-ttu-id="9d648-114">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9d648-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9d648-115">Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d648-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="9d648-116">Параметр _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG не установлен в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="9d648-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="9d648-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d648-117">_ulFlags_</span></span>
  
> <span data-ttu-id="9d648-118">[in] Битоваяmas флагов, которая управляет установкой флага чтения сообщения и обработкой отчетов о прочте..</span><span class="sxs-lookup"><span data-stu-id="9d648-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="9d648-119">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9d648-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="9d648-120">CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о прочтях.</span><span class="sxs-lookup"><span data-stu-id="9d648-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="9d648-121">CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и не должен быть отправлен непрочитанные отчеты.</span><span class="sxs-lookup"><span data-stu-id="9d648-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="9d648-122">CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о прочтях.</span><span class="sxs-lookup"><span data-stu-id="9d648-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="9d648-123">GENERATE_RECEIPT_ONLY. Если отчет находится в состоянии ожидания, должен быть отправлен отчет о MSGFLAG_READ состояния.</span><span class="sxs-lookup"><span data-stu-id="9d648-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="9d648-124">MAPI_DEFERRED_ERRORS: позволяет **SetReadFlags** успешно возвращаться, возможно, до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9d648-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="9d648-125">MESSAGE_DIALOG: отображает индикатор хода выполнения во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9d648-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="9d648-126">SUPPRESS_RECEIPT: отчет об ожидающих чтениях должен быть отменен, если запросят отчет о прочтечении и этот вызов изменяет состояние сообщения с непрочитанного на прочитанные.</span><span class="sxs-lookup"><span data-stu-id="9d648-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="9d648-127">Если этот вызов не меняет состояние сообщения, поставщик store сообщений может игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="9d648-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9d648-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9d648-128">Return values</span></span>

<span data-ttu-id="9d648-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d648-129">S_OK</span></span> 
  
> <span data-ttu-id="9d648-130">Флаг чтения для указанного сообщения или сообщений успешно установлен или очищен.</span><span class="sxs-lookup"><span data-stu-id="9d648-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="9d648-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="9d648-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="9d648-132">Поставщик store сообщений не поддерживает подавление отчетов о прочтениях.</span><span class="sxs-lookup"><span data-stu-id="9d648-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="9d648-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9d648-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="9d648-134">В параметре  _ulFlags_ задана одна из следующих несовместимых комбинаций флагов:</span><span class="sxs-lookup"><span data-stu-id="9d648-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="9d648-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="9d648-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="9d648-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="9d648-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="9d648-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="9d648-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="9d648-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="9d648-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="9d648-139">Вызов был успешным, но не все сообщения были успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="9d648-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="9d648-140">При возврате этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="9d648-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="9d648-141">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="9d648-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="9d648-142">Дополнительные сведения см. в теме ["Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="9d648-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d648-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d648-143">Remarks</span></span>

<span data-ttu-id="9d648-144">Метод **IMAPIFolder::SetReadFlags** задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** одного или более сообщений папки.</span><span class="sxs-lookup"><span data-stu-id="9d648-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="9d648-145">Установка флага MSGFLAG_READ помечания сообщения как прочитаного, что необязательно указывает на то, что указанный получатель действительно прочитал сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d648-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="9d648-146">**SetReadFlags** также управляет отправкой отчетов чтения.</span><span class="sxs-lookup"><span data-stu-id="9d648-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="9d648-147">Флаг чтения нельзя изменить для следующих ок.</span><span class="sxs-lookup"><span data-stu-id="9d648-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="9d648-148">Сообщения, которые не существуют.</span><span class="sxs-lookup"><span data-stu-id="9d648-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="9d648-149">Сообщения, которые были перемещены в другое место.</span><span class="sxs-lookup"><span data-stu-id="9d648-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="9d648-150">Сообщения, которые открываются с разрешением на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="9d648-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="9d648-151">Отправленные в данный момент сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d648-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="9d648-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="9d648-152">Notes to implementers</span></span>

<span data-ttu-id="9d648-153">Вы можете не поддерживать отправку отчетов о прочтях и запрос на подавление отчетов о прочтях.</span><span class="sxs-lookup"><span data-stu-id="9d648-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="9d648-154">Чтобы избежать подавления отчета о прочтение, MAPI_E_NO_SUPPRESS при SUPPRESS_RECEIPT **SetReadFlags** в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="9d648-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="9d648-155">Если параметр  _lpMsgList_ указывает на несколько сообщений, выполните операцию как можно точнее для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9d648-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="9d648-156">Не останавливайте операцию раньше времени, если не произойдет сбой, который находится вне вашего контроля, например, если недостаточно памяти, недостаточно места на диске или не будет повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d648-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="9d648-157">Если ни один из флагов не задан в параметре  _ulFlags,_ применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="9d648-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="9d648-158">Если MSGFLAG_READ уже установлен, ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="9d648-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="9d648-159">Если MSGFLAG_READ не установлен, задайте его немедленно и отправьте все ожидающих отчетов о прочтение, если установлено свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested).](pidtagreadreceiptrequested-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9d648-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="9d648-160">При SUPPRESS_RECEIPT флага применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="9d648-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="9d648-161">Если MSGFLAG_READ уже установлен, ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="9d648-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="9d648-162">Если MSGFLAG_READ не установлен, установите его и отмените все ожидающих отчетов о прочте..</span><span class="sxs-lookup"><span data-stu-id="9d648-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="9d648-163">Когда флаг CLEAR_READ_FLAG установлен, MSGFLAG_READ флага в свойстве PR_MESSAGE_FLAGS сообщения  и не отправляйте отчеты о прочтенных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="9d648-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="9d648-164">Когда флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающих отчетов о прочте..</span><span class="sxs-lookup"><span data-stu-id="9d648-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="9d648-165">Не устанавливать и не очищать MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="9d648-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="9d648-166">Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, установите PR_READ_RECEIPT_REQUESTED false,  если он установлен, и не отправляйте отчет о прочтях.</span><span class="sxs-lookup"><span data-stu-id="9d648-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9d648-167">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9d648-167">Notes to callers</span></span>

<span data-ttu-id="9d648-168">Эти возвращаемые значения следует ожидать при следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="9d648-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="9d648-169">**Condition**</span><span class="sxs-lookup"><span data-stu-id="9d648-169">**Condition**</span></span>|<span data-ttu-id="9d648-170">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="9d648-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d648-171">**SetReadFlags успешно** обработал каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d648-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="9d648-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d648-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="9d648-173">**SetReadFlags** не удалось успешно обработать каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d648-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="9d648-174">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9d648-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="9d648-175">Не удалось завершить **setReadFlags.**</span><span class="sxs-lookup"><span data-stu-id="9d648-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="9d648-176">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9d648-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="9d648-177">Если **SetReadFlags** не удается завершить работу, не предполагать, что ничего не было сделано.</span><span class="sxs-lookup"><span data-stu-id="9d648-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="9d648-178">**SetReadFlags** мог установить или очистить флаг MSGFLAG_READ для одного или более сообщений, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="9d648-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9d648-179">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9d648-179">MFCMAPI reference</span></span>

<span data-ttu-id="9d648-180">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9d648-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9d648-181">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9d648-181">**File**</span></span>|<span data-ttu-id="9d648-182">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9d648-182">**Function**</span></span>|<span data-ttu-id="9d648-183">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9d648-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d648-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9d648-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="9d648-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="9d648-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="9d648-186">MFCMAPI использует метод **IMAPIFolder::SetReadFlags,** чтобы вручную установить состояние чтения для указанных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d648-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d648-187">См. также</span><span class="sxs-lookup"><span data-stu-id="9d648-187">See also</span></span>

- [<span data-ttu-id="9d648-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="9d648-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="9d648-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="9d648-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="9d648-190">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="9d648-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="9d648-191">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="9d648-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="9d648-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9d648-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="9d648-193">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="9d648-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="9d648-194">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="9d648-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

