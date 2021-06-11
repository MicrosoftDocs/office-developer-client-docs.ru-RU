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
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="9e823-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="9e823-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="9e823-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e823-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e823-105">Создает новый подмосток.</span><span class="sxs-lookup"><span data-stu-id="9e823-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="9e823-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9e823-106">Parameters</span></span>

 <span data-ttu-id="9e823-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="9e823-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="9e823-108">[in] Тип папки для создания.</span><span class="sxs-lookup"><span data-stu-id="9e823-108">[in] The type of folder to create.</span></span> <span data-ttu-id="9e823-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9e823-109">The following flags can be set:</span></span>
    
<span data-ttu-id="9e823-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="9e823-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="9e823-111">Должна быть создана общая папка.</span><span class="sxs-lookup"><span data-stu-id="9e823-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="9e823-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="9e823-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="9e823-113">Необходимо создать папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="9e823-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="9e823-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="9e823-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="9e823-115">[in] Указатель на строку, содержаную имя новой папки.</span><span class="sxs-lookup"><span data-stu-id="9e823-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="9e823-116">Это имя является основой для свойства  PR_DISPLAY_NAME[(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9e823-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="9e823-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="9e823-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="9e823-118">[in] Указатель на строку, содержаную комментарий, связанный с новой папкой.</span><span class="sxs-lookup"><span data-stu-id="9e823-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="9e823-119">Эта строка становится значением свойства  PR_COMMENT[(PidTagComment).](pidtagcomment-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9e823-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="9e823-120">Если NULL передается, у папки нет начального комментария.</span><span class="sxs-lookup"><span data-stu-id="9e823-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="9e823-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="9e823-121">_lpInterface_</span></span>
  
> <span data-ttu-id="9e823-122">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к новой папке.</span><span class="sxs-lookup"><span data-stu-id="9e823-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="9e823-123">Передача NULL заставляет поставщика хранения сообщений возвращать стандартный интерфейс папки [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="9e823-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="9e823-124">Клиенты должны пройти NULL.</span><span class="sxs-lookup"><span data-stu-id="9e823-124">Clients must pass NULL.</span></span> <span data-ttu-id="9e823-125">Другие звонители могут установить параметр  _lpInterface_ для IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="9e823-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="9e823-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e823-126">_ulFlags_</span></span>
  
> <span data-ttu-id="9e823-127">[in] Битмаска флагов, контролируемая тем, как создается папка.</span><span class="sxs-lookup"><span data-stu-id="9e823-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="9e823-128">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9e823-128">The following flags can be set:</span></span>
    
<span data-ttu-id="9e823-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9e823-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9e823-130">Позволяет **CreateFolder** успешно возвращаться, возможно, до того, как новая папка будет полностью доступна для вызываемого клиента.</span><span class="sxs-lookup"><span data-stu-id="9e823-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="9e823-131">Если новая папка недоступна, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="9e823-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="9e823-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9e823-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9e823-133">Имя папки находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="9e823-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="9e823-134">Если флаг MAPI_UNICODE не установлен, имя папки находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9e823-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="9e823-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="9e823-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="9e823-136">Позволяет методу добиться успеха, даже если папка, названная в параметре  _lpszFolderName,_ уже существует, открыв существующую папку с таким именем.</span><span class="sxs-lookup"><span data-stu-id="9e823-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="9e823-137">Обратите внимание, что поставщики магазинов сообщений, которые позволяют папкам-однобрачам иметь одно имя, могут не открывать существующую папку, если с предоставленным именем существует несколько.</span><span class="sxs-lookup"><span data-stu-id="9e823-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="9e823-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="9e823-138">_lppFolder_</span></span>
  
> <span data-ttu-id="9e823-139">[вышел] Указатель на указатель на вновь созданную папку.</span><span class="sxs-lookup"><span data-stu-id="9e823-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e823-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e823-140">Return value</span></span>

<span data-ttu-id="9e823-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e823-141">S_OK</span></span> 
  
> <span data-ttu-id="9e823-142">Новая папка успешно создана или открыта, если OPEN_IF_EXISTS установлен флаг.</span><span class="sxs-lookup"><span data-stu-id="9e823-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="9e823-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9e823-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9e823-144">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="9e823-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9e823-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="9e823-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="9e823-146">Папка с именем, заданным в  _параметре lpszFolderName,_ уже существует.</span><span class="sxs-lookup"><span data-stu-id="9e823-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="9e823-147">Имена папок должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="9e823-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9e823-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e823-148">Remarks</span></span>

<span data-ttu-id="9e823-149">Метод **IMAPIFolder::CreateFolder** создает подмостки в текущей папке и назначает идентификатор входа в новую папку.</span><span class="sxs-lookup"><span data-stu-id="9e823-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9e823-150">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9e823-150">Notes to callers</span></span>

<span data-ttu-id="9e823-151">Когда **CreateFolder** возвращается, следует помнить, что идентификатор записи для новой папки может быть недоступным.</span><span class="sxs-lookup"><span data-stu-id="9e823-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="9e823-152">Некоторые поставщики магазинов сообщений не делают идентификаторы записей доступными до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой папки для его постоянного сохранения.</span><span class="sxs-lookup"><span data-stu-id="9e823-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="9e823-153">Это особенно актуально, если вы установили флаг MAPI_DEFERRED_ERRORS.</span><span class="sxs-lookup"><span data-stu-id="9e823-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="9e823-154">Следует помнить, что некоторые поставщики магазинов сообщений всегда указывают параметр _lppFolder_ на стандартный интерфейс папки, независимо от значения, которое вы передаете для _параметра lpInterface._</span><span class="sxs-lookup"><span data-stu-id="9e823-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="9e823-155">Поскольку возвращаемая указатель интерфейса может быть не того типа, который вы ожидаете, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) новой **папки,** чтобы получить свойство [PR_OBJECT_TYPE (PidTagObjectType).](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9e823-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="9e823-156">При необходимости переведите указатель в более подходящий тип перед другими вызовами.</span><span class="sxs-lookup"><span data-stu-id="9e823-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="9e823-157">Большинство поставщиков магазинов сообщений требуют, чтобы имя новой папки было уникальным по отношению к именам его папок-окантов.</span><span class="sxs-lookup"><span data-stu-id="9e823-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="9e823-158">Возможность обработки значения MAPI_E_COLLISION ошибки, которое возвращается, если это правило не следует.</span><span class="sxs-lookup"><span data-stu-id="9e823-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="9e823-159">Чтобы определить идентификатор записи вновь созданной папки, позвоните по методу **IMAPIProp::GetProps** новой папки, чтобы получить ее свойство [PR_ENTRYID (PidTagEntryId).](pidtagentryid-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="9e823-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e823-160">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9e823-160">MFCMAPI reference</span></span>

<span data-ttu-id="9e823-161">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9e823-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e823-162">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9e823-162">**File**</span></span>|<span data-ttu-id="9e823-163">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9e823-163">**Function**</span></span>|<span data-ttu-id="9e823-164">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9e823-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e823-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9e823-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="9e823-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="9e823-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="9e823-167">MFCMAPI использует **метод CMsgStoreDlg::OnCreateSubFolder** для создания новых папок в MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="9e823-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e823-168">См. также</span><span class="sxs-lookup"><span data-stu-id="9e823-168">See also</span></span>



[<span data-ttu-id="9e823-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="9e823-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="9e823-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="9e823-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="9e823-171">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9e823-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

