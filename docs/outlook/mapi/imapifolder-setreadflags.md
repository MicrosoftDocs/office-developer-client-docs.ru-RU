---
title: имапифолдерсетреадфлагс
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
# <a name="imapifoldersetreadflags"></a><span data-ttu-id="eef8b-103">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="eef8b-103">IMAPIFolder::SetReadFlags</span></span>

<span data-ttu-id="eef8b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eef8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eef8b-105">Задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) одного или нескольких сообщений папки и управляет отправкой отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span> 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="eef8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eef8b-106">Parameters</span></span>

<span data-ttu-id="eef8b-107">_лпмсглист_</span><span class="sxs-lookup"><span data-stu-id="eef8b-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="eef8b-108">возврата Указатель на массив структур [ентрилист](entrylist.md) , определяющий сообщение или сообщения, для которых задаются или удаляются флаги чтения.</span><span class="sxs-lookup"><span data-stu-id="eef8b-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages that have read flags to set or clear.</span></span> <span data-ttu-id="eef8b-109">Если для _лпмсглист_ ЗАДАНО значение null, флаги чтения для всех сообщений папки задаются или сбрасываются.</span><span class="sxs-lookup"><span data-stu-id="eef8b-109">If  _lpMsgList_ is set to NULL, the read flags for all the folder's messages are set or cleared.</span></span> 
    
<span data-ttu-id="eef8b-110">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="eef8b-110">_ulUIParam_</span></span>
  
> <span data-ttu-id="eef8b-111">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="eef8b-111">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="eef8b-112">Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг MESSAGE_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="eef8b-112">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="eef8b-113">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="eef8b-113">_lpProgress_</span></span>
  
> <span data-ttu-id="eef8b-114">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="eef8b-114">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="eef8b-115">Если в _лппрогресс_передается значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации MAPI.</span><span class="sxs-lookup"><span data-stu-id="eef8b-115">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using MAPI's implementation.</span></span> <span data-ttu-id="eef8b-116">Параметр _лппрогресс_ игнорируется, если не установлен флаг MESSAGE_DIALOG в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="eef8b-116">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
<span data-ttu-id="eef8b-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eef8b-117">_ulFlags_</span></span>
  
> <span data-ttu-id="eef8b-118">возврата Битовая маска флагов, определяющая параметр флага чтения сообщения и обработки отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-118">[in] A bitmask of flags that controls the setting of a message's read flag and the processing of read reports.</span></span> <span data-ttu-id="eef8b-119">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="eef8b-119">The following flags can be set:</span></span>
    
  - <span data-ttu-id="eef8b-120">CLEAR_READ_FLAG: флажок MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о прочтении не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="eef8b-120">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="eef8b-121">CLEAR_NRN_PENDING: флажок MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о непрочтенных сообщениях не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="eef8b-121">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and an unread report should not be sent.</span></span> 
        
  - <span data-ttu-id="eef8b-122">CLEAR_RN_PENDING: флажок MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о прочтении не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="eef8b-122">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a read report should not be sent.</span></span> 
        
  - <span data-ttu-id="eef8b-123">GENERATE_RECEIPT_ONLY: отчет о прочтении должен быть отправлен, если он находится в состоянии ожидания, но в состоянии флага MSGFLAG_READ не должно быть никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="eef8b-123">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
        
  - <span data-ttu-id="eef8b-124">MAPI_DEFERRED_ERRORS: разрешает успешно возвращаться **сетреадфлагс** , возможно, до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="eef8b-124">MAPI_DEFERRED_ERRORS: Allows **SetReadFlags** to return successfully, possibly before the operation has completed.</span></span> 
        
  - <span data-ttu-id="eef8b-125">MESSAGE_DIALOG: отображает индикатор хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="eef8b-125">MESSAGE_DIALOG: Displays a progress indicator while the operation proceeds.</span></span>
    
  - <span data-ttu-id="eef8b-126">SUPPRESS_RECEIPT: ожидающий отчет о прочтении должен быть отменен, если был запрошен отчет о прочтении, и этот вызов изменяет состояние сообщения с "непрочтено" на "чтение".</span><span class="sxs-lookup"><span data-stu-id="eef8b-126">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="eef8b-127">Если этот вызов не изменяет состояние сообщения, поставщик хранилища сообщений может игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="eef8b-127">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="eef8b-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="eef8b-128">Return values</span></span>

<span data-ttu-id="eef8b-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="eef8b-129">S_OK</span></span> 
  
