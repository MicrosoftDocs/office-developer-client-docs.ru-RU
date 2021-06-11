---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437240"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="11c3b-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="11c3b-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="11c3b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11c3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11c3b-105">Копирует профиль.</span><span class="sxs-lookup"><span data-stu-id="11c3b-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="11c3b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="11c3b-106">Parameters</span></span>

 <span data-ttu-id="11c3b-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="11c3b-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="11c3b-108">[in] Указатель на имя профиля для копирования.</span><span class="sxs-lookup"><span data-stu-id="11c3b-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="11c3b-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="11c3b-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="11c3b-110">[in] Указатель на пароль профиля для копирования.</span><span class="sxs-lookup"><span data-stu-id="11c3b-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="11c3b-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="11c3b-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="11c3b-112">[in] Указатель на новое имя скопированного профиля.</span><span class="sxs-lookup"><span data-stu-id="11c3b-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="11c3b-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="11c3b-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="11c3b-114">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="11c3b-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="11c3b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="11c3b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="11c3b-116">[in] Битмашка флагов, которые контролируют копирование профиля.</span><span class="sxs-lookup"><span data-stu-id="11c3b-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="11c3b-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="11c3b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="11c3b-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="11c3b-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="11c3b-119">Отображает диалоговое окно, которое подсказывет пользователю правильный пароль профиля для копирования.</span><span class="sxs-lookup"><span data-stu-id="11c3b-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="11c3b-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="11c3b-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11c3b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11c3b-121">Return value</span></span>

<span data-ttu-id="11c3b-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="11c3b-122">S_OK</span></span> 
  
> <span data-ttu-id="11c3b-123">Профиль был успешно скопирован.</span><span class="sxs-lookup"><span data-stu-id="11c3b-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="11c3b-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="11c3b-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="11c3b-125">Новое имя профиля является таким же, как и существующего профиля.</span><span class="sxs-lookup"><span data-stu-id="11c3b-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="11c3b-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="11c3b-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="11c3b-127">Пароль для копирования профиля неверен, и диалоговое окно не может отображаться пользователю для запроса правильного пароля, так как MAPI_DIALOG не был задан в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="11c3b-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="11c3b-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="11c3b-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="11c3b-129">Указанного профиля не существует.</span><span class="sxs-lookup"><span data-stu-id="11c3b-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="11c3b-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="11c3b-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="11c3b-131">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="11c3b-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="11c3b-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="11c3b-132">Remarks</span></span>

<span data-ttu-id="11c3b-133">Метод **IProfAdmin::CopyProfile** создает копию профиля, на который указывает _lpszOldProfileName,_ придавая ему имя, на которое указывает _lpszNewProfileName._</span><span class="sxs-lookup"><span data-stu-id="11c3b-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="11c3b-134">Копирование профиля оставляет копию с тем же паролем, что и оригинал.</span><span class="sxs-lookup"><span data-stu-id="11c3b-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="11c3b-135">Имя исходного профиля, его пароль и копия могут иметь длину до 64 символов и включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="11c3b-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="11c3b-136">Все буквы, включая символы акцента и символы подчеркнуть.</span><span class="sxs-lookup"><span data-stu-id="11c3b-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="11c3b-137">Встроенные пробелы, но не ведущие и не ведущие.</span><span class="sxs-lookup"><span data-stu-id="11c3b-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="11c3b-138">Пароли профилей поддерживаются не во всех операционных системах.</span><span class="sxs-lookup"><span data-stu-id="11c3b-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="11c3b-139">В операционных системах, которые не поддерживают пароли профилей,  _lpszOldPassword_ может быть NULL или указателем на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="11c3b-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="11c3b-140">Если  _lpszOldPassword_ задает NULL, для скопивного профиля требуется пароль, а MAPI_DIALOG задает флаг; отображается диалоговое окно, в которое пользователь должен предоставить пароль.</span><span class="sxs-lookup"><span data-stu-id="11c3b-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="11c3b-141">Если требуется пароль, но  _для lpszOldPassword_ задавалось NULL и флаг MAPI_DIALOG не установлен, **CopyProfile** возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="11c3b-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11c3b-142">См. также</span><span class="sxs-lookup"><span data-stu-id="11c3b-142">See also</span></span>



[<span data-ttu-id="11c3b-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11c3b-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

