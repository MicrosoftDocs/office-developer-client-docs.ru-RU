---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808847"
---
# <a name="imapifolderdeletefolder"></a><span data-ttu-id="2037b-103">IMAPIFolder::DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="2037b-103">IMAPIFolder::DeleteFolder</span></span>

  
  
<span data-ttu-id="2037b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2037b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2037b-105">Удаляет вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="2037b-105">Deletes a subfolder.</span></span>
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2037b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2037b-106">Parameters</span></span>

 <span data-ttu-id="2037b-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="2037b-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="2037b-108">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2037b-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="2037b-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="2037b-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="2037b-110">[in] Указатель на идентификатор записи вложенную папку для удаления.</span><span class="sxs-lookup"><span data-stu-id="2037b-110">[in] A pointer to the entry identifier of the subfolder to delete.</span></span>
    
 <span data-ttu-id="2037b-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2037b-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="2037b-112">[in] Дескриптор родительского окна индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2037b-112">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="2037b-113">Параметр _ulUIParam_ игнорируется, пока флаг FOLDER_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="2037b-113">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="2037b-114">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2037b-114">_lpProgress_</span></span>
  
> <span data-ttu-id="2037b-115">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2037b-115">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2037b-116">Если в _lpProgress_передается значение NULL, поставщика хранилища сообщений отображает индикатор выполнения с помощью реализация объекта MAPI хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2037b-116">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2037b-117">Параметр _lpProgress_ используется только флаг FOLDER_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="2037b-117">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2037b-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2037b-118">_ulFlags_</span></span>
  
> <span data-ttu-id="2037b-119">[in] Битовая маска флаги, который управляет удаления вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="2037b-119">[in] A bitmask of flags that controls the deletion of the subfolder.</span></span> <span data-ttu-id="2037b-120">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="2037b-120">The following flags can be set:</span></span>
    
<span data-ttu-id="2037b-121">DEL_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="2037b-121">DEL_FOLDERS</span></span> 
  
> <span data-ttu-id="2037b-122">Следует удалить все вложенные папки вложенной папке, на который указывает _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2037b-122">All subfolders of the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="2037b-123">DEL_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="2037b-123">DEL_MESSAGES</span></span> 
  
> <span data-ttu-id="2037b-124">Следует удалить все сообщения в папке, на который указывает _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="2037b-124">All messages in the subfolder pointed to by  _lpEntryID_ should be deleted.</span></span> 
    
<span data-ttu-id="2037b-125">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2037b-125">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="2037b-126">Индикатор выполнения должен отображаться во время операции.</span><span class="sxs-lookup"><span data-stu-id="2037b-126">A progress indicator should be displayed while the operation proceeds.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2037b-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="2037b-128">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2037b-128">S_OK</span></span> 
  
> <span data-ttu-id="2037b-129">Указанная папка успешно удален.</span><span class="sxs-lookup"><span data-stu-id="2037b-129">The specified folder has been successfully deleted.</span></span>
    
<span data-ttu-id="2037b-130">MAPI_E_HAS_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="2037b-130">MAPI_E_HAS_FOLDERS</span></span> 
  
> <span data-ttu-id="2037b-131">Вложенной папке удаления содержит вложенные папки, не был установлен флажок DEL_FOLDERS.</span><span class="sxs-lookup"><span data-stu-id="2037b-131">The subfolder being deleted contains subfolders, and the DEL_FOLDERS flag was not set.</span></span> <span data-ttu-id="2037b-132">Вложенные папки не были удалены.</span><span class="sxs-lookup"><span data-stu-id="2037b-132">The subfolders were not deleted.</span></span>
    
<span data-ttu-id="2037b-133">MAPI_E_HAS_MESSAGES</span><span class="sxs-lookup"><span data-stu-id="2037b-133">MAPI_E_HAS_MESSAGES</span></span> 
  
> <span data-ttu-id="2037b-134">Вложенной папке удаления содержит сообщения, а не был установлен флажок DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="2037b-134">The subfolder being deleted contains messages, and the DEL_MESSAGES flag was not set.</span></span> <span data-ttu-id="2037b-135">Вложенной папке не был удален.</span><span class="sxs-lookup"><span data-stu-id="2037b-135">The subfolder was not deleted.</span></span>
    
<span data-ttu-id="2037b-136">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="2037b-136">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="2037b-137">Вызов завершился успешно, но не все записи были успешно удалены.</span><span class="sxs-lookup"><span data-stu-id="2037b-137">The call succeeded, but not all of the entries were successfully deleted.</span></span> <span data-ttu-id="2037b-138">При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="2037b-138">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="2037b-139">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="2037b-139">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="2037b-140">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="2037b-140">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2037b-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="2037b-141">Remarks</span></span>

