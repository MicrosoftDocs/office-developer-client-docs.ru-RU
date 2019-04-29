---
title: Имаписуппорткопифолдер
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
# <a name="imapisupportcopyfolder"></a><span data-ttu-id="7a404-103">IMAPISupport::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="7a404-103">IMAPISupport::CopyFolder</span></span>

  
  
<span data-ttu-id="7a404-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a404-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a404-105">Копирует или перемещает папку из текущей родительской папки в другую родительскую папку.</span><span class="sxs-lookup"><span data-stu-id="7a404-105">Copies or moves a folder from its current parent folder to another parent folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7a404-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a404-106">Parameters</span></span>

 <span data-ttu-id="7a404-107">_ЛпсрЦинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="7a404-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="7a404-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к родительской папке копируемого или перемещаемого папки.</span><span class="sxs-lookup"><span data-stu-id="7a404-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the parent folder of the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="7a404-109">_Лпсркфолдер_</span><span class="sxs-lookup"><span data-stu-id="7a404-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="7a404-110">возврата Указатель на родительскую папку копируемого или перемещаемого папки.</span><span class="sxs-lookup"><span data-stu-id="7a404-110">[in] A pointer to the parent folder of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="7a404-111">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="7a404-111">_cbEntryID_</span></span>
  
> <span data-ttu-id="7a404-112">возврата Число байтов в идентификаторе записи, на которое указывает _лпентрид_.</span><span class="sxs-lookup"><span data-stu-id="7a404-112">[in] The byte count in the entry identifier pointed to by  _lpEntryID_.</span></span>
    
 <span data-ttu-id="7a404-113">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="7a404-113">_lpEntryID_</span></span>
  
> <span data-ttu-id="7a404-114">возврата Указатель на идентификатор записи копируемого или перемещаемого папки.</span><span class="sxs-lookup"><span data-stu-id="7a404-114">[in] A pointer to the entry identifier of the folder to be copied or moved.</span></span> 
    
 <span data-ttu-id="7a404-115">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="7a404-115">_lpInterface_</span></span>
  
> <span data-ttu-id="7a404-116">возврата Резервирования должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="7a404-116">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="7a404-117">_Лпдестфолдер_</span><span class="sxs-lookup"><span data-stu-id="7a404-117">_lpDestFolder_</span></span>
  
> <span data-ttu-id="7a404-118">возврата Указатель на папку, которая должна получать копируемую или переместив папку.</span><span class="sxs-lookup"><span data-stu-id="7a404-118">[in] A pointer to the folder that is to receive the folder to be copied or moved.</span></span>
    
 <span data-ttu-id="7a404-119">_Лпсзневфолдернаме_</span><span class="sxs-lookup"><span data-stu-id="7a404-119">_lpszNewFolderName_</span></span>
  
> <span data-ttu-id="7a404-120">возврата Указатель на имя скопированной или перемещенной папки; в противном случае — значение NULL, которое указывает, что имя скопированной или перемещенной папки должно совпадать с именем исходной папки (папкой, на которую указывает _лпентрид_).</span><span class="sxs-lookup"><span data-stu-id="7a404-120">[in] A pointer to the name of the copied or moved folder; otherwise, NULL, which indicates that the copied or moved folder should have the same name as the source folder (the folder pointed to by  _lpEntryID_).</span></span>
    
 <span data-ttu-id="7a404-121">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="7a404-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="7a404-122">возврата Дескриптор окна для диалогового окна "индикатор хода выполнения" и связанные с ним окна.</span><span class="sxs-lookup"><span data-stu-id="7a404-122">[in] A handle of the window for the progress indicator dialog box and related windows.</span></span> <span data-ttu-id="7a404-123">Параметр _улуипарам_ игнорируется, если не установлен флаг фолдер_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="7a404-123">The  _ulUIParam_ parameter is ignored unless the FOLDER_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="7a404-124">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="7a404-124">_lpProgress_</span></span>
  
