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
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420243"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="38934-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="38934-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="38934-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38934-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38934-105">Устарело.</span><span class="sxs-lookup"><span data-stu-id="38934-105">Deprecated.</span></span> <span data-ttu-id="38934-106">Изменяет пароль для профиля.</span><span class="sxs-lookup"><span data-stu-id="38934-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="38934-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="38934-107">Parameters</span></span>

 <span data-ttu-id="38934-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="38934-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="38934-109">[in] Указатель на имя профиля, связанного с паролем, который необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="38934-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="38934-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="38934-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="38934-111">[in] Указатель на текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="38934-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="38934-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="38934-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="38934-113">[in] Указатель на новый пароль.</span><span class="sxs-lookup"><span data-stu-id="38934-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="38934-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38934-114">_ulFlags_</span></span>
  
> <span data-ttu-id="38934-115">[in] Битоваяmas флагов, которая управляет типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="38934-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="38934-116">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="38934-116">The following flag can be set:</span></span>
    
<span data-ttu-id="38934-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="38934-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="38934-118">Имя профиля и пароли имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="38934-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="38934-119">Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="38934-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38934-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38934-120">Return value</span></span>

<span data-ttu-id="38934-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="38934-121">S_OK</span></span> 
  
> <span data-ttu-id="38934-122">Если этот метод вызван, он возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="38934-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="38934-123">Однако никаких действий не будет.</span><span class="sxs-lookup"><span data-stu-id="38934-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38934-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="38934-124">Remarks</span></span>

<span data-ttu-id="38934-125">Не используйте этот метод.</span><span class="sxs-lookup"><span data-stu-id="38934-125">Do not use this method.</span></span> <span data-ttu-id="38934-126">MAPI не поддерживает пароли для профилей.</span><span class="sxs-lookup"><span data-stu-id="38934-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="38934-127">См. также</span><span class="sxs-lookup"><span data-stu-id="38934-127">See also</span></span>



[<span data-ttu-id="38934-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38934-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

