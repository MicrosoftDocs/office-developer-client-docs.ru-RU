---
title: IMAPIFolderCreateFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateFolder
api_type:
- COM
ms.assetid: 39d07fc8-09aa-4122-af32-b02f2c893d29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 606d780aa59e363c30ddc7a5b562db64d845ccb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436764"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="d0cc9-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d0cc9-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="d0cc9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0cc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0cc9-105">Создает новую ветвь.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-105">Creates a new subfolder.</span></span>
  
```cpp
HRESULT CreateFolder(
  ULONG ulFolderType,
  LPSTR lpszFolderName,
  LPSTR lpszFolderComment,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMAPIFOLDER FAR * lppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="d0cc9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0cc9-106">Parameters</span></span>

 <span data-ttu-id="d0cc9-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="d0cc9-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="d0cc9-108">[in] Тип создаемой папки.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-108">[in] The type of folder to create.</span></span> <span data-ttu-id="d0cc9-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d0cc9-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d0cc9-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="d0cc9-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="d0cc9-111">Должна быть создана общая папка.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="d0cc9-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="d0cc9-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="d0cc9-113">Необходимо создать папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="d0cc9-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="d0cc9-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="d0cc9-115">[in] Указатель на строку, содержаную имя новой папки.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="d0cc9-116">Это имя является основой для свойства PR_DISPLAY_NAME **новой** папки ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d0cc9-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="d0cc9-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="d0cc9-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="d0cc9-118">[in] Указатель на строку, которая содержит комментарий, связанный с новой папкой.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="d0cc9-119">Эта строка становится значением свойства PR_COMMENT **новой** папки ([PidTagComment).](pidtagcomment-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d0cc9-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="d0cc9-120">Если передается NULL, у папки нет начального комментария.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="d0cc9-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="d0cc9-121">_lpInterface_</span></span>
  
> <span data-ttu-id="d0cc9-122">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к новой папке.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="d0cc9-123">Передача NULL приводит к возвращению поставщиком магазина сообщений стандартного интерфейса папки [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="d0cc9-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="d0cc9-124">Клиенты должны передавать NULL.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-124">Clients must pass NULL.</span></span> <span data-ttu-id="d0cc9-125">Другие вызыватели могут установить для  _параметра lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="d0cc9-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0cc9-126">_ulFlags_</span></span>
  
> <span data-ttu-id="d0cc9-127">[in] Битоваяmas флагов, которая управляет процессом создания папки.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="d0cc9-128">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d0cc9-128">The following flags can be set:</span></span>
    
<span data-ttu-id="d0cc9-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d0cc9-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d0cc9-130">Позволяет **CreateFolder** успешно возвращаться, возможно, до того, как новая папка будет полностью доступна вызываемому клиенту.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="d0cc9-131">Если новая папка недоступна, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="d0cc9-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0cc9-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d0cc9-133">Имя папки имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="d0cc9-134">Если флаг MAPI_UNICODE не установлен, имя папки будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="d0cc9-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="d0cc9-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="d0cc9-136">Позволяет успешно использовать метод, даже если папка с именем в параметре  _lpszFolderName_ уже существует, открыв существующую папку с таким именем.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="d0cc9-137">Обратите внимание, что поставщики store сообщений, которые позволяют папок одного и того же имени иметь одно и то же имя, могут не открывать существующую папку, если существует несколько папок с предоставленным именем.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="d0cc9-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="d0cc9-138">_lppFolder_</span></span>
  
> <span data-ttu-id="d0cc9-139">[out] Указатель на указатель на созданную папку.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0cc9-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0cc9-140">Return value</span></span>

<span data-ttu-id="d0cc9-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0cc9-141">S_OK</span></span> 
  
> <span data-ttu-id="d0cc9-142">Новая папка успешно создана или открыта, если OPEN_IF_EXISTS установлен.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="d0cc9-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d0cc9-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d0cc9-144">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="d0cc9-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="d0cc9-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="d0cc9-146">Папка с именем, заданным в  _параметре lpszFolderName,_ уже существует.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="d0cc9-147">Имена папок должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d0cc9-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0cc9-148">Remarks</span></span>

<span data-ttu-id="d0cc9-149">Метод **IMAPIFolder::CreateFolder** создает вложенную папку в текущей папке и назначает идентификатор записи новой папке.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d0cc9-150">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d0cc9-150">Notes to callers</span></span>

<span data-ttu-id="d0cc9-151">При **возвращении CreateFolder** следует помнить, что идентификатор записи для новой папки может быть не доступен.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="d0cc9-152">Некоторые поставщики store сообщений не делают идентификаторы записей доступными до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой папки для его постоянного сохранения.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="d0cc9-153">Это особенно актуально, если вы установили MAPI_DEFERRED_ERRORS флага.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="d0cc9-154">Следует помнить, что некоторые поставщики параметров хранения сообщений всегда указывают параметр _lppFolder_ на стандартный интерфейс папки независимо от значения параметра _lpInterface._</span><span class="sxs-lookup"><span data-stu-id="d0cc9-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="d0cc9-155">Так как возвращаемая указатель интерфейса может не иметь нужного типа, вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) новой папки, чтобы получить свойство **PR_OBJECT_TYPE** ([PidTagObjectType).](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d0cc9-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="d0cc9-156">При необходимости перед другими вызовами приведите указатель к более подходящему типу.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="d0cc9-157">Большинству поставщиков store сообщений требуется, чтобы имя новой папки было уникальным по отношению к именам ее папок одного и того же того же.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="d0cc9-158">Иметь возможность обрабатывать значение MAPI_E_COLLISION ошибки, которое возвращается, если это правило не следует.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="d0cc9-159">Чтобы определить идентификатор записи только что созданной папки, вызовите метод **IMAPIProp::GetProps** новой папки, чтобы получить ее свойство **PR_ENTRYID** ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d0cc9-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d0cc9-160">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d0cc9-160">MFCMAPI reference</span></span>

<span data-ttu-id="d0cc9-161">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d0cc9-162">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d0cc9-162">**File**</span></span>|<span data-ttu-id="d0cc9-163">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d0cc9-163">**Function**</span></span>|<span data-ttu-id="d0cc9-164">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d0cc9-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d0cc9-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d0cc9-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="d0cc9-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="d0cc9-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="d0cc9-167">MFCMAPI использует метод **CMsgStoreDlg::OnCreateSubFolder** для создания новых папок в MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="d0cc9-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0cc9-168">См. также</span><span class="sxs-lookup"><span data-stu-id="d0cc9-168">See also</span></span>



[<span data-ttu-id="d0cc9-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="d0cc9-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="d0cc9-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d0cc9-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="d0cc9-171">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d0cc9-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