> <span data-ttu-id="eef8b-130">Флаг чтения для указанного сообщения или сообщений был успешно установлен или снят.</span><span class="sxs-lookup"><span data-stu-id="eef8b-130">The read flag for the specified message or messages was successfully set or cleared.</span></span>
    
<span data-ttu-id="eef8b-131">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="eef8b-131">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="eef8b-132">Поставщик хранилища сообщений не поддерживает отдавление отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-132">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="eef8b-133">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eef8b-133">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="eef8b-134">В параметре _ulFlags_ задано одно из следующих несовместимых комбинаций флагов:</span><span class="sxs-lookup"><span data-stu-id="eef8b-134">One of the following incompatible combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="eef8b-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="eef8b-135">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="eef8b-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="eef8b-136">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="eef8b-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="eef8b-137">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
<span data-ttu-id="eef8b-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="eef8b-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="eef8b-139">Вызов выполнен успешно, но не все сообщения успешно обработаны.</span><span class="sxs-lookup"><span data-stu-id="eef8b-139">The call succeeded, but not all of the messages were successfully processed.</span></span> <span data-ttu-id="eef8b-140">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="eef8b-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="eef8b-141">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="eef8b-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="eef8b-142">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="eef8b-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eef8b-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="eef8b-143">Remarks</span></span>

<span data-ttu-id="eef8b-144">Метод **IMAPIFolder:: сетреадфлагс** задает или очищает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** одного или нескольких сообщений папки.</span><span class="sxs-lookup"><span data-stu-id="eef8b-144">The **IMAPIFolder::SetReadFlags** method sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property of one or more of the folder's messages.</span></span> <span data-ttu-id="eef8b-145">При установке флага MSGFLAG_READ сообщение помечается как прочитанное, что не обязательно указывает на то, что предполагаемый получатель действительно прочитал сообщение.</span><span class="sxs-lookup"><span data-stu-id="eef8b-145">Setting the MSGFLAG_READ flag marks a message as read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="eef8b-146">**Сетреадфлагс** также управляет отправкой отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-146">**SetReadFlags** also manages the sending of read reports.</span></span> 
  
<span data-ttu-id="eef8b-147">Невозможно изменить флаг чтения для следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="eef8b-147">The read flag cannot be changed for the following:</span></span>
  
- <span data-ttu-id="eef8b-148">Несуществующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="eef8b-148">Messages that do not exist.</span></span>
    
- <span data-ttu-id="eef8b-149">Сообщения, перемещенные в другое место.</span><span class="sxs-lookup"><span data-stu-id="eef8b-149">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="eef8b-150">Сообщения, открытые с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="eef8b-150">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="eef8b-151">Отправленные в настоящее время сообщения.</span><span class="sxs-lookup"><span data-stu-id="eef8b-151">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="eef8b-152">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="eef8b-152">Notes to implementers</span></span>

<span data-ttu-id="eef8b-153">Вы можете не поддерживать отправку отчетов о прочтении и запрос на отключение отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-153">You can decide not to support the sending of read reports and the request to suppress read reports.</span></span> <span data-ttu-id="eef8b-154">Чтобы избежать подавления отчета о прочтении, возвращайте MAPI_E_NO_SUPPRESS при вызове **сетреадфлагс** с SUPPRESS_RECEIPT Set в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="eef8b-154">To avoid suppressing a read report, return MAPI_E_NO_SUPPRESS when **SetReadFlags** is called with SUPPRESS_RECEIPT set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="eef8b-155">Если параметр _лпмсглист_ указывает на несколько сообщений, выполните операцию полностью, как можно скорее для каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="eef8b-155">When the  _lpMsgList_ parameter points to more than one message, perform the operation as completely as possible for each message.</span></span> <span data-ttu-id="eef8b-156">Не прекращайте выполнение операции преждевременно, если не произойдет сбой, который выходит за рамки элемента управления, например, не хватает памяти, не хватает места на диске или повреждено хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="eef8b-156">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span> 
  
<span data-ttu-id="eef8b-157">Если ни один из флагов не задан в параметре _ulFlags_ , применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="eef8b-157">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="eef8b-158">Если MSGFLAG_READ уже заданы, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="eef8b-158">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="eef8b-159">Если MSGFLAG_READ не задано, немедленно установите его и отправьте все ожидающие отчеты о прочтении, если задано свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="eef8b-159">If MSGFLAG_READ is not set, set it immediately and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="eef8b-160">Если установлен флаг SUPPRESS_RECEIPT, применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="eef8b-160">When the SUPPRESS_RECEIPT flag is set, the following rules apply:</span></span>
  
