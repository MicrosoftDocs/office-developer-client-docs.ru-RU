---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419522"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="5e912-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="5e912-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="5e912-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e912-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e912-105">Назначает новое имя для профиля.</span><span class="sxs-lookup"><span data-stu-id="5e912-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5e912-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e912-106">Parameters</span></span>

 <span data-ttu-id="5e912-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="5e912-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="5e912-108">[in] Указатель на текущее имя профиля, который необходимо переименовать.</span><span class="sxs-lookup"><span data-stu-id="5e912-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="5e912-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="5e912-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="5e912-110">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="5e912-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="5e912-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="5e912-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="5e912-112">[in] Указатель на новое имя профиля, которое необходимо переименовать.</span><span class="sxs-lookup"><span data-stu-id="5e912-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="5e912-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5e912-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5e912-114">[in] Handle to the parent window of any dialog boxes or windows that this method displays.</span><span class="sxs-lookup"><span data-stu-id="5e912-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="5e912-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e912-115">_ulFlags_</span></span>
  
> <span data-ttu-id="5e912-116">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="5e912-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e912-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e912-117">Return value</span></span>

<span data-ttu-id="5e912-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e912-118">S_OK</span></span> 
  
> <span data-ttu-id="5e912-119">Профиль успешно переименован.</span><span class="sxs-lookup"><span data-stu-id="5e912-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="5e912-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="5e912-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="5e912-121">Пароль профиля неправильный.</span><span class="sxs-lookup"><span data-stu-id="5e912-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="5e912-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5e912-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5e912-123">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5e912-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5e912-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e912-124">Remarks</span></span>

<span data-ttu-id="5e912-125">Метод **IProfAdmin::RenameProfile** назначает новое имя профилю, если он имеет его.</span><span class="sxs-lookup"><span data-stu-id="5e912-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="5e912-126">Если профиль для переименования используется клиентом при его использовании, **RenameProfile** пометит профиль и возвращает S_OK вместо того, чтобы пытаться переименовать его, пока используется профиль. </span><span class="sxs-lookup"><span data-stu-id="5e912-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="5e912-127">Когда профиль больше не используется, **RenameProfile** назначает ему новое имя.</span><span class="sxs-lookup"><span data-stu-id="5e912-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="5e912-128">Старые и новые имена профиля могут иметь длину до 64 символов и могут включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="5e912-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="5e912-129">Все буквы и цифры, включая знаки акцента и символ подчеркиваения.</span><span class="sxs-lookup"><span data-stu-id="5e912-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="5e912-130">Внедренные пробелы, но не пробелы в первой или вехе.</span><span class="sxs-lookup"><span data-stu-id="5e912-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="5e912-131">_LpszPassword_ всегда должен иметь значение NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="5e912-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e912-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5e912-132">See also</span></span>



[<span data-ttu-id="5e912-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e912-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

