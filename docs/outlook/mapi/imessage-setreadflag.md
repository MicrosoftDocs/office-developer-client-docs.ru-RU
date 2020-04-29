---
title: имессажесетреадфлаг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439872"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="a4440-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="a4440-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="a4440-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4440-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4440-105">Задает или снимает флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения и управляет отправкой отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a4440-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4440-106">Parameters</span></span>

<span data-ttu-id="a4440-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a4440-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a4440-108">возврата Битовая маска флагов, которые управляют параметром флага чтения сообщения, флаг MSGFLAG_READ сообщения в свойстве **PR_MESSAGE_FLAGS** и обработки отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="a4440-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a4440-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="a4440-110">CLEAR_READ_FLAG: флажок MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о прочтении не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="a4440-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="a4440-111">CLEAR_NRN_PENDING: флажок MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о состоянии, не являющемся отчетом о прочтении, не должен отправляться.</span><span class="sxs-lookup"><span data-stu-id="a4440-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="a4440-112">CLEAR_RN_PENDING: флажок MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** , а отчет о прочтении не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="a4440-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="a4440-113">GENERATE_RECEIPT_ONLY: отчет о прочтении должен быть отправлен, если он находится в состоянии ожидания, но в состоянии флага MSGFLAG_READ не должно быть никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="a4440-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="a4440-114">MAPI_DEFERRED_ERRORS: разрешает успешно возвращаться **сетреадфлаг** , возможно, до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a4440-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="a4440-115">SUPPRESS_RECEIPT: ожидающий отчет о прочтении должен быть отменен, если был запрошен отчет о прочтении, и этот вызов изменяет состояние сообщения с "непрочтено" на "чтение".</span><span class="sxs-lookup"><span data-stu-id="a4440-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="a4440-116">Если этот вызов не изменяет состояние сообщения, поставщик хранилища сообщений может игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="a4440-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a4440-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4440-117">Return value</span></span>

<span data-ttu-id="a4440-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a4440-118">S_OK</span></span> 
  
> <span data-ttu-id="a4440-119">Флаг чтения сообщения успешно установлен или снят.</span><span class="sxs-lookup"><span data-stu-id="a4440-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="a4440-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="a4440-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="a4440-121">Поставщик хранилища сообщений не поддерживает отдавление отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="a4440-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a4440-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="a4440-123">В параметре _ulFlags_ задано одно из следующих сочетаний флагов:</span><span class="sxs-lookup"><span data-stu-id="a4440-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="a4440-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="a4440-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="a4440-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="a4440-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="a4440-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="a4440-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a4440-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4440-127">Remarks</span></span>

<span data-ttu-id="a4440-128">Метод **iMessage:: сетреадфлаг** задает или очищает флаг MSGFLAG_READ сообщения в свойстве **PR_MESSAGE_FLAGS** и вызывает [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4440-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="a4440-129">При установке флага MSGFLAG_READ сообщение помечается как прочитанное, что не обязательно свидетельствует о том, что предполагаемый получатель действительно прочитал сообщение.</span><span class="sxs-lookup"><span data-stu-id="a4440-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="a4440-130">**Сетреадфлагс** также управляет отправкой отчетов о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="a4440-131">Отчет о прочтении отправляются только в том случае, если отправитель запросил его.</span><span class="sxs-lookup"><span data-stu-id="a4440-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="a4440-132">Невозможно изменить флаг чтения для:</span><span class="sxs-lookup"><span data-stu-id="a4440-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="a4440-133">Несуществующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4440-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="a4440-134">Сообщения, перемещенные в другое место.</span><span class="sxs-lookup"><span data-stu-id="a4440-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="a4440-135">Сообщения, открытые с разрешениями на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="a4440-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="a4440-136">Отправленные в настоящее время сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4440-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="a4440-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a4440-137">Notes to callers</span></span>

<span data-ttu-id="a4440-138">Если ни один из флагов не задан в параметре _ulFlags_ , применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="a4440-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="a4440-139">Если MSGFLAG_READ уже заданы, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="a4440-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="a4440-140">Если MSGFLAG_READ не задано, установите его и отправьте все ожидающие отчеты о прочтении, если задано свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a4440-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="a4440-141">Если установлены флаги SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, то PR_READ_RECEIPT_REQUESTED бит (если он установлен) должен быть снят, а отчет о прочтении не должен быть отправлен.</span><span class="sxs-lookup"><span data-stu-id="a4440-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="a4440-142">Если установлен флаг SUPPRESS_RECEIPT:</span><span class="sxs-lookup"><span data-stu-id="a4440-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="a4440-143">Если MSGFLAG_READ уже заданы, ничего делать не нужно.</span><span class="sxs-lookup"><span data-stu-id="a4440-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="a4440-144">Если MSGFLAG_READ не задано, установите его и отмените все ожидающие отчеты о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="a4440-145">Если установлен флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправляются отчеты о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="a4440-146">Когда установлен флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающие отчеты о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="a4440-147">Не задавайте и не снимайте MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="a4440-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="a4440-148">Если установлены флаги SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, задайте для свойства PR_READ_RECEIPT_REQUESTED значение FALSE, если оно задано и не отправляет отчет о прочтении.</span><span class="sxs-lookup"><span data-stu-id="a4440-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="a4440-149">Вы можете оптимизировать поведение отчета, отменив создание отчетов о прочтении при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="a4440-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="a4440-150">Тем не менее, если вы не поддерживаете отдавление отчетов и клиент вызывает **сетреадфлаг** с установленным флагом SUPPRESS_RECEIPT, возвращайте MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="a4440-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a4440-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a4440-151">MFCMAPI reference</span></span>

<span data-ttu-id="a4440-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a4440-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a4440-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a4440-153">**File**</span></span>|<span data-ttu-id="a4440-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a4440-154">**Function**</span></span>|<span data-ttu-id="a4440-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a4440-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a4440-156">Фолдердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="a4440-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="a4440-157">Кфолдердлг:: Онсетреадфлаг</span><span class="sxs-lookup"><span data-stu-id="a4440-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="a4440-158">MFCMAPI использует метод **iMessage:: сетреадфлаг** для установки флагов чтения для выбранных сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4440-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4440-159">См. также</span><span class="sxs-lookup"><span data-stu-id="a4440-159">See also</span></span>

- [<span data-ttu-id="a4440-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a4440-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="a4440-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="a4440-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="a4440-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="a4440-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="a4440-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a4440-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="a4440-164">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="a4440-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="a4440-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a4440-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="a4440-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a4440-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