<span data-ttu-id="2037b-142">Метод **IMAPIFolder::DeleteFolder** удаляет вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="2037b-142">The **IMAPIFolder::DeleteFolder** method deletes a subfolder.</span></span> <span data-ttu-id="2037b-143">По умолчанию **DeleteFolder** работает только для пустых папок, но можно использовать его успешно непустые папок, задав два флага: DEL_FOLDERS и DEL_MESSAGES.</span><span class="sxs-lookup"><span data-stu-id="2037b-143">By default, **DeleteFolder** operates only on empty folders, but you can use it successfully on non-empty folders by setting two flags: DEL_FOLDERS and DEL_MESSAGES.</span></span> <span data-ttu-id="2037b-144">Можно удалить только пустые папки или папки, которые установить флаги DEL_FOLDERS и DEL_MESSAGES на вызов **DeleteFolder** .</span><span class="sxs-lookup"><span data-stu-id="2037b-144">Only empty folders or folders that set both the DEL_FOLDERS and DEL_MESSAGES flags on the **DeleteFolder** call can be deleted.</span></span> <span data-ttu-id="2037b-145">DEL_FOLDERS включает все вложенные папки удаляется; DEL_MESSAGES включает все сообщения в папке требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="2037b-145">DEL_FOLDERS enables all of the folder's subfolders to be removed; DEL_MESSAGES enables all of the folder's messages to be removed.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2037b-146">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2037b-146">Notes to implementers</span></span>

<span data-ttu-id="2037b-147">При операции удаления состоит из нескольких папок, как можно выполните операцию для каждой папки.</span><span class="sxs-lookup"><span data-stu-id="2037b-147">When the delete operation involves more than one folder, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="2037b-148">В некоторых случаях один из папки к удалению не существует или был перемещен или скопирован в другое место.</span><span class="sxs-lookup"><span data-stu-id="2037b-148">Sometimes one of the folders to be deleted does not exist or has been moved or copied elsewhere.</span></span> <span data-ttu-id="2037b-149">Не останавливайте операции преждевременно Если произошла ошибка, которая находится за пределами элементу управления, такие как хватает памяти, недостаточно места на диске или повреждение в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="2037b-149">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2037b-150">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2037b-150">Notes to callers</span></span>

<span data-ttu-id="2037b-151">Ожидается, что эти возвращаемые значения в следующих случаях.</span><span class="sxs-lookup"><span data-stu-id="2037b-151">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="2037b-152">**Условие**</span><span class="sxs-lookup"><span data-stu-id="2037b-152">**Condition**</span></span>|<span data-ttu-id="2037b-153">**������������ ��������**</span><span class="sxs-lookup"><span data-stu-id="2037b-153">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2037b-154">**DeleteFolder** успешно удалил все сообщения и вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="2037b-154">**DeleteFolder** has successfully deleted every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2037b-155">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2037b-155">S_OK</span></span>  <br/> |
|<span data-ttu-id="2037b-156">**DeleteFolder** не удалось успешно удалить все сообщения и вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="2037b-156">**DeleteFolder** was unable to successfully delete every message and subfolder.</span></span>  <br/> |<span data-ttu-id="2037b-157">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2037b-157">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="2037b-158">Не удалось завершить **DeleteFolder** .</span><span class="sxs-lookup"><span data-stu-id="2037b-158">**DeleteFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="2037b-159">Любое значение ошибки, за исключением MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2037b-159">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="2037b-160">Если не удается завершить **DeleteFolder** не предполагают, что работа не выполнена.</span><span class="sxs-lookup"><span data-stu-id="2037b-160">When **DeleteFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="2037b-161">**DeleteFolder** мог удалить одно или несколько сообщений и вложенные папки до появления ошибки.</span><span class="sxs-lookup"><span data-stu-id="2037b-161">**DeleteFolder** might have been able to delete one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="2037b-162">Если не удается удалить один или несколько вложенных папок, **DeleteFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2037b-162">If one or more subfolders cannot be deleted, **DeleteFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store provider's implementation.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2037b-163">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="2037b-163">MFCMAPI reference</span></span>

<span data-ttu-id="2037b-164">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="2037b-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2037b-165">**����**</span><span class="sxs-lookup"><span data-stu-id="2037b-165">**File**</span></span>|<span data-ttu-id="2037b-166">**�������**</span><span class="sxs-lookup"><span data-stu-id="2037b-166">**Function**</span></span>|<span data-ttu-id="2037b-167">**�����������**</span><span class="sxs-lookup"><span data-stu-id="2037b-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2037b-168">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2037b-168">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="2037b-169">CMsgStoreDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="2037b-169">CMsgStoreDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="2037b-170">Mfcmapi (en) метод **IMAPIFolder::DeleteFolder** используется для удаления папок.</span><span class="sxs-lookup"><span data-stu-id="2037b-170">MFCMAPI uses the **IMAPIFolder::DeleteFolder** method to delete folders.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2037b-171">См. также</span><span class="sxs-lookup"><span data-stu-id="2037b-171">See also</span></span>



[<span data-ttu-id="2037b-172">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2037b-172">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="2037b-173">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2037b-173">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