- <span data-ttu-id="eef8b-161">Если MSGFLAG_READ уже заданы, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="eef8b-161">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="eef8b-162">Если MSGFLAG_READ не задано, установите его и отмените все ожидающие отчеты о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-162">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="eef8b-163">Если установлен флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправляются отчеты о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-163">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="eef8b-164">Когда установлен флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающие отчеты о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-164">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="eef8b-165">Не задавайте и не снимайте MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="eef8b-165">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="eef8b-166">Если установлены флаги SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, задайте для **PR_READ_RECEIPT_REQUESTED** значение false, если он установлен и не отправляет отчет о прочтении.</span><span class="sxs-lookup"><span data-stu-id="eef8b-166">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set **PR_READ_RECEIPT_REQUESTED** to FALSE if it is set and do not send a read report.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eef8b-167">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="eef8b-167">Notes to callers</span></span>

<span data-ttu-id="eef8b-168">Эти возвращаемые значения следует ожидать при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="eef8b-168">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="eef8b-169">**Условие**</span><span class="sxs-lookup"><span data-stu-id="eef8b-169">**Condition**</span></span>|<span data-ttu-id="eef8b-170">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="eef8b-170">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eef8b-171">**Сетреадфлагс** успешно обработал каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="eef8b-171">**SetReadFlags** has successfully processed every message.</span></span>  <br/> |<span data-ttu-id="eef8b-172">S_OK</span><span class="sxs-lookup"><span data-stu-id="eef8b-172">S_OK</span></span>  <br/> |
|<span data-ttu-id="eef8b-173">**Сетреадфлагс** не удалось успешно обработать каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="eef8b-173">**SetReadFlags** was unable to successfully process every message.</span></span>  <br/> |<span data-ttu-id="eef8b-174">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eef8b-174">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="eef8b-175">**Сетреадфлагс** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="eef8b-175">**SetReadFlags** was unable to complete.</span></span>  <br/> |<span data-ttu-id="eef8b-176">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="eef8b-176">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="eef8b-177">Если **сетреадфлагс** не удается выполнить, не следует предполагать, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="eef8b-177">When **SetReadFlags** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="eef8b-178">В **сетреадфлагс** может быть возможно установить или снять флаг MSGFLAG_READ для одного или нескольких сообщений, прежде чем возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="eef8b-178">**SetReadFlags** might have been able to set or clear the MSGFLAG_READ flag for one or more of the messages before encountering the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eef8b-179">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="eef8b-179">MFCMAPI reference</span></span>

<span data-ttu-id="eef8b-180">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="eef8b-180">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eef8b-181">**Файл**</span><span class="sxs-lookup"><span data-stu-id="eef8b-181">**File**</span></span>|<span data-ttu-id="eef8b-182">**Функция**</span><span class="sxs-lookup"><span data-stu-id="eef8b-182">**Function**</span></span>|<span data-ttu-id="eef8b-183">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="eef8b-183">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eef8b-184">Фолдердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="eef8b-184">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="eef8b-185">Кфолдердлг:: Онсетреадфлаг</span><span class="sxs-lookup"><span data-stu-id="eef8b-185">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="eef8b-186">MFCMAPI использует метод **IMAPIFolder:: сетреадфлагс** , чтобы вручную задать состояние чтения для указанных сообщений.</span><span class="sxs-lookup"><span data-stu-id="eef8b-186">MFCMAPI uses the **IMAPIFolder::SetReadFlags** method to manually set the read status on the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eef8b-187">См. также</span><span class="sxs-lookup"><span data-stu-id="eef8b-187">See also</span></span>

- [<span data-ttu-id="eef8b-188">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="eef8b-188">ENTRYLIST</span></span>](entrylist.md) 
- [<span data-ttu-id="eef8b-189">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="eef8b-189">IMessage::SetReadFlag</span></span>](imessage-setreadflag.md)  
- [<span data-ttu-id="eef8b-190">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="eef8b-190">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)  
- [<span data-ttu-id="eef8b-191">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="eef8b-191">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)  
- [<span data-ttu-id="eef8b-192">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="eef8b-192">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
- [<span data-ttu-id="eef8b-193">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="eef8b-193">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)  
- [<span data-ttu-id="eef8b-194">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="eef8b-194">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

