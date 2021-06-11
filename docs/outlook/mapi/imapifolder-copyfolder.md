---
title: IMAPIFolderCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyFolder
api_type:
- COM
ms.assetid: 2c1c25c6-1aec-4d9e-a2a3-bf1b4a2908b8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d9c1e88b12baf50593212a3ae3c02907ce6617b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425661"
---
# <a name="imapifoldercopyfolder"></a><span data-ttu-id="05719-103">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="05719-103">IMAPIFolder::CopyFolder</span></span>

  
  
<span data-ttu-id="05719-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05719-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05719-105">Копирует или перемещает подмостки.</span><span class="sxs-lookup"><span data-stu-id="05719-105">Copies or moves a subfolder.</span></span>
  
```cpp
HRESULT CopyFolder(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  LPSTR lpszNewFolderName,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="05719-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="05719-106">Parameters</span></span>

 <span data-ttu-id="05719-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="05719-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="05719-108">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="05719-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="05719-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="05719-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="05719-110">[in] Указатель на идентификатор записи подмостка для копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="05719-110">[in] A pointer to the entry identifier of the subfolder to copy or move.</span></span>
    
 <span data-ttu-id="05719-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="05719-111">_lpInterface_</span></span>
  
> <span data-ttu-id="05719-112">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к папке, на которую указывает параметр _lpDestFolder._</span><span class="sxs-lookup"><span data-stu-id="05719-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that the  _lpDestFolder_ parameter points to.</span></span> <span data-ttu-id="05719-113">Передача NULL заставляет поставщика услуг возвращать стандартный интерфейс папки [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="05719-113">Passing NULL causes the service provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="05719-114">Допустимые значения  _для lpInterface_ включают IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer и IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="05719-114">Valid values for  _lpInterface_ include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="05719-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="05719-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="05719-116">[in] Указатель на открытую папку для получения скопированной или перемещенной подмостки.</span><span class="sxs-lookup"><span data-stu-id="05719-116">[in] A pointer to the open folder to receive the copied or moved subfolder.</span></span>
    
 <span data-ttu-id="05719-117">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="05719-117">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="05719-118">[in] Указатель на имя скопированной или перемещенной папки в новом пункте назначения.</span><span class="sxs-lookup"><span data-stu-id="05719-118">[in] A pointer to the name of the copied or moved folder in its new destination.</span></span> <span data-ttu-id="05719-119">Если  _для lpszNewFolderName_ установлено имя NULL, для имени папки назначения используется имя подмостка источника.</span><span class="sxs-lookup"><span data-stu-id="05719-119">If  _lpszNewFolderName_ is set to NULL, the name of the source subfolder is used for the name of the destination folder.</span></span> 
    
 <span data-ttu-id="05719-120">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="05719-120">_ulUIParam_</span></span>
  
> <span data-ttu-id="05719-121">[in] Ручка родительского окна индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="05719-121">[in] A handle to the parent window of the progress indicator.</span></span> <span data-ttu-id="05719-122">Параметр _ulUIParam_ игнорируется, если FOLDER_DIALOG флаг в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="05719-122">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag in the  _ulFlags_ parameter is set.</span></span> 
    
 <span data-ttu-id="05719-123">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="05719-123">_lpProgress_</span></span>
  
> <span data-ttu-id="05719-124">[in] Указатель на объект progress, отображает индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="05719-124">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="05719-125">Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI.</span><span class="sxs-lookup"><span data-stu-id="05719-125">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="05719-126">Параметр  _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="05719-126">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="05719-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05719-127">_ulFlags_</span></span>
  
> <span data-ttu-id="05719-128">[in] Битмашка флагов, которые контролируют операцию копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="05719-128">[in] A bitmask of flags that controls the copy or move operation.</span></span> <span data-ttu-id="05719-129">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="05719-129">The following flags can be set:</span></span>
    
<span data-ttu-id="05719-130">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="05719-130">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="05719-131">Все подмостки в подмостке, которые будут скопированы, также должны быть скопированы.</span><span class="sxs-lookup"><span data-stu-id="05719-131">All of the subfolders in the subfolder to be copied should also be copied.</span></span> <span data-ttu-id="05719-132">Если COPY_SUBFOLDERS не задан для операции копирования, копируется только подмостки, идентифицированные _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="05719-132">When COPY_SUBFOLDERS is not set for a copy operation, only the subfolder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="05719-133">При операции перемещения поведение COPY_SUBFOLDERS по умолчанию независимо от того, установлен ли флаг.</span><span class="sxs-lookup"><span data-stu-id="05719-133">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="05719-134">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="05719-134">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="05719-135">Запрашивает отображение индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="05719-135">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="05719-136">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="05719-136">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="05719-137">Подмостки должны быть перемещены вместо копирования.</span><span class="sxs-lookup"><span data-stu-id="05719-137">The subfolder is to be moved instead of copied.</span></span> <span data-ttu-id="05719-138">Если FOLDER_MOVE не установлен, подмостки копируется.</span><span class="sxs-lookup"><span data-stu-id="05719-138">If FOLDER_MOVE is not set, the subfolder is copied.</span></span>
    
<span data-ttu-id="05719-139">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="05719-139">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="05719-140">Информирует поставщика магазина сообщений о том, что если он реализует метод **CopyFolder,** назвав [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) или [IMAPISupport::D oCopyProps,](imapisupport-docopyprops.md) **copyFolder** должен немедленно вернуться MAPI_E_DECLINE_COPY.</span><span class="sxs-lookup"><span data-stu-id="05719-140">Informs the message store provider that if it implements **CopyFolder** by calling its support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method, **CopyFolder** should instead immediately return MAPI_E_DECLINE_COPY.</span></span> 
    
<span data-ttu-id="05719-141">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05719-141">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="05719-142">Имя папки назначения находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="05719-142">The name of the destination folder is in Unicode format.</span></span> <span data-ttu-id="05719-143">Если флаг MAPI_UNICODE не установлен, имя папки находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="05719-143">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="05719-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05719-144">Return value</span></span>

<span data-ttu-id="05719-145">S_OK</span><span class="sxs-lookup"><span data-stu-id="05719-145">S_OK</span></span> 
  
> <span data-ttu-id="05719-146">Указанная папка успешно скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="05719-146">The specified folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="05719-147">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="05719-147">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="05719-148">Либо был MAPI_UNICODE флаг, а поставщик магазина сообщений не поддерживает Unicode, либо MAPI_UNICODE не установлен, а поставщик магазина сообщений поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="05719-148">Either the MAPI_UNICODE flag was set and the message store provider does not support Unicode, or MAPI_UNICODE was not set and the message store provider supports only Unicode.</span></span>
    
<span data-ttu-id="05719-149">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="05719-149">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="05719-150">Имя перемещаемой или копируется папки так же, как и имя подмостка в папке назначения.</span><span class="sxs-lookup"><span data-stu-id="05719-150">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="05719-151">Поставщику магазина сообщений требуются уникальные имена папок.</span><span class="sxs-lookup"><span data-stu-id="05719-151">The message store provider requires unique folder names.</span></span>
    
<span data-ttu-id="05719-152">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="05719-152">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="05719-153">Поставщик реализует этот метод, вызывая метод объекта поддержки, и вызыватель передал флаг MAPI_DECLINE_OK.</span><span class="sxs-lookup"><span data-stu-id="05719-153">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="05719-154">MAPI_E_FOLDER_CYCLE</span><span class="sxs-lookup"><span data-stu-id="05719-154">MAPI_E_FOLDER_CYCLE</span></span> 
  
> <span data-ttu-id="05719-155">Папка источника прямо или косвенно содержит папку назначения.</span><span class="sxs-lookup"><span data-stu-id="05719-155">The source folder directly or indirectly contains the destination folder.</span></span> <span data-ttu-id="05719-156">Перед обнаружением этого условия, возможно, была выполнена значительная работа, поэтому папка источника и назначения может быть частично изменена.</span><span class="sxs-lookup"><span data-stu-id="05719-156">Significant work may have been performed before this condition was discovered, so the source and destination folder may be partially modified.</span></span> 
    
<span data-ttu-id="05719-157">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="05719-157">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="05719-158">Вызов удался, но не все записи были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="05719-158">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="05719-159">Когда это предупреждение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="05719-159">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="05719-160">Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="05719-160">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="05719-161">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="05719-161">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05719-162">Примечания</span><span class="sxs-lookup"><span data-stu-id="05719-162">Remarks</span></span>

<span data-ttu-id="05719-163">Метод **IMAPIFolder::CopyFolder** копирует или перемещает подмостки из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="05719-163">The **IMAPIFolder::CopyFolder** method copies or moves a subfolder from one location to another.</span></span> <span data-ttu-id="05719-164">Скопированная или перемещенная подмостка добавляется в папку назначения в качестве подмостков.</span><span class="sxs-lookup"><span data-stu-id="05719-164">The subfolder being copied or moved is added to the destination folder as a subfolder.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="05719-165">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="05719-165">Notes to implementers</span></span>

<span data-ttu-id="05719-166">Если операция копирования или перемещения включает в себя несколько папок, как указывается при установке флага COPY_SUBFOLDERS, выполните операцию как можно более полной для каждой папки.</span><span class="sxs-lookup"><span data-stu-id="05719-166">When the copy or move operation involves more than one folder, as indicated by setting the COPY_SUBFOLDERS flag, perform the operation as completely as possible for each folder.</span></span> <span data-ttu-id="05719-167">Иногда одна из папок, которые будут перемещены или скопированы, не существует или уже перемещена или скопирована в другом месте.</span><span class="sxs-lookup"><span data-stu-id="05719-167">Sometimes one of the folders to be moved or copied does not exist or has already been moved or copied elsewhere.</span></span> <span data-ttu-id="05719-168">Не останавливайте операцию преждевременно, если не произойдет сбой, неподконтрольный вам, например из-за потери памяти, потери дискового пространства или повреждения в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="05719-168">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="05719-169">Попробуйте сохранить все идентификаторы записи сообщений в скопированные сообщения.</span><span class="sxs-lookup"><span data-stu-id="05719-169">Try to retain all message entry identifiers in the copied messages.</span></span> <span data-ttu-id="05719-170">Кроме того, следует попытаться сохранить идентификаторы записей, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="05719-170">You should also try to preserve entry identifiers, but it is not required.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="05719-171">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="05719-171">Notes to callers</span></span>

<span data-ttu-id="05719-172">Ожидайте этих значений возврата в следующих условиях.</span><span class="sxs-lookup"><span data-stu-id="05719-172">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="05719-173">**Condition**</span><span class="sxs-lookup"><span data-stu-id="05719-173">**Condition**</span></span>|<span data-ttu-id="05719-174">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="05719-174">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05719-175">**CopyFolder** успешно копирует или перемещает каждое сообщение и подмостки.</span><span class="sxs-lookup"><span data-stu-id="05719-175">**CopyFolder** has successfully copied or moved every message and subfolder.</span></span>  <br/> |<span data-ttu-id="05719-176">S_OK</span><span class="sxs-lookup"><span data-stu-id="05719-176">S_OK</span></span>  <br/> |
|<span data-ttu-id="05719-177">**CopyFolder** не удалось успешно скопировать или переместить каждое сообщение и подмостки.</span><span class="sxs-lookup"><span data-stu-id="05719-177">**CopyFolder** was unable to successfully copy or move every message and subfolder.</span></span>  <br/> |<span data-ttu-id="05719-178">MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="05719-178">MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND</span></span>  <br/> |
|<span data-ttu-id="05719-179">**CopyFolder** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="05719-179">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="05719-180">Любое значение ошибки, кроме MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="05719-180">Any error value except MAPI_E_NOT_FOUND</span></span>  <br/> |
   
<span data-ttu-id="05719-181">Если **copyFolder** не удается выполнить, не думайте, что работы не было сделано.</span><span class="sxs-lookup"><span data-stu-id="05719-181">When **CopyFolder** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="05719-182">**CopyFolder,** возможно, удалось скопировать или переместить один или несколько сообщений и подмостков, прежде чем столкнуться с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="05719-182">**CopyFolder** might have been able to copy or move one or more of the messages and subfolders before encountering the error.</span></span> 
  
<span data-ttu-id="05719-183">Если идентификатор записи для папки, которая не существует, передается в  _lpEntryID,_ **copyFolder** возвращает MAPI_W_PARTIAL_COMPLETION или MAPI_E_NOT_FOUND, в зависимости от реализации магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="05719-183">If an entry identifier for a folder that does not exist is passed in  _lpEntryID_, **CopyFolder** returns MAPI_W_PARTIAL_COMPLETION or MAPI_E_NOT_FOUND, depending on the message store's implementation.</span></span> 
  
<span data-ttu-id="05719-184">В зависимости от поставщика магазина сообщений идентификатор записи исходного сообщения может сохраняться или не сохраняться в скопированном сообщении.</span><span class="sxs-lookup"><span data-stu-id="05719-184">Depending on the message store provider, the entry identifier of the original message may or may not be preserved in the copied message.</span></span> <span data-ttu-id="05719-185">Идентификаторы записей следует сохранять по мере возможности, но это не является требованием.</span><span class="sxs-lookup"><span data-stu-id="05719-185">You should preserve entry identifiers whenever possible, but it is not a requirement.</span></span> <span data-ttu-id="05719-186">Обычно можно зависеть от следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="05719-186">You can generally depend on the following scenarios:</span></span>
  
- <span data-ttu-id="05719-187">При перемещениях папки между двумя разными типами магазинов сообщений идентификатор записи гарантированно изменится.</span><span class="sxs-lookup"><span data-stu-id="05719-187">When you move a folder between two different types of message stores, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="05719-188">При перемещениях папки между двумя хранилищами сообщений одного типа идентификатор записи почти всегда изменяется.</span><span class="sxs-lookup"><span data-stu-id="05719-188">When you move a folder between two message stores of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="05719-189">При перемещение папки в другое расположение в том же хранилище сообщений идентификатор записи может изменяться или не изменяться в зависимости от поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="05719-189">When you move a folder to another location in the same message store, the entry identifier may or may not change, depending on the message store provider.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="05719-190">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="05719-190">MFCMAPI reference</span></span>

<span data-ttu-id="05719-191">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="05719-191">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="05719-192">**Файл**</span><span class="sxs-lookup"><span data-stu-id="05719-192">**File**</span></span>|<span data-ttu-id="05719-193">**Функция**</span><span class="sxs-lookup"><span data-stu-id="05719-193">**Function**</span></span>|<span data-ttu-id="05719-194">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="05719-194">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="05719-195">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="05719-195">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="05719-196">CMsgStoreDlg::OnPasteFolder</span><span class="sxs-lookup"><span data-stu-id="05719-196">CMsgStoreDlg::OnPasteFolder</span></span>  <br/> |<span data-ttu-id="05719-197">MFCMAPI использует **метод IMAPIFolder::CopyFolder** для копирования папок из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="05719-197">MFCMAPI uses the **IMAPIFolder::CopyFolder** method to copy folders from one location to another.</span></span> <span data-ttu-id="05719-198">MFCMAPI запоминает исходные папки во время операции копирования и фактически выполняет копию во время операции вклейки.</span><span class="sxs-lookup"><span data-stu-id="05719-198">MFCMAPI remembers the source folder during the copy operation and actually performs the copy during the paste operation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05719-199">См. также</span><span class="sxs-lookup"><span data-stu-id="05719-199">See also</span></span>



[<span data-ttu-id="05719-200">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="05719-200">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="05719-201">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="05719-201">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

