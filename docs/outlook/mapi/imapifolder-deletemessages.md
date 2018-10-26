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
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578635"
---
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="f1b98-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="f1b98-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="f1b98-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1b98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1b98-105">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="f1b98-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f1b98-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1b98-106">Parameters</span></span>

 <span data-ttu-id="f1b98-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="f1b98-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="f1b98-108">[in] Указатель на структуру [ENTRYLIST](entrylist.md) , содержащее число сообщений для удаления и массив структур [ENTRYID](entryid.md) , чтобы указать сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1b98-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="f1b98-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f1b98-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="f1b98-110">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1b98-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="f1b98-111">Параметр _ulUIParam_ игнорируется, пока флаг MESSAGE_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f1b98-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f1b98-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="f1b98-112">_lpProgress_</span></span>
  
> <span data-ttu-id="f1b98-113">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1b98-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="f1b98-114">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f1b98-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="f1b98-115">Параметр _lpProgress_ игнорируется, пока флаг MESSAGE_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f1b98-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f1b98-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f1b98-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f1b98-117">[in] Битовая маска флаги, который определяет, как сообщения будут удалены.</span><span class="sxs-lookup"><span data-stu-id="f1b98-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="f1b98-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="f1b98-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f1b98-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="f1b98-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="f1b98-120">Безвозвратно удаляет все сообщения, включая удаленные из них.</span><span class="sxs-lookup"><span data-stu-id="f1b98-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="f1b98-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f1b98-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="f1b98-122">Отображает индикатор выполнения, как операция продолжается.</span><span class="sxs-lookup"><span data-stu-id="f1b98-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1b98-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1b98-123">Return value</span></span>

<span data-ttu-id="f1b98-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1b98-124">S_OK</span></span> 
  
> <span data-ttu-id="f1b98-125">Указанный сообщения или сообщения были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="f1b98-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="f1b98-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="f1b98-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="f1b98-127">Вызов завершился успешно, но не все сообщения были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="f1b98-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="f1b98-128">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="f1b98-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="f1b98-129">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="f1b98-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f1b98-130">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="f1b98-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1b98-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="f1b98-131">Remarks</span></span>

<span data-ttu-id="f1b98-132">Метод **IMAPIFolder::DeleteMessages** удаляет сообщения из папки.</span><span class="sxs-lookup"><span data-stu-id="f1b98-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="f1b98-133">Не удается удалить сообщения, не существует, были перемещены в другом месте, открытые с разрешением на чтение и запись или, представленных в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="f1b98-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f1b98-134">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="f1b98-134">Notes to implementers</span></span>

<span data-ttu-id="f1b98-135">При операции удаления состоит из нескольких сообщений, выполните операцию, как можно для каждой папки даже в том случае, если не удается удалить один или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="f1b98-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="f1b98-136">Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="f1b98-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1b98-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f1b98-137">Notes to callers</span></span>

<span data-ttu-id="f1b98-138">Ожидается, что эти возвращаемые значения в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="f1b98-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="f1b98-139">**Условие**</span><span class="sxs-lookup"><span data-stu-id="f1b98-139">**Condition**</span></span>|<span data-ttu-id="f1b98-140">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="f1b98-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f1b98-141">**DeleteMessages** успешно удален каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f1b98-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="f1b98-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1b98-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="f1b98-143">**DeleteMessages** не удалось успешно удалить все сообщения и вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="f1b98-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="f1b98-144">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f1b98-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="f1b98-145">**DeleteMessages** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="f1b98-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="f1b98-146">Любое значение ошибки, за исключением MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f1b98-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="f1b98-147">При **DeleteMessages** не удается завершить, не предполагают, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="f1b98-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="f1b98-148">**DeleteMessages** мог удалить одно или несколько сообщений, прежде чем ошибок.</span><span class="sxs-lookup"><span data-stu-id="f1b98-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="f1b98-149">**DeleteMessages** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="f1b98-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1b98-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f1b98-150">MFCMAPI reference</span></span>

<span data-ttu-id="f1b98-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f1b98-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1b98-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f1b98-152">**File**</span></span>|<span data-ttu-id="f1b98-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f1b98-153">**Function**</span></span>|<span data-ttu-id="f1b98-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f1b98-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1b98-155">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f1b98-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="f1b98-156">CFolderDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="f1b98-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="f1b98-157">Mfcmapi (en) метод **IMAPIFolder::DeleteMessages** используется для удаления указанного сообщений.</span><span class="sxs-lookup"><span data-stu-id="f1b98-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1b98-158">См. также</span><span class="sxs-lookup"><span data-stu-id="f1b98-158">See also</span></span>



[<span data-ttu-id="f1b98-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f1b98-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="f1b98-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="f1b98-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="f1b98-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f1b98-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="f1b98-162">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="f1b98-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f1b98-163">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="f1b98-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

