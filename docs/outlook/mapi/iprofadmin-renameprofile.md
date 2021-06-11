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
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="80015-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="80015-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="80015-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80015-105">Назначает новое имя в профиль.</span><span class="sxs-lookup"><span data-stu-id="80015-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="80015-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="80015-106">Parameters</span></span>

 <span data-ttu-id="80015-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="80015-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="80015-108">[in] Указатель на текущее имя профиля для переименования.</span><span class="sxs-lookup"><span data-stu-id="80015-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="80015-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="80015-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="80015-110">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="80015-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="80015-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="80015-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="80015-112">[in] Указатель на новое имя профиля для переименования.</span><span class="sxs-lookup"><span data-stu-id="80015-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="80015-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="80015-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="80015-114">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="80015-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="80015-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80015-115">_ulFlags_</span></span>
  
> <span data-ttu-id="80015-116">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="80015-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80015-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80015-117">Return value</span></span>

<span data-ttu-id="80015-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="80015-118">S_OK</span></span> 
  
> <span data-ttu-id="80015-119">Профиль был успешно переименован.</span><span class="sxs-lookup"><span data-stu-id="80015-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="80015-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="80015-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="80015-121">Пароль профиля неправильный.</span><span class="sxs-lookup"><span data-stu-id="80015-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="80015-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="80015-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="80015-123">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="80015-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="80015-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="80015-124">Remarks</span></span>

<span data-ttu-id="80015-125">Метод **IProfAdmin::RenameProfile** назначает новое имя для профиля, если оно имеет его.</span><span class="sxs-lookup"><span data-stu-id="80015-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="80015-126">Если профиль для переименования используется клиентом, когда называется **RenameProfile,** **renameProfile** пометит профиль и возвращает его S_OK вместо попытки операции переименования во время использования профиля.</span><span class="sxs-lookup"><span data-stu-id="80015-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="80015-127">Когда профиль больше не используется, **RenameProfile** назначает ему новое имя.</span><span class="sxs-lookup"><span data-stu-id="80015-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="80015-128">Старые и новые имена профиля могут иметь длину до 64 символов и включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="80015-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="80015-129">Все буквы, включая символы акцента и символы подчеркнуть.</span><span class="sxs-lookup"><span data-stu-id="80015-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="80015-130">Встроенные пробелы, но не ведущие и не ведущие.</span><span class="sxs-lookup"><span data-stu-id="80015-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="80015-131">_LpszPassword_ всегда должен быть NULL или указателем для строки нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="80015-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="80015-132">См. также</span><span class="sxs-lookup"><span data-stu-id="80015-132">See also</span></span>



[<span data-ttu-id="80015-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80015-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