> <span data-ttu-id="7a404-125">возврата Указатель на объект Progress, который отображает индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7a404-125">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7a404-126">Если в _лппрогресс_переДАЕТСЯ значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI.</span><span class="sxs-lookup"><span data-stu-id="7a404-126">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="7a404-127">Параметр _лппрогресс_ игнорируется, если не установлен флаг Фолдер_диалог в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="7a404-127">The  _lpProgress_ parameter is ignored unless the FOLDER_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7a404-128">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a404-128">_ulFlags_</span></span>
  
> <span data-ttu-id="7a404-129">возврата Битовая маска флагов, определяющих, как выполняется операция копирования или перемещения.</span><span class="sxs-lookup"><span data-stu-id="7a404-129">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="7a404-130">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7a404-130">The following flags can be set:</span></span>
    
<span data-ttu-id="7a404-131">КОПИ_СУБФОЛДЕРС</span><span class="sxs-lookup"><span data-stu-id="7a404-131">COPY_SUBFOLDERS</span></span> 
  
> <span data-ttu-id="7a404-132">Все подпапки папки должны копироваться или перемещаться.</span><span class="sxs-lookup"><span data-stu-id="7a404-132">All of the folder's subfolders should be copied or moved.</span></span> <span data-ttu-id="7a404-133">Если для операции копирования не задано значение КОПИ_СУБФОЛДЕРС, копируется только папка, определенная с помощью _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="7a404-133">When COPY_SUBFOLDERS is not set for a copy operation, only the folder identified by  _lpEntryID_ is copied.</span></span> <span data-ttu-id="7a404-134">При выполнении операции перемещения поведение КОПИ_СУБФОЛДЕРС по умолчанию зависит от того, установлен ли флаг.</span><span class="sxs-lookup"><span data-stu-id="7a404-134">With a move operation, the COPY_SUBFOLDERS behavior is the default regardless of whether the flag is set.</span></span> 
    
<span data-ttu-id="7a404-135">ФОЛДЕР_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="7a404-135">FOLDER_DIALOG</span></span> 
  
> <span data-ttu-id="7a404-136">ЗаПрашивает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7a404-136">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="7a404-137">ФОЛДЕР_МОВЕ</span><span class="sxs-lookup"><span data-stu-id="7a404-137">FOLDER_MOVE</span></span> 
  
> <span data-ttu-id="7a404-138">Вместо копирования папку следует переместить.</span><span class="sxs-lookup"><span data-stu-id="7a404-138">The folder should be moved instead of copied.</span></span> <span data-ttu-id="7a404-139">Если ФОЛДЕР_МОВЕ не задано, то папка копируется.</span><span class="sxs-lookup"><span data-stu-id="7a404-139">If FOLDER_MOVE is not set, the folder is copied.</span></span>
    
<span data-ttu-id="7a404-140">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a404-140">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7a404-141">Имя папки имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="7a404-141">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="7a404-142">Если флаг МАПИ_УНИКОДЕ не установлен, имя папки будет иметь формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="7a404-142">If the MAPI_UNICODE flag is not set, the name of the folder is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a404-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a404-143">Return value</span></span>

<span data-ttu-id="7a404-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a404-144">S_OK</span></span> 
  
> <span data-ttu-id="7a404-145">Папка успешно скопирована или перемещена.</span><span class="sxs-lookup"><span data-stu-id="7a404-145">The folder has been successfully copied or moved.</span></span>
    
<span data-ttu-id="7a404-146">МАПИ_Е_КОЛЛИСИОН</span><span class="sxs-lookup"><span data-stu-id="7a404-146">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="7a404-147">Имя папки, которую вы перемещаете или копирует, совпадает с именем вложенной папки в папке назначения.</span><span class="sxs-lookup"><span data-stu-id="7a404-147">The name of the folder being moved or copied is the same as that of a subfolder in the destination folder.</span></span> <span data-ttu-id="7a404-148">Для поставщика хранилища сообщений необходимо, чтобы имена папок были уникальными.</span><span class="sxs-lookup"><span data-stu-id="7a404-148">The message store provider requires that folder names be unique.</span></span> <span data-ttu-id="7a404-149">Операция завершается без завершения.</span><span class="sxs-lookup"><span data-stu-id="7a404-149">The operation stops without completing.</span></span>
    
