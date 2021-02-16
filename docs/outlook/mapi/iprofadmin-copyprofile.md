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
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="e80b9-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="e80b9-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="e80b9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e80b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e80b9-105">Копирует профиль.</span><span class="sxs-lookup"><span data-stu-id="e80b9-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e80b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e80b9-106">Parameters</span></span>

 <span data-ttu-id="e80b9-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="e80b9-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="e80b9-108">[in] Указатель на имя профиля, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="e80b9-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="e80b9-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="e80b9-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="e80b9-110">[in] Указатель на пароль профиля, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="e80b9-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="e80b9-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="e80b9-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="e80b9-112">[in] Указатель на новое имя скопированного профиля.</span><span class="sxs-lookup"><span data-stu-id="e80b9-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="e80b9-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e80b9-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="e80b9-114">[in] Handle to the parent window of any dialog boxes or windows that this method displays.</span><span class="sxs-lookup"><span data-stu-id="e80b9-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="e80b9-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e80b9-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e80b9-116">[in] Битоваяmas флагов, которая управляет копированием профиля.</span><span class="sxs-lookup"><span data-stu-id="e80b9-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="e80b9-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e80b9-117">The following flags can be set:</span></span>
    
<span data-ttu-id="e80b9-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e80b9-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="e80b9-119">Отображает диалоговое окно, в которое пользователю будет предложено скопировать правильный пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="e80b9-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="e80b9-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="e80b9-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e80b9-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e80b9-121">Return value</span></span>

<span data-ttu-id="e80b9-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e80b9-122">S_OK</span></span> 
  
> <span data-ttu-id="e80b9-123">Профиль успешно скопирован.</span><span class="sxs-lookup"><span data-stu-id="e80b9-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="e80b9-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="e80b9-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="e80b9-125">Имя нового профиля такое же, как у существующего профиля.</span><span class="sxs-lookup"><span data-stu-id="e80b9-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="e80b9-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="e80b9-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="e80b9-127">Неправильный пароль для скопируйте профиль, и пользователю не удалось отобразить диалоговое окно для запроса правильного пароля, так как MAPI_DIALOG не задан в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e80b9-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="e80b9-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e80b9-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="e80b9-129">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="e80b9-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="e80b9-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="e80b9-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="e80b9-131">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e80b9-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e80b9-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="e80b9-132">Remarks</span></span>

<span data-ttu-id="e80b9-133">Метод **IProfAdmin::CopyProfile** создает копию профиля, на который указывает _lpszOldProfileName,_ придавая ему имя, на которое указывает _lpszNewProfileName._</span><span class="sxs-lookup"><span data-stu-id="e80b9-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="e80b9-134">Копирование профиля оставляет копию с тем же паролем, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="e80b9-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="e80b9-135">Имя исходного профиля, его пароль и копия могут иметь длину до 64 символов и могут включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="e80b9-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="e80b9-136">Все буквы и цифры, включая знаки акцента и символ подчеркиваения.</span><span class="sxs-lookup"><span data-stu-id="e80b9-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="e80b9-137">Внедренные пробелы, но не пробелы в первой или вехе.</span><span class="sxs-lookup"><span data-stu-id="e80b9-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="e80b9-138">Пароли профилей не поддерживаются во всех операционных системах.</span><span class="sxs-lookup"><span data-stu-id="e80b9-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="e80b9-139">В операционных системах, которые не поддерживают пароли профилей,  _lpszOldPassword_ может иметь значение NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="e80b9-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="e80b9-140">Если  _для lpszOldPassword_ установлено nULL, для копируется профиль требуется пароль, а также MAPI_DIALOG флаг; Отобразилось диалоговое окно с запросом вводить пароль.</span><span class="sxs-lookup"><span data-stu-id="e80b9-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="e80b9-141">Если пароль обязален, но для  _lpszOldPassword_ установлено MAPI_DIALOG NULL, **copyProfile** возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="e80b9-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e80b9-142">См. также</span><span class="sxs-lookup"><span data-stu-id="e80b9-142">See also</span></span>



[<span data-ttu-id="e80b9-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e80b9-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

