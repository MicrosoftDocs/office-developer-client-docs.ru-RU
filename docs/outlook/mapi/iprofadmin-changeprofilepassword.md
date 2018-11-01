---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 41066d4418760a676fbc02241bfc12d83275da9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573000"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="706f2-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="706f2-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="706f2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="706f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="706f2-105">Рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="706f2-105">Deprecated.</span></span> <span data-ttu-id="706f2-106">Изменение пароля для профиля.</span><span class="sxs-lookup"><span data-stu-id="706f2-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="706f2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="706f2-107">Parameters</span></span>

 <span data-ttu-id="706f2-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="706f2-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="706f2-109">[in] Указатель на имя профиля, связанные с использованием пароля, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="706f2-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="706f2-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="706f2-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="706f2-111">[in] Указатель на текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="706f2-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="706f2-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="706f2-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="706f2-113">[in] Указатель на новый пароль.</span><span class="sxs-lookup"><span data-stu-id="706f2-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="706f2-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="706f2-114">_ulFlags_</span></span>
  
> <span data-ttu-id="706f2-115">[in] Битовая маска флаги, определяющее тип строк, переданное.</span><span class="sxs-lookup"><span data-stu-id="706f2-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="706f2-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="706f2-116">The following flag can be set:</span></span>
    
<span data-ttu-id="706f2-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="706f2-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="706f2-118">Имя профиля и пароли, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="706f2-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="706f2-119">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="706f2-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="706f2-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="706f2-120">Return value</span></span>

<span data-ttu-id="706f2-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="706f2-121">S_OK</span></span> 
  
> <span data-ttu-id="706f2-122">Если этот метод вызывается, она возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="706f2-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="706f2-123">Тем не менее не действие не выполняется.</span><span class="sxs-lookup"><span data-stu-id="706f2-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="706f2-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="706f2-124">Remarks</span></span>

<span data-ttu-id="706f2-125">Не используйте этот метод.</span><span class="sxs-lookup"><span data-stu-id="706f2-125">Do not use this method.</span></span> <span data-ttu-id="706f2-126">MAPI не поддерживает пароли для профилей.</span><span class="sxs-lookup"><span data-stu-id="706f2-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="706f2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="706f2-127">See also</span></span>



[<span data-ttu-id="706f2-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="706f2-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

