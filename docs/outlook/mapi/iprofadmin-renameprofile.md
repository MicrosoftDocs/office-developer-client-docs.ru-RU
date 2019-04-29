---
title: Ипрофадминренамепрофиле
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
# <a name="iprofadminrenameprofile"></a><span data-ttu-id="ded3a-103">IProfAdmin::RenameProfile</span><span class="sxs-lookup"><span data-stu-id="ded3a-103">IProfAdmin::RenameProfile</span></span>

  
  
<span data-ttu-id="ded3a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ded3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ded3a-105">Назначает новое имя профилю.</span><span class="sxs-lookup"><span data-stu-id="ded3a-105">Assigns a new name to a profile.</span></span>
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ded3a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ded3a-106">Parameters</span></span>

 <span data-ttu-id="ded3a-107">_Лпсзолдпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="ded3a-107">_lpszOldProfileName_</span></span>
  
> <span data-ttu-id="ded3a-108">возврата Указатель на текущее имя профиля, которое требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="ded3a-108">[in] A pointer to the current name of the profile to rename.</span></span>
    
 <span data-ttu-id="ded3a-109">_Лпсзолдпассворд_</span><span class="sxs-lookup"><span data-stu-id="ded3a-109">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="ded3a-110">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ded3a-110">[in] Always NULL.</span></span>
    
 <span data-ttu-id="ded3a-111">_Лпсзневпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="ded3a-111">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="ded3a-112">возврата Указатель на новое имя профиля, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="ded3a-112">[in] A pointer to the new name of the profile to rename.</span></span>
    
 <span data-ttu-id="ded3a-113">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="ded3a-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="ded3a-114">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="ded3a-114">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> 
    
 <span data-ttu-id="ded3a-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ded3a-115">_ulFlags_</span></span>
  
> <span data-ttu-id="ded3a-116">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ded3a-116">[in] Always NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ded3a-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ded3a-117">Return value</span></span>

<span data-ttu-id="ded3a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ded3a-118">S_OK</span></span> 
  
> <span data-ttu-id="ded3a-119">Профиль успешно переименован.</span><span class="sxs-lookup"><span data-stu-id="ded3a-119">The profile was successfully renamed.</span></span>
    
<span data-ttu-id="ded3a-120">МАПИ_Е_ЛОГОН_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="ded3a-120">MAPI_E_LOGON_FAILED</span></span> 
  
> <span data-ttu-id="ded3a-121">Недопустимый пароль профиля.</span><span class="sxs-lookup"><span data-stu-id="ded3a-121">The profile password is incorrect.</span></span>
    
<span data-ttu-id="ded3a-122">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="ded3a-122">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ded3a-123">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ded3a-123">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ded3a-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="ded3a-124">Remarks</span></span>

<span data-ttu-id="ded3a-125">Метод **ипрофадмин:: ренамепрофиле** назначает новое имя профилю, если он имеет такой профиль.</span><span class="sxs-lookup"><span data-stu-id="ded3a-125">The **IProfAdmin::RenameProfile** method assigns a new name to a profile, if it has one.</span></span> <span data-ttu-id="ded3a-126">Если профиль для переименования используется клиентом при вызове **ренамепрофиле** , **ренамепрофиле** помечает профиль и возвращает значение S_OK вместо попытки выполнить операцию переименования во время использования профиля.</span><span class="sxs-lookup"><span data-stu-id="ded3a-126">If the profile to rename is in use by a client when **RenameProfile** is called, **RenameProfile** marks the profile and returns S_OK instead of attempting the rename operation while the profile is in use.</span></span> <span data-ttu-id="ded3a-127">Если профиль больше не используется, **ренамепрофиле** назначает ему новое имя.</span><span class="sxs-lookup"><span data-stu-id="ded3a-127">When the profile is no longer being used, **RenameProfile** assigns it the new name.</span></span> 
  
<span data-ttu-id="ded3a-128">Длина старого и нового имен профиля может доставлять до 64 символов и содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="ded3a-128">The old and new names of the profile can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="ded3a-129">Все буквенно-цифровые символы, включая диакритические знаки и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="ded3a-129">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="ded3a-130">Внутренние пробелы, но не ведущие и замыкающие пробелы.</span><span class="sxs-lookup"><span data-stu-id="ded3a-130">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="ded3a-131">_Лпсзпассворд_ всегда должно иметь значение null или быть указателем на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="ded3a-131">The  _lpszPassword_ should always be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ded3a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="ded3a-132">See also</span></span>



[<span data-ttu-id="ded3a-133">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ded3a-133">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

