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
ms.openlocfilehash: 4453465c04d7a5a3de79f2ae34d13095863487cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569507"
---
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="efe10-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="efe10-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="efe10-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efe10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efe10-105">Назначает новое имя профиля.</span><span class="sxs-lookup"><span data-stu-id="efe10-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="efe10-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efe10-106">Parameters</span></span>

 <span data-ttu-id="efe10-107">_lpszOldProfileName_</span><span class="sxs-lookup"><span data-stu-id="efe10-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="efe10-108">[in] Указатель на имя текущего профиля, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="efe10-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="efe10-109">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="efe10-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="efe10-110">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="efe10-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="efe10-111">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="efe10-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="efe10-112">[in] Указатель на новое имя профиля, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="efe10-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="efe10-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="efe10-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="efe10-114">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="efe10-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="efe10-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="efe10-115">_ulFlags_</span></span>
  
> <span data-ttu-id="efe10-116">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="efe10-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="efe10-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efe10-117">Return value</span></span>

<span data-ttu-id="efe10-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="efe10-118">S_OK</span></span> 
  
> <span data-ttu-id="efe10-119">Профиль успешно переименован.</span><span class="sxs-lookup"><span data-stu-id="efe10-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="efe10-120">MAPI_E_LOGON_FAILED</span><span class="sxs-lookup"><span data-stu-id="efe10-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="efe10-121">Неправильный пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="efe10-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="efe10-122">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="efe10-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="efe10-123">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="efe10-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="efe10-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="efe10-124">Remarks</span></span>

<span data-ttu-id="efe10-125">Метод **IProfAdmin::RenameProfile** назначается новое имя профиля, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="efe10-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="efe10-126">Если профиль, чтобы переименовать используется клиентом при вызове **RenameProfile** , **RenameProfile** помечает профиля и возвращает значение S_OK вместо попытки подключения операция переименования профиля во время работы.</span><span class="sxs-lookup"><span data-stu-id="efe10-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="efe10-127">Если профиль больше не используется, **RenameProfile** назначает ее новое имя.</span><span class="sxs-lookup"><span data-stu-id="efe10-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="efe10-128">Имена старый и новый профиль может иметь длину до 64 символов и может содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="efe10-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="efe10-129">Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="efe10-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="efe10-130">Пробелы, но не начальных и конечных пробелов.</span><span class="sxs-lookup"><span data-stu-id="efe10-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="efe10-131">_LpszPassword_ всегда должно быть NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="efe10-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efe10-132">См. также</span><span class="sxs-lookup"><span data-stu-id="efe10-132">See also</span></span>



[<span data-ttu-id="efe10-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="efe10-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

