---
title: IMAPISupportCopyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyFolder
api_type:
- COM
ms.assetid: c2e0939f-0668-473f-856c-a27af094070b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 11ee944a14f8c9bd881b9c79a4ce66817275e73a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420887"
---
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="205a9-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="205a9-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="205a9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="205a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="205a9-105">Копирует или перемещает папку из текущей родительской папки в другую родительную папку.</span><span class="sxs-lookup"><span data-stu-id="205a9-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
```cpp
HRESULT CopyFolder(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
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

## <a name="parameters"></a><span data-ttu-id="205a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="205a9-106">Parameters</span></span>

 <span data-ttu-id="205a9-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="205a9-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="205a9-108">[in] Указатель на идентификатор интерфейса , который представляет интерфейс, используемый для доступа к родительской папке папки для копирования или перемещений.</span><span class="sxs-lookup"><span data-stu-id="205a9-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="205a9-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="205a9-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="205a9-110">[in] Указатель на родительская папка папки, которая должна быть скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="205a9-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="205a9-111">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="205a9-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="205a9-112">[in] Количество byte в идентификаторе записи, на который указывает _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="205a9-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="205a9-113">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="205a9-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="205a9-114">[in] Указатель на идентификатор записи папки, которая должна быть скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="205a9-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="205a9-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="205a9-115">_lpInterface_</span></span>
  
> <span data-ttu-id="205a9-116">[in] Зарезервировано; должно быть NULL.</span><span class="sxs-lookup"><span data-stu-id="205a9-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="205a9-117">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="205a9-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="205a9-118">[in] Указатель на папку, которая должна быть скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="205a9-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="205a9-119">_lpszNewFolderName_</span><span class="sxs-lookup"><span data-stu-id="205a9-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="205a9-120">[in] Указатель на имя скопированной или перемещенной папки; в противном случае NULL указывает, что скопированная или перемещенная папка должна иметь то же имя, что и у папки источника (папка, на которую указывает _lpEntryID)._</span><span class="sxs-lookup"><span data-stu-id="205a9-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="205a9-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="205a9-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="205a9-122">[in] Handle of the window for the progress indicator dialog box and related windows.</span><span class="sxs-lookup"><span data-stu-id="205a9-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="205a9-123">Параметр  _ulUIParam_ игнорируется, если FOLDER_DIALOG в параметре  _ulFlags_ не задан флаг FOLDER_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="205a9-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="205a9-124">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="205a9-124">_lpProgress_</span></span>
  
> <span data-ttu-id="205a9-125">[in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="205a9-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="205a9-126">Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="205a9-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="205a9-127">Параметр _lpProgress_ игнорируется, если флаг FOLDER_DIALOG не установлен в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="205a9-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="205a9-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="205a9-128">_ulFlags_</span></span>
  
> <span data-ttu-id="205a9-129">[in] Битоваяmas флагов, которая управляет выполнением операции копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="205a9-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="205a9-130">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="205a9-130">The following flags can be set:</span></span>
    
<span data-ttu-id="205a9-131">COPY_SUBFOLDERS</span><span class="sxs-lookup"><span data-stu-id="205a9-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="205a9-132">Все вложенные папки папки должны быть скопированы или перемещены.</span><span class="sxs-lookup"><span data-stu-id="205a9-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="205a9-133">Если COPY_SUBFOLDERS не задан для операции копирования, копируется только папка, заданная _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="205a9-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="205a9-134">При операции перемещения поведение COPY_SUBFOLDERS по умолчанию независимо от того, установлен ли флаг.</span><span class="sxs-lookup"><span data-stu-id="205a9-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="205a9-135">FOLDER_DIALOG</span><span class="sxs-lookup"><span data-stu-id="205a9-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="205a9-136">Запрашивает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="205a9-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="205a9-137">FOLDER_MOVE</span><span class="sxs-lookup"><span data-stu-id="205a9-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="205a9-138">Папка должна быть перемещена вместо копирования.</span><span class="sxs-lookup"><span data-stu-id="205a9-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="205a9-139">Если FOLDER_MOVE не установлен, папка копируется.</span><span class="sxs-lookup"><span data-stu-id="205a9-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="205a9-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="205a9-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="205a9-141">Имя папки имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="205a9-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="205a9-142">Если флаг MAPI_UNICODE не установлен, имя папки будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="205a9-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="205a9-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="205a9-143">Return value</span></span>

<span data-ttu-id="205a9-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="205a9-144">S_OK</span></span> 
  
> <span data-ttu-id="205a9-145">Папка успешно скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="205a9-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="205a9-146">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="205a9-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="205a9-147">Имя перемещаемой или копируется папки так же, как и имя вложенной папки в конечной папке.</span><span class="sxs-lookup"><span data-stu-id="205a9-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="205a9-148">Поставщику store сообщений требуется, чтобы имена папок были уникальными.</span><span class="sxs-lookup"><span data-stu-id="205a9-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="205a9-149">Операция останавливается без завершения.</span><span class="sxs-lookup"><span data-stu-id="205a9-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="205a9-150">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="205a9-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="205a9-151">Вызов был успешным, но не все записи были успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="205a9-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="205a9-152">При возвращении этого предупреждения вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="205a9-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="205a9-153">Чтобы проверить это предупреждение, используйте **макрос HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="205a9-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="205a9-154">Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="205a9-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="205a9-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="205a9-155">Remarks</span></span>

<span data-ttu-id="205a9-156">Метод **IMAPISupport::CopyFolder** реализован для объектов поддержки поставщика хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="205a9-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="205a9-157">Поставщики store сообщений могут вызывать **IMAPISupport::CopyFolder** в своей реализации [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) для копирования или перемещения одной папки из одной родительской папки в другую.</span><span class="sxs-lookup"><span data-stu-id="205a9-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="205a9-158">**IMAPISupport::CopyFolder** добавляет скопированную или перемещенную папку в качестве вложенной папки назначения.</span><span class="sxs-lookup"><span data-stu-id="205a9-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="205a9-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="205a9-159">Notes to callers</span></span>

 <span data-ttu-id="205a9-160">**IMAPISupport::CopyFolder** позволяет одновременно переименовывание и перемещение папок, а также копирование или перемещение вложенных папок затронутой папки.</span><span class="sxs-lookup"><span data-stu-id="205a9-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="205a9-161">Чтобы скопировать или переместить все вложенные папки, вложенные в скопированную или перемещенную папку, передав флаг COPY_SUBFOLDERS в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="205a9-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="205a9-162">При следующих условиях следует ожидать следующих возвращаемых значений:</span><span class="sxs-lookup"><span data-stu-id="205a9-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="205a9-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="205a9-163">**Condition**</span></span>|<span data-ttu-id="205a9-164">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="205a9-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="205a9-165">**CopyFolder** успешно скопировал или переместил папку и все ее вложенные папки, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="205a9-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="205a9-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="205a9-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="205a9-167">**CopyFolder** не удалось успешно скопировать или переместить все папки.</span><span class="sxs-lookup"><span data-stu-id="205a9-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="205a9-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="205a9-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="205a9-169">**CopyFolder** не удалось завершить.</span><span class="sxs-lookup"><span data-stu-id="205a9-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="205a9-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="205a9-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="205a9-171">Если **CopyFolder** возвращает значение ошибки, не переходите к предположению о том, что работа не была сделана.</span><span class="sxs-lookup"><span data-stu-id="205a9-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="205a9-172">Одна или несколько папок могли быть скопированы или перемещены до того, как **в CopyFolder** сбой.</span><span class="sxs-lookup"><span data-stu-id="205a9-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="205a9-173">См. также</span><span class="sxs-lookup"><span data-stu-id="205a9-173">See also</span></span>



[<span data-ttu-id="205a9-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="205a9-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

