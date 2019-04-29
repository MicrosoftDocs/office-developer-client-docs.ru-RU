---
title: Ипрофадминкопипрофиле
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
# <a name="iprofadmincopyprofile"></a><span data-ttu-id="50e00-103">IProfAdmin::CopyProfile</span><span class="sxs-lookup"><span data-stu-id="50e00-103">IProfAdmin::CopyProfile</span></span>

  
  
<span data-ttu-id="50e00-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50e00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50e00-105">Копирует профиль.</span><span class="sxs-lookup"><span data-stu-id="50e00-105">Copies a profile.</span></span>
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="50e00-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50e00-106">Parameters</span></span>

 <span data-ttu-id="50e00-107">_Лпсзолдпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="50e00-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="50e00-108">возврата Указатель на имя профиля, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="50e00-108">[in] A pointer to the name of the profile to copy.</span></span>
    
 <span data-ttu-id="50e00-109">_Лпсзолдпассворд_</span><span class="sxs-lookup"><span data-stu-id="50e00-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="50e00-110">возврата Указатель на пароль, который необходимо скопировать.</span><span class="sxs-lookup"><span data-stu-id="50e00-110">[in] A pointer to the password of the profile to copy.</span></span>
    
 <span data-ttu-id="50e00-111">_Лпсзневпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="50e00-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="50e00-112">возврата Указатель на новое имя скопированного профиля.</span><span class="sxs-lookup"><span data-stu-id="50e00-112">[in] A pointer to the new name of the copied profile.</span></span>
    
 <span data-ttu-id="50e00-113">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="50e00-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="50e00-114">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="50e00-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="50e00-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50e00-115">_ulFlags_</span></span>
  
> <span data-ttu-id="50e00-116">возврата Битовая маска флагов, определяющих способ копирования профиля.</span><span class="sxs-lookup"><span data-stu-id="50e00-116">[in] A bitmask of flags that controls how the profile is copied.</span></span> <span data-ttu-id="50e00-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="50e00-117">The following flags can be set:</span></span>
    
<span data-ttu-id="50e00-118">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="50e00-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="50e00-119">Отображает диалоговое окно, в котором пользователю предлагается ввести правильный пароль для копирования профиля.</span><span class="sxs-lookup"><span data-stu-id="50e00-119">Displays a dialog box that prompts the user for the correct password of the profile to copy.</span></span> <span data-ttu-id="50e00-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="50e00-120">If this flag is not set, no dialog box is displayed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50e00-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50e00-121">Return value</span></span>

<span data-ttu-id="50e00-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="50e00-122">S_OK</span></span> 
  
> <span data-ttu-id="50e00-123">Профиль успешно скопирован.</span><span class="sxs-lookup"><span data-stu-id="50e00-123">The profile was successfully copied.</span></span>
    
<span data-ttu-id="50e00-124">МАПИ_Е_АКЦЕСС_ДЕНИЕД</span><span class="sxs-lookup"><span data-stu-id="50e00-124">MAPI_E_ACCESS_DENIED</span></span> 
  
> <span data-ttu-id="50e00-125">Имя нового профиля совпадает с именем существующего профиля.</span><span class="sxs-lookup"><span data-stu-id="50e00-125">The new profile name is the same as that of an existing profile.</span></span>
    
<span data-ttu-id="50e00-126">МАПИ_Е_ЛОГОН_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="50e00-126">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="50e00-127">Неправильный пароль для копирования профиля, и пользователю не удалось отобразить диалоговое окно, чтобы запросить правильный пароль, так как МАПИ_ДИАЛОГ не задан в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="50e00-127">The password for the profile to copy is incorrect, and a dialog box could not be displayed to the user to request the correct password because MAPI_DIALOG was not set in the  _ulFlags_ parameter.</span></span> 
    
<span data-ttu-id="50e00-128">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="50e00-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="50e00-129">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="50e00-129">The specified profile does not exist.</span></span>
    
<span data-ttu-id="50e00-130">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="50e00-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="50e00-131">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="50e00-131">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="50e00-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="50e00-132">Remarks</span></span>

<span data-ttu-id="50e00-133">Метод **ипрофадмин:: копипрофиле** создает копию профиля, на которую указывает _лпсзолдпрофиленаме_, предоставляя ему имя, на которое указывает _лпсзневпрофиленаме_.</span><span class="sxs-lookup"><span data-stu-id="50e00-133">The **IProfAdmin::CopyProfile** method makes a copy of the profile pointed to by  _lpszOldProfileName_, giving it the name pointed to by  _lpszNewProfileName_.</span></span> <span data-ttu-id="50e00-134">Копирование профиля оставляет копию с тем же паролем, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="50e00-134">Copying a profile leaves the copy with the same password as the original.</span></span>
  
<span data-ttu-id="50e00-135">Имя исходного профиля, его пароль и копия могут иметь длину до 64 символов и могут включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="50e00-135">The name of the original profile, its password, and the copy can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="50e00-136">Все буквенно-цифровые символы, включая диакритические знаки и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="50e00-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="50e00-137">Внутренние пробелы, но не ведущие и замыкающие пробелы.</span><span class="sxs-lookup"><span data-stu-id="50e00-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="50e00-138">Пароли профилей не поддерживаются во всех операционных системах.</span><span class="sxs-lookup"><span data-stu-id="50e00-138">Profile passwords are not supported on all operating systems.</span></span> <span data-ttu-id="50e00-139">В операционных системах, не поддерживающих пароли профилей, _лпсзолдпассворд_ может иметь значение null или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="50e00-139">On operating systems that do not support profile passwords,  _lpszOldPassword_ can be NULL or a pointer to a zero-length string.</span></span> 
  
<span data-ttu-id="50e00-140">Если для параметра _лпсзолдпассворд_ ЗАДАНО значение null, то для профиля требуется пароль, а флаг мапи_диалог установлен; диалоговое окно, предлагающее пользователю ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="50e00-140">If  _lpszOldPassword_ is set to NULL, the profile to be copied requires a password, and the MAPI_DIALOG flag is set; a dialog box that prompts the user to provide the password is displayed.</span></span> <span data-ttu-id="50e00-141">Если требуется пароль, но для параметра _лпсзолдпассворд_ ЗАДАНО значение null, а флаг мапи_диалог не установлен, **копипрофиле** возвращает мапи_е_логон_фаилед.</span><span class="sxs-lookup"><span data-stu-id="50e00-141">If a password is required, but  _lpszOldPassword_ is set to NULL and the MAPI_DIALOG flag is not set, **CopyProfile** returns MAPI_E_LOGON_FAILED.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50e00-142">См. также</span><span class="sxs-lookup"><span data-stu-id="50e00-142">See also</span></span>



[<span data-ttu-id="50e00-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50e00-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

