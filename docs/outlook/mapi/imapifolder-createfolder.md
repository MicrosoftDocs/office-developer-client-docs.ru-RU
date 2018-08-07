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
ms.openlocfilehash: 36fd729b1ca3e5d877d03358d581b83fc6d4782c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808861"
---
# <a name="imapifoldercreatefolder"></a><span data-ttu-id="0f3da-103">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="0f3da-103">IMAPIFolder::CreateFolder</span></span>

  
  
<span data-ttu-id="0f3da-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f3da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f3da-105">Создает папку.</span><span class="sxs-lookup"><span data-stu-id="0f3da-105">Creates a new subfolder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="0f3da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f3da-106">Parameters</span></span>

 <span data-ttu-id="0f3da-107">_ulFolderType_</span><span class="sxs-lookup"><span data-stu-id="0f3da-107">_ulFolderType_</span></span>
  
> <span data-ttu-id="0f3da-108">[in] Тип папки для создания.</span><span class="sxs-lookup"><span data-stu-id="0f3da-108">[in] The type of folder to create.</span></span> <span data-ttu-id="0f3da-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="0f3da-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0f3da-110">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="0f3da-110">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="0f3da-111">Должен быть создан общей папки.</span><span class="sxs-lookup"><span data-stu-id="0f3da-111">A generic folder should be created.</span></span>
    
<span data-ttu-id="0f3da-112">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="0f3da-112">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="0f3da-113">Должен быть создан в папку результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="0f3da-113">A search-results folder should be created.</span></span>
    
 <span data-ttu-id="0f3da-114">_lpszFolderName_</span><span class="sxs-lookup"><span data-stu-id="0f3da-114">_lpszFolderName_</span></span>
  
> <span data-ttu-id="0f3da-115">[in] Указатель на строку, содержащую имя новой папки.</span><span class="sxs-lookup"><span data-stu-id="0f3da-115">[in] A pointer to a string that contains the name for the new folder.</span></span> <span data-ttu-id="0f3da-116">Это имя является основой для свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) новую папку.</span><span class="sxs-lookup"><span data-stu-id="0f3da-116">This name is the basis for the new folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="0f3da-117">_lpszFolderComment_</span><span class="sxs-lookup"><span data-stu-id="0f3da-117">_lpszFolderComment_</span></span>
  
> <span data-ttu-id="0f3da-118">[in] Указатель на строку, которая содержит комментарий, связанный с новой папки.</span><span class="sxs-lookup"><span data-stu-id="0f3da-118">[in] A pointer to a string that contains a comment associated with the new folder.</span></span> <span data-ttu-id="0f3da-119">Эта строка становится значением свойства **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) новую папку.</span><span class="sxs-lookup"><span data-stu-id="0f3da-119">This string becomes the value of the new folder's **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) property.</span></span> <span data-ttu-id="0f3da-120">Если передается значение NULL, папка содержит начальной комментарий.</span><span class="sxs-lookup"><span data-stu-id="0f3da-120">If NULL is passed, the folder has no initial comment.</span></span>
    
 <span data-ttu-id="0f3da-121">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0f3da-121">_lpInterface_</span></span>
  
