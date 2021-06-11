---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426074"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="233ae-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="233ae-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="233ae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="233ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="233ae-105">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="233ae-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="233ae-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="233ae-106">Parameters</span></span>

 <span data-ttu-id="233ae-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="233ae-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="233ae-108">[in] Указатель на структуру [ENTRYLIST,](entrylist.md) которая содержит количество удаляемого сообщения, и массив [структур ENTRYID,](entryid.md) которые идентифицируют сообщения.</span><span class="sxs-lookup"><span data-stu-id="233ae-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="233ae-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="233ae-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="233ae-110">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="233ae-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="233ae-111">Параметр _ulUIParam_ игнорируется, если флаг MESSAGE_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="233ae-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="233ae-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="233ae-112">_lpProgress_</span></span>
  
> <span data-ttu-id="233ae-113">[in] Указатель на объект progress, отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="233ae-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="233ae-114">Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI.</span><span class="sxs-lookup"><span data-stu-id="233ae-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="233ae-115">Параметр _lpProgress_ игнорируется, если флаг MESSAGE_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="233ae-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="233ae-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="233ae-116">_ulFlags_</span></span>
  
> <span data-ttu-id="233ae-117">[in] Немного флагов, которые контролируют удаление сообщений.</span><span class="sxs-lookup"><span data-stu-id="233ae-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="233ae-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="233ae-118">The following flags can be set:</span></span>
    
<span data-ttu-id="233ae-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="233ae-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="233ae-120">Постоянно удаляет все сообщения, в том числе удаленные с мягкими сообщениями.</span><span class="sxs-lookup"><span data-stu-id="233ae-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="233ae-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="233ae-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="233ae-122">Отображает индикатор прогресса по мере выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="233ae-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="233ae-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="233ae-123">Return value</span></span>

<span data-ttu-id="233ae-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="233ae-124">S_OK</span></span> 
  
> <span data-ttu-id="233ae-125">Указанное сообщение или сообщения были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="233ae-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="233ae-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="233ae-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="233ae-127">Вызов удался, но не все сообщения были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="233ae-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="233ae-128">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="233ae-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="233ae-129">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="233ae-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="233ae-130">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="233ae-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="233ae-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="233ae-131">Remarks</span></span>

<span data-ttu-id="233ae-132">Метод **IMAPIFolder::D eleteMessages** удаляет сообщения из папки.</span><span class="sxs-lookup"><span data-stu-id="233ae-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="233ae-133">Сообщения, которые не существуют, которые были перемещены в другое место, открытые с разрешения чтения или записи или отправленные в настоящее время, не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="233ae-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="233ae-134">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="233ae-134">Notes to implementers</span></span>

<span data-ttu-id="233ae-135">Если операция удаления включает несколько сообщений, выполните операцию как можно более полной для каждой папки, даже если одно или несколько сообщений невозможно удалить.</span><span class="sxs-lookup"><span data-stu-id="233ae-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="233ae-136">Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="233ae-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="233ae-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="233ae-137">Notes to callers</span></span>

<span data-ttu-id="233ae-138">Ожидайте этих значений возврата в следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="233ae-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="233ae-139">**Condition**</span><span class="sxs-lookup"><span data-stu-id="233ae-139">**Condition**</span></span>|<span data-ttu-id="233ae-140">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="233ae-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="233ae-141">**DeleteMessages** успешно удалил каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="233ae-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="233ae-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="233ae-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="233ae-143">**DeleteMessages** не удалось успешно удалить каждое сообщение и подмостки.</span><span class="sxs-lookup"><span data-stu-id="233ae-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="233ae-144">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="233ae-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="233ae-145">**DeleteMessages** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="233ae-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="233ae-146">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="233ae-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="233ae-147">Если **DeleteMessages** не удается выполнить, не думайте, что работы не было сделано.</span><span class="sxs-lookup"><span data-stu-id="233ae-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="233ae-148">**DeleteMessages,** возможно, удалось удалить одно или несколько сообщений, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="233ae-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="233ae-149">**DeleteMessages** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND в зависимости от реализации магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="233ae-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="233ae-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="233ae-150">MFCMAPI reference</span></span>

<span data-ttu-id="233ae-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="233ae-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="233ae-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="233ae-152">**File**</span></span>|<span data-ttu-id="233ae-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="233ae-153">**Function**</span></span>|<span data-ttu-id="233ae-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="233ae-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="233ae-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="233ae-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="233ae-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="233ae-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="233ae-157">MFCMAPI использует метод **IMAPIFolder::D eleteMessages** для удаления указанных сообщений.</span><span class="sxs-lookup"><span data-stu-id="233ae-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="233ae-158">См. также</span><span class="sxs-lookup"><span data-stu-id="233ae-158">See also</span></span>



[<span data-ttu-id="233ae-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="233ae-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="233ae-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="233ae-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="233ae-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="233ae-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="233ae-162">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="233ae-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="233ae-163">Использование макроса для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="233ae-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

