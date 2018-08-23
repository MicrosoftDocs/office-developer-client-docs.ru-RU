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
ms.openlocfilehash: 9e22111ec920d89e0874baf71946681c204cacd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571208"
---
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="a3dbe-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="a3dbe-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="a3dbe-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3dbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3dbe-105">Копирует профиль.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a3dbe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3dbe-106">Parameters</span></span>

 <span data-ttu-id="a3dbe-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="a3dbe-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="a3dbe-108">[in] Указатель на имя профиля для копирования.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="a3dbe-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="a3dbe-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="a3dbe-110">[in] Указатель на пароль профиля для копирования.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="a3dbe-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="a3dbe-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="a3dbe-112">[in] Указатель на новое имя скопированного профиля.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="a3dbe-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a3dbe-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="a3dbe-114">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="a3dbe-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3dbe-115">_ulFlags_</span></span>
  
> <span data-ttu-id="a3dbe-116">[in] Битовая маска флаги, который определяет, как скопировать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="a3dbe-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="a3dbe-117">The following flags can be set:</span></span>
    
<span data-ttu-id="a3dbe-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="a3dbe-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="a3dbe-119">Отображает диалоговое окно, которое запрашивает у правильный пароль профиля пользователя для копирования.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="a3dbe-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3dbe-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a3dbe-121">Return value</span></span>

<span data-ttu-id="a3dbe-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a3dbe-122">S_OK</span></span> 
  
> <span data-ttu-id="a3dbe-123">Профиль успешно скопирован.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="a3dbe-124">MAPI_E_ACCESS_DENIED</span><span class="sxs-lookup"><span data-stu-id="a3dbe-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="a3dbe-125">Имя нового профиля — это то же самое, что и существующий профиль.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="a3dbe-126">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="a3dbe-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="a3dbe-127">Неправильный пароль для профиля для копирования и диалоговое окно "" не удается отобразить для пользователя, чтобы запросить правильный пароль, так как MAPI_DIALOG не установлен в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="a3dbe-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="a3dbe-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a3dbe-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a3dbe-129">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="a3dbe-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a3dbe-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a3dbe-131">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a3dbe-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3dbe-132">Remarks</span></span>

<span data-ttu-id="a3dbe-133">Предоставляет метод **IProfAdmin::CopyProfile** , копию профиля, который указывает _lpszOldProfileName_, указав имя указывает _lpszNewProfileName_.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="a3dbe-134">Копирование профиля оставляет эту копию с тот же пароль, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="a3dbe-135">Имя исходного профиля, его пароль и эту копию может быть длиной до 64 символов и может содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="a3dbe-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="a3dbe-136">Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="a3dbe-137">Пробелы, но не начальных и конечных пробелов.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="a3dbe-138">Профиль пароли не поддерживаются для всех операционных систем.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="a3dbe-139">В операционных системах, которые не поддерживают пароли профилей _lpszOldPassword_ может быть NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="a3dbe-140">Если _lpszOldPassword_ имеет значение NULL, профиля для копирования требуется пароль, а флаг MAPI_DIALOG — значение; отображается диалоговое окно, в котором пользователь для ввода пароля.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="a3dbe-141">Если пароль является обязательным, но _lpszOldPassword_ имеет значение NULL и MAPI_DIALOG флаг не установлен, **CopyProfile** возвращает MAPI_E_LOGON_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a3dbe-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3dbe-142">См. также</span><span class="sxs-lookup"><span data-stu-id="a3dbe-142">See also</span></span>



[<span data-ttu-id="a3dbe-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3dbe-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

