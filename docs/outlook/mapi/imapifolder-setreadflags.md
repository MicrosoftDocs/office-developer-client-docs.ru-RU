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
ms.openlocfilehash: a52c0501040d77ddb8172b212bf341a08704dcc3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808872"
---
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="aea69-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="aea69-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="aea69-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aea69-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aea69-105">Задает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) из одного или нескольких сообщений, папок и управляет Отправка чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="aea69-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="aea69-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aea69-106">Parameters</span></span>

<span data-ttu-id="aea69-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="aea69-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="aea69-108">[in] Указатель на массив структур [ENTRYLIST](entrylist.md) , чтобы указать сообщения или сообщения, прочли флаги, установите или снимите флажок.</span><span class="sxs-lookup"><span data-stu-id="aea69-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="aea69-109">Если _lpMsgList_ имеет значение NULL, прочтите помечает для всех установить или снять папки сообщений.</span><span class="sxs-lookup"><span data-stu-id="aea69-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="aea69-110">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="aea69-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="aea69-111">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aea69-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="aea69-112">Параметр _ulUIParam_ игнорируется, пока флаг MESSAGE_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="aea69-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="aea69-113">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="aea69-113">_lpProgress_</span></span>
  
> <span data-ttu-id="aea69-114">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aea69-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="aea69-115">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор хода выполнения с помощью реализации MAPI's.</span><span class="sxs-lookup"><span data-stu-id="aea69-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="aea69-116">Параметр _lpProgress_ используется только флаг MESSAGE_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="aea69-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="aea69-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="aea69-117">_ulFlags_</span></span>
  
> <span data-ttu-id="aea69-118">[in] Битовая маска флаги, которыми управляет состояние флага чтения сообщения и обработку чтение отчеты.</span><span class="sxs-lookup"><span data-stu-id="aea69-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="aea69-119">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="aea69-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="aea69-120">CLEAR_READ_FLAG: Флаг MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="aea69-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="aea69-121">CLEAR_NRN_PENDING: Флаг MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться непрочитанные сообщения отчета.</span><span class="sxs-lookup"><span data-stu-id="aea69-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="aea69-122">CLEAR_RN_PENDING: Флаг MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="aea69-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="aea69-123">GENERATE_RECEIPT_ONLY: Чтения отчет следует отправить один ожидающий, когда должно быть никаких изменений в состояние флага MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="aea69-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="aea69-124">MAPI_DEFERRED_ERRORS: Разрешает **SetReadFlags** для возврата успешно, возможно до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="aea69-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="aea69-125">MESSAGE_DIALOG: Отображает индикатор хода выполнения во время операции.</span><span class="sxs-lookup"><span data-stu-id="aea69-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="aea69-126">SUPPRESS_RECEIPT: Ожидающие чтения отчета должна быть отменена Если запрошен чтения отчета, и этот вызов изменяет состояние сообщения из непрочитанные сообщения для чтения.</span><span class="sxs-lookup"><span data-stu-id="aea69-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="aea69-127">Если этот вызов не изменяет состояние сообщения, поставщик хранения сообщений можно игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="aea69-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="aea69-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="aea69-128">Return values</span></span>

<span data-ttu-id="aea69-129">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="aea69-129">S_OK</span></span> 
  
> <span data-ttu-id="aea69-130">Чтение флаг для указанного сообщения или сообщения успешно задание или снят.</span><span class="sxs-lookup"><span data-stu-id="aea69-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="aea69-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="aea69-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="aea69-132">Поставщик хранения сообщения не поддерживает подавления чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="aea69-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="aea69-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aea69-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="aea69-134">Один из следующих комбинаций несовместимых флагов задано с помощью параметра _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="aea69-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="aea69-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="aea69-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="aea69-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="aea69-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="aea69-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="aea69-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="aea69-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="aea69-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="aea69-139">Вызов завершился успешно, но не все сообщения были успешно обработан.</span><span class="sxs-lookup"><span data-stu-id="aea69-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="aea69-140">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="aea69-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="aea69-141">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="aea69-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="aea69-142">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="aea69-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aea69-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="aea69-143">Remarks</span></span>

<span data-ttu-id="aea69-144">Метод **IMAPIFolder::SetReadFlags** устанавливает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** одной или нескольких папок сообщений.</span><span class="sxs-lookup"><span data-stu-id="aea69-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="aea69-145">Установка флага MSGFLAG_READ помечает сообщения как прочитанного, который не обязательно означает, что получателю фактически имеет чтение сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea69-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="aea69-146">Кроме того, **SetReadFlags** управляет Отправка просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="aea69-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="aea69-147">Чтение флаг нельзя изменить в следующих:</span><span class="sxs-lookup"><span data-stu-id="aea69-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="aea69-148">Сообщения, не существует.</span><span class="sxs-lookup"><span data-stu-id="aea69-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="aea69-149">Сообщения, которые были перемещены в другом месте.</span><span class="sxs-lookup"><span data-stu-id="aea69-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="aea69-150">Сообщения, открытые с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="aea69-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="aea69-151">Сообщения, которые передаются в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="aea69-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="aea69-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="aea69-152">Notes to implementers</span></span>