<span data-ttu-id="7a404-150">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="7a404-150">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7a404-151">Вызов выполнен успешно, но не все записи успешно скопированы.</span><span class="sxs-lookup"><span data-stu-id="7a404-151">The call succeeded, but not all entries were successfully copied.</span></span> <span data-ttu-id="7a404-152">При возвращении этого предупреждения вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="7a404-152">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7a404-153">Чтобы проверить это предупреждение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="7a404-153">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7a404-154">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7a404-154">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a404-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="7a404-155">Remarks</span></span>

<span data-ttu-id="7a404-156">Метод **имаписуппорт:: CopyFolder** реализован для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7a404-156">The **IMAPISupport::CopyFolder** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="7a404-157">Поставщики хранилищ сообщений могут вызывать **имаписуппорт:: CopyFolder** в реализации [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) для копирования или перемещения одной папки из одной родительской папки в другую.</span><span class="sxs-lookup"><span data-stu-id="7a404-157">Message store providers can call **IMAPISupport::CopyFolder** in their implementation of [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) to copy or move a single folder from one parent folder to another.</span></span> 
  
 <span data-ttu-id="7a404-158">**Имаписуппорт:: CopyFolder** добавляет скопированную или перемещенную папку в качестве вложенной папки целевой папки.</span><span class="sxs-lookup"><span data-stu-id="7a404-158">**IMAPISupport::CopyFolder** adds the copied or moved folder as a subfolder of the destination folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a404-159">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7a404-159">Notes to callers</span></span>

 <span data-ttu-id="7a404-160">**Имаписуппорт:: CopyFolder** разрешает одновременное переименование и перемещение папок, а также копирование или перемещение вложенных папок затронутой папки.</span><span class="sxs-lookup"><span data-stu-id="7a404-160">**IMAPISupport::CopyFolder** allows simultaneous renaming and moving of folders and the copying or moving of subfolders of the affected folder.</span></span> <span data-ttu-id="7a404-161">Чтобы скопировать или переместить все вложенные папки, вложенные в скопированную или перемещенную папку, передайте флаг КОПИ_СУБФОЛДЕРС в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="7a404-161">To copy or move all subfolders nested in the copied or moved folder, pass the COPY_SUBFOLDERS flag in  _ulFlags_.</span></span> 
  
<span data-ttu-id="7a404-162">Ожидаются следующие возвращаемые значения в следующих условиях:</span><span class="sxs-lookup"><span data-stu-id="7a404-162">Expect the following return values under the following conditions:</span></span>
  
|<span data-ttu-id="7a404-163">**Условие**</span><span class="sxs-lookup"><span data-stu-id="7a404-163">**Condition**</span></span>|<span data-ttu-id="7a404-164">**Возвращаемое значение**</span><span class="sxs-lookup"><span data-stu-id="7a404-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a404-165">**CopyFolder** успешно скопировал или переместил папку и все вложенные в нее папки (если это необходимо).</span><span class="sxs-lookup"><span data-stu-id="7a404-165">**CopyFolder** successfully copied or moved the folder and all its subfolders, if applicable.</span></span>  <br/> |<span data-ttu-id="7a404-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a404-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="7a404-167">**CopyFolder** не удалось успешно скопировать или переместить все папки.</span><span class="sxs-lookup"><span data-stu-id="7a404-167">**CopyFolder** was unable to successfully copy or move all of the folders.</span></span>  <br/> |<span data-ttu-id="7a404-168">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="7a404-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="7a404-169">**CopyFolder** не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="7a404-169">**CopyFolder** was unable to complete.</span></span>  <br/> |<span data-ttu-id="7a404-170">Любое значение ошибки</span><span class="sxs-lookup"><span data-stu-id="7a404-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="7a404-171">Если **CopyFolder** возвращает значение ошибки, не переходите к предположении, что работа не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="7a404-171">If **CopyFolder** returns an error value, do not proceed on the assumption that no work was done.</span></span> <span data-ttu-id="7a404-172">Одну или несколько папок можно скопировать или переместить до того, как **CopyFolder** произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="7a404-172">One or more folders could have been copied or moved before **CopyFolder** experienced the failure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a404-173">См. также</span><span class="sxs-lookup"><span data-stu-id="7a404-173">See also</span></span>



[<span data-ttu-id="7a404-174">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a404-174">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

