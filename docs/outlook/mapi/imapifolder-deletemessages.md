---
title: имапифолдерделетемессажес
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
# <a name="imapifolderdeletemessages"></a><span data-ttu-id="efd82-103">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="efd82-103">IMAPIFolder::DeleteMessages</span></span>

  
  
<span data-ttu-id="efd82-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efd82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efd82-105">Удаляет одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="efd82-105">Deletes one or more messages.</span></span>
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="efd82-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efd82-106">Parameters</span></span>

 <span data-ttu-id="efd82-107">_лпмсглист_</span><span class="sxs-lookup"><span data-stu-id="efd82-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="efd82-108">возврата Указатель на структуру [ентрилист](entrylist.md) , которая содержит количество сообщений, которые необходимо удалить, и массив структуры [EntryID](entryid.md) , определяющих сообщения.</span><span class="sxs-lookup"><span data-stu-id="efd82-108">[in] A pointer to an [ENTRYLIST](entrylist.md) structure that contains the number of messages to delete and an array of [ENTRYID](entryid.md) structures that identify the messages.</span></span> 
    
 <span data-ttu-id="efd82-109">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="efd82-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="efd82-110">возврата Дескриптор родительского окна индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="efd82-110">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="efd82-111">Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг MESSAGE_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="efd82-111">The  _ulUIParam_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="efd82-112">_лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="efd82-112">_lpProgress_</span></span>
  
> <span data-ttu-id="efd82-113">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="efd82-113">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="efd82-114">Если в _лппрогресс_передается значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="efd82-114">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="efd82-115">Параметр _лппрогресс_ игнорируется, если в параметре _ulFlags_ не задан флаг MESSAGE_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="efd82-115">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="efd82-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efd82-116">_ulFlags_</span></span>
  
> <span data-ttu-id="efd82-117">возврата Битовая маска флагов, определяющих способ удаления сообщений.</span><span class="sxs-lookup"><span data-stu-id="efd82-117">[in] A bitmask of flags that controls how the messages are deleted.</span></span> <span data-ttu-id="efd82-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="efd82-118">The following flags can be set:</span></span>
    
<span data-ttu-id="efd82-119">DELETE_HARD_DELETE</span><span class="sxs-lookup"><span data-stu-id="efd82-119">DELETE_HARD_DELETE</span></span>
  
> <span data-ttu-id="efd82-120">Окончательно удаляет все сообщения, включая обратимо удаленные.</span><span class="sxs-lookup"><span data-stu-id="efd82-120">Permanently removes all messages, including soft-deleted ones.</span></span>
    
<span data-ttu-id="efd82-121">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="efd82-121">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="efd82-122">Отображает индикатор хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="efd82-122">Displays a progress indicator as the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efd82-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efd82-123">Return value</span></span>

<span data-ttu-id="efd82-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="efd82-124">S_OK</span></span> 
  
> <span data-ttu-id="efd82-125">Указанное сообщение или сообщения были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="efd82-125">The specified message or messages were successfully deleted.</span></span>
    
<span data-ttu-id="efd82-126">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="efd82-126">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="efd82-127">Вызов выполнен успешно, но не все сообщения были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="efd82-127">The call succeeded, but not all of the messages were successfully deleted.</span></span> <span data-ttu-id="efd82-128">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="efd82-128">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="efd82-129">Чтобы проверить это предупреждение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="efd82-129">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="efd82-130">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="efd82-130">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="efd82-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="efd82-131">Remarks</span></span>

<span data-ttu-id="efd82-132">Метод **IMAPIFolder::D елетемессажес** удаляет сообщения из папки.</span><span class="sxs-lookup"><span data-stu-id="efd82-132">The **IMAPIFolder::DeleteMessages** method deletes messages from a folder.</span></span> <span data-ttu-id="efd82-133">Сообщения, которые не существуют, перемещены в другое место, открыты с разрешением на чтение и запись или которые уже отправлены, невозможно удалить.</span><span class="sxs-lookup"><span data-stu-id="efd82-133">Messages that do not exist, that have been moved elsewhere, that are open with read/write permission, or that are currently submitted cannot be deleted.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="efd82-134">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="efd82-134">Notes to implementers</span></span>