<span data-ttu-id="aea69-153">Можно указать, кто не поддерживает отправку чтения отчетов и запроса для отмены вывода чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="aea69-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="aea69-154">Чтобы избежать подавления чтения отчета, возврата MAPI_E_NO_SUPPRESS при вызове **SetReadFlags** с SUPPRESS_RECEIPT задавать в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="aea69-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="aea69-155">Если параметр _lpMsgList_ указывает на более одного сообщения, как можно выполните операцию для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea69-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="aea69-156">Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="aea69-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="aea69-157">Если ни один из флагов в параметре _ulFlags_ , применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="aea69-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="aea69-158">Если MSGFLAG_READ уже задано, ничего не предпринимать.</span><span class="sxs-lookup"><span data-stu-id="aea69-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="aea69-159">Если MSGFLAG_READ не установлен, установите его сразу же и отправить все ожидающие просмотра отчетов, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) имеет значение.</span><span class="sxs-lookup"><span data-stu-id="aea69-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="aea69-160">Если для флага SUPPRESS_RECEIPT, применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="aea69-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="aea69-161">Если MSGFLAG_READ уже задано, ничего не предпринимать.</span><span class="sxs-lookup"><span data-stu-id="aea69-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="aea69-162">Если MSGFLAG_READ не установлен, установите его и отменить ожидающие просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="aea69-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="aea69-163">Если флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправлять чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="aea69-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="aea69-164">Если для флага GENERATE_RECEIPT_ONLY, отправьте все ожидающие чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="aea69-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="aea69-165">Выполните MSGFLAG_READ не установлен или clear.</span><span class="sxs-lookup"><span data-stu-id="aea69-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="aea69-166">Когда SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, задайте **PR_READ_RECEIPT_REQUESTED** значение FALSE, если оно установлено и не отправлять просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="aea69-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="aea69-167">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="aea69-167">Notes to callers</span></span>

<span data-ttu-id="aea69-168">Ожидается, что эти возвращаемые значения в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="aea69-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="aea69-169">**Условие**</span><span class="sxs-lookup"><span data-stu-id="aea69-169">**Condition**</span></span>|<span data-ttu-id="aea69-170">**������������ ��������**</span><span class="sxs-lookup"><span data-stu-id="aea69-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aea69-171">**SetReadFlags** успешно обработал каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea69-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="aea69-172">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="aea69-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="aea69-173">**SetReadFlags** не удалось успешно обработать каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea69-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="aea69-174">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aea69-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="aea69-175">**SetReadFlags** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="aea69-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="aea69-176">Любое значение ошибки, за исключением MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aea69-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="aea69-177">При **SetReadFlags** не удается завершить, не предполагают, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="aea69-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="aea69-178">**SetReadFlags** мог установить или сбросить флаг MSGFLAG_READ для одного или нескольких сообщений перед ошибок.</span><span class="sxs-lookup"><span data-stu-id="aea69-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="aea69-179">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="aea69-179">MFCMAPI reference</span></span>

<span data-ttu-id="aea69-180">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="aea69-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="aea69-181">**����**</span><span class="sxs-lookup"><span data-stu-id="aea69-181">**File**</span></span>|<span data-ttu-id="aea69-182">**�������**</span><span class="sxs-lookup"><span data-stu-id="aea69-182">**Function**</span></span>|<span data-ttu-id="aea69-183">**�����������**</span><span class="sxs-lookup"><span data-stu-id="aea69-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aea69-184">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="aea69-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="aea69-185">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="aea69-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="aea69-186">Mfcmapi (en) использует метод **IMAPIFolder::SetReadFlags** Чтобы вручную задать состояние чтения на указанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="aea69-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aea69-187">См. также</span><span class="sxs-lookup"><span data-stu-id="aea69-187">See also</span></span>

- [<span data-ttu-id="aea69-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="aea69-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="aea69-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="aea69-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="aea69-190">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="aea69-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="aea69-191">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="aea69-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="aea69-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="aea69-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="aea69-193">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="aea69-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="aea69-194">Обработка ошибок с помощью макросов</span><span class="sxs-lookup"><span data-stu-id="aea69-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