> <span data-ttu-id="0f3da-122">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к новой папки.</span><span class="sxs-lookup"><span data-stu-id="0f3da-122">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new folder.</span></span> <span data-ttu-id="0f3da-123">Значение NULL вызывает поставщика хранилища сообщений для возврата интерфейсе стандартные папки [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0f3da-123">Passing NULL causes the message store provider to return the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0f3da-124">Клиенты необходимо передать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="0f3da-124">Clients must pass NULL.</span></span> <span data-ttu-id="0f3da-125">Другие абонентов можно включить параметр _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer или IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="0f3da-125">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="0f3da-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0f3da-126">_ulFlags_</span></span>
  
> <span data-ttu-id="0f3da-127">[in] Битовая маска флаги, который определяет, как создать папку.</span><span class="sxs-lookup"><span data-stu-id="0f3da-127">[in] A bitmask of flags that controls how the folder is created.</span></span> <span data-ttu-id="0f3da-128">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="0f3da-128">The following flags can be set:</span></span>
    
<span data-ttu-id="0f3da-129">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0f3da-129">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0f3da-130">Разрешает **CreateFolder** для возврата успешно, возможно перед новой папки доступными для клиента.</span><span class="sxs-lookup"><span data-stu-id="0f3da-130">Allows **CreateFolder** to return successfully, possibly before the new folder is fully available to the calling client.</span></span> <span data-ttu-id="0f3da-131">Если новую папку не поддерживается, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="0f3da-131">If the new folder is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0f3da-132">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0f3da-132">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0f3da-133">— Это имя папки в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="0f3da-133">The name of the folder is in Unicode format.</span></span> <span data-ttu-id="0f3da-134">Если флаг MAPI_UNICODE не установлен, — это имя папки в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0f3da-134">If the MAPI_UNICODE flag is not set, the folder name is in ANSI format.</span></span>
    
<span data-ttu-id="0f3da-135">OPEN_IF_EXISTS</span><span class="sxs-lookup"><span data-stu-id="0f3da-135">OPEN_IF_EXISTS</span></span> 
  
> <span data-ttu-id="0f3da-136">Позволяет методу успешной даже в том случае, если папку с именем в параметре _lpszFolderName_ уже существует, откройте существующую папку с таким именем.</span><span class="sxs-lookup"><span data-stu-id="0f3da-136">Allows the method to succeed even if the folder named in the  _lpszFolderName_ parameter already exists by opening the existing folder that has that name.</span></span> <span data-ttu-id="0f3da-137">Обратите внимание на то, что поставщиков хранилища сообщений, которые позволяют одноуровневого папок, с одинаковыми именами не может открыть существующую папку, если существует несколько экземпляров с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="0f3da-137">Note that message store providers that allow sibling folders to have the same name might not open an existing folder if more than one exists with the supplied name.</span></span> 
    
 <span data-ttu-id="0f3da-138">_lppFolder_</span><span class="sxs-lookup"><span data-stu-id="0f3da-138">_lppFolder_</span></span>
  
> <span data-ttu-id="0f3da-139">[out] Указатель на указатель на только что созданная папка.</span><span class="sxs-lookup"><span data-stu-id="0f3da-139">[out] A pointer to a pointer to the newly created folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0f3da-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="0f3da-141">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0f3da-141">S_OK</span></span> 
  
> <span data-ttu-id="0f3da-142">Новую папку были успешно создана или открыта, если флаг OPEN_IF_EXISTS установлен.</span><span class="sxs-lookup"><span data-stu-id="0f3da-142">The new folder has been successfully created or opened, if the OPEN_IF_EXISTS flag is set.</span></span>
    
<span data-ttu-id="0f3da-143">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0f3da-143">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0f3da-144">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0f3da-144">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0f3da-145">MAPI_E_COLLISION</span><span class="sxs-lookup"><span data-stu-id="0f3da-145">MAPI_E_COLLISION</span></span> 
  
> <span data-ttu-id="0f3da-146">Папка, которая имеет имя, присвоенное с помощью параметра _lpszFolderName_ уже существует.</span><span class="sxs-lookup"><span data-stu-id="0f3da-146">A folder that has the name given in the  _lpszFolderName_ parameter already exists.</span></span> <span data-ttu-id="0f3da-147">Имена папок должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="0f3da-147">Folder names must be unique.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0f3da-148">Замечания</span><span class="sxs-lookup"><span data-stu-id="0f3da-148">Remarks</span></span>

<span data-ttu-id="0f3da-149">Метод **IMAPIFolder::CreateFolder** создает вложенную папку в текущей папке и назначает идентификатор записи в новую папку.</span><span class="sxs-lookup"><span data-stu-id="0f3da-149">The **IMAPIFolder::CreateFolder** method creates a subfolder in the current folder and assigns an entry identifier to the new folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0f3da-150">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0f3da-150">Notes to callers</span></span>

<span data-ttu-id="0f3da-151">При возврате **CreateFolder** , обратите внимание, что идентификатор записи на новую папку может быть недоступна.</span><span class="sxs-lookup"><span data-stu-id="0f3da-151">When **CreateFolder** returns, be aware that the entry identifier for the new folder might not be available.</span></span> <span data-ttu-id="0f3da-152">Некоторые поставщики хранения сообщения не предоставляют идентификаторы записей до после вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новую папку для сохранения ее без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="0f3da-152">Some message store providers do not make entry identifiers available until after you have called the new folder's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to permanently save it.</span></span> <span data-ttu-id="0f3da-153">Это особенно важно, если выбрать флаг MAPI_DEFERRED_ERRORS.</span><span class="sxs-lookup"><span data-stu-id="0f3da-153">This is especially true if you have set the MAPI_DEFERRED_ERRORS flag.</span></span> 
  
<span data-ttu-id="0f3da-154">Обратите внимание, что некоторые поставщики хранилища сообщений всегда указывать параметр _lppFolder_ стандартный интерфейс папки, независимо от того, значение, переданное для параметра _lpInterface_ .</span><span class="sxs-lookup"><span data-stu-id="0f3da-154">Be aware that some message store providers always point the  _lppFolder_ parameter to the folder's standard interface, regardless of the value that you pass in for the  _lpInterface_ parameter.</span></span> <span data-ttu-id="0f3da-155">Указатель интерфейса, который возвращается может быть типа, предполагается, что, вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) новую папку для получения свойства **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f3da-155">Because the interface pointer that is returned might not be of the type that you expect, call the new folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) property.</span></span> <span data-ttu-id="0f3da-156">При необходимости привести указатель на более подходящий тип, прежде чем принять других вызовов.</span><span class="sxs-lookup"><span data-stu-id="0f3da-156">If necessary, cast the pointer to a more appropriate type before you make other calls.</span></span>
  
<span data-ttu-id="0f3da-157">Большинство поставщиков хранилища сообщений требуется имя новой папки должно быть уникальным по отношению к имена его папки.</span><span class="sxs-lookup"><span data-stu-id="0f3da-157">Most message store providers require the name of the new folder to be unique with respect to the names of its sibling folders.</span></span> <span data-ttu-id="0f3da-158">Иметь возможность обрабатывать MAPI_E_COLLISION об ошибке, которое возвращается, если это правило не следует.</span><span class="sxs-lookup"><span data-stu-id="0f3da-158">Be able to handle the MAPI_E_COLLISION error value, which is returned if this rule is not followed.</span></span> 
  
<span data-ttu-id="0f3da-159">Чтобы определить идентификатор записи только что созданная папка, вызовите метод **IMAPIProp::GetProps** новую папку для получения его свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f3da-159">To determine the entry identifier of the newly created folder, call the new folder's **IMAPIProp::GetProps** method to retrieve its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0f3da-160">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="0f3da-160">MFCMAPI reference</span></span>

<span data-ttu-id="0f3da-161">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="0f3da-161">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0f3da-162">**����**</span><span class="sxs-lookup"><span data-stu-id="0f3da-162">**File**</span></span>|<span data-ttu-id="0f3da-163">**�������**</span><span class="sxs-lookup"><span data-stu-id="0f3da-163">**Function**</span></span>|<span data-ttu-id="0f3da-164">**�����������**</span><span class="sxs-lookup"><span data-stu-id="0f3da-164">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0f3da-165">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="0f3da-165">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="0f3da-166">CMsgStoreDlg::OnCreateSubFolder</span><span class="sxs-lookup"><span data-stu-id="0f3da-166">CMsgStoreDlg::OnCreateSubFolder</span></span>  <br/> |<span data-ttu-id="0f3da-167">Mfcmapi (en) использует метод **CMsgStoreDlg::OnCreateSubFolder** для создания новой папки в mfcmapi (en).</span><span class="sxs-lookup"><span data-stu-id="0f3da-167">MFCMAPI uses the **CMsgStoreDlg::OnCreateSubFolder** method to create new folders in MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f3da-168">См. также</span><span class="sxs-lookup"><span data-stu-id="0f3da-168">See also</span></span>



[<span data-ttu-id="0f3da-169">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="0f3da-169">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="0f3da-170">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0f3da-170">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="0f3da-171">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0f3da-171">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