<span data-ttu-id="efd82-135">Если операция удаления содержит более одного сообщения, выполните операцию как можно скорее для каждой папки, даже если не удается удалить одно или несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="efd82-135">When the delete operation involves more than one message, perform the operation as completely as possible for each folder, even if one or more of the messages cannot be deleted.</span></span> <span data-ttu-id="efd82-136">Не прекращайте выполнение операции преждевременно, если не произойдет сбой, который выходит за рамки элемента управления, например, не хватает памяти, не хватает места на диске или повреждено хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="efd82-136">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="efd82-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="efd82-137">Notes to callers</span></span>

<span data-ttu-id="efd82-138">Эти возвращаемые значения следует ожидать при соблюдении следующих условий.</span><span class="sxs-lookup"><span data-stu-id="efd82-138">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="efd82-139">**Условие**</span><span class="sxs-lookup"><span data-stu-id="efd82-139">**Condition**</span></span>|<span data-ttu-id="efd82-140">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="efd82-140">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="efd82-141">**Делетемессажес** успешно удалил каждое сообщение.</span><span class="sxs-lookup"><span data-stu-id="efd82-141">**DeleteMessages** has successfully deleted every message.</span></span>  <br/> |<span data-ttu-id="efd82-142">S_OK</span><span class="sxs-lookup"><span data-stu-id="efd82-142">S_OK</span></span>  <br/> |
|<span data-ttu-id="efd82-143">**Делетемессажес** не удалось удалить все сообщения и вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="efd82-143">**DeleteMessages** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="efd82-144">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="efd82-144">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="efd82-145">**Делетемессажес** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="efd82-145">**DeleteMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="efd82-146">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="efd82-146">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="efd82-147">Если **делетемессажес** не удается выполнить, не следует предполагать, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="efd82-147">When **DeleteMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="efd82-148">Возможно, в **делетемессажес** удалось удалить одно или несколько сообщений, прежде чем возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="efd82-148">**DeleteMessages** might have been able to delete one or more of the messages before encountering the error.</span></span> 
  
 <span data-ttu-id="efd82-149">**Делетемессажес** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="efd82-149">**DeleteMessages** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="efd82-150">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="efd82-150">MFCMAPI reference</span></span>

<span data-ttu-id="efd82-151">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="efd82-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="efd82-152">**Файл**</span><span class="sxs-lookup"><span data-stu-id="efd82-152">**File**</span></span>|<span data-ttu-id="efd82-153">**Функция**</span><span class="sxs-lookup"><span data-stu-id="efd82-153">**Function**</span></span>|<span data-ttu-id="efd82-154">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="efd82-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="efd82-155">Фолдердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="efd82-155">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="efd82-156">Кфолдердлг:: Онделетеселектедитем</span><span class="sxs-lookup"><span data-stu-id="efd82-156">CFolderDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="efd82-157">MFCMAPI использует метод **IMAPIFolder::D елетемессажес** для удаления указанных сообщений.</span><span class="sxs-lookup"><span data-stu-id="efd82-157">MFCMAPI uses the **IMAPIFolder::DeleteMessages** method to delete the specified messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efd82-158">См. также</span><span class="sxs-lookup"><span data-stu-id="efd82-158">See also</span></span>



[<span data-ttu-id="efd82-159">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="efd82-159">ENTRYID</span></span>](entryid.md)
  
[<span data-ttu-id="efd82-160">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="efd82-160">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="efd82-161">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="efd82-161">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="efd82-162">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="efd82-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="efd82-163">Использование макросов для обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="efd82-163">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)

