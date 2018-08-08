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
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809515"
---
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="b1451-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="b1451-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="b1451-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1451-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1451-105">Рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="b1451-105">Deprecated.</span></span> <span data-ttu-id="b1451-106">Изменение пароля для профиля.</span><span class="sxs-lookup"><span data-stu-id="b1451-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b1451-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1451-107">Parameters</span></span>

 <span data-ttu-id="b1451-108">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="b1451-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="b1451-109">[in] Указатель на имя профиля, связанные с использованием пароля, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b1451-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="b1451-110">_lpszOldPassword_</span><span class="sxs-lookup"><span data-stu-id="b1451-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="b1451-111">[in] Указатель на текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="b1451-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="b1451-112">_lpszNewPassword_</span><span class="sxs-lookup"><span data-stu-id="b1451-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="b1451-113">[in] Указатель на новый пароль.</span><span class="sxs-lookup"><span data-stu-id="b1451-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="b1451-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1451-114">_ulFlags_</span></span>
  
> <span data-ttu-id="b1451-115">[in] Битовая маска флаги, определяющее тип строк, переданное.</span><span class="sxs-lookup"><span data-stu-id="b1451-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="b1451-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b1451-116">The following flag can be set:</span></span>
    
<span data-ttu-id="b1451-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1451-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1451-118">Имя профиля и пароли, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b1451-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="b1451-119">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1451-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1451-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b1451-120">Return value</span></span>

<span data-ttu-id="b1451-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b1451-121">S_OK</span></span> 
  
> <span data-ttu-id="b1451-122">Если этот метод вызывается, она возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="b1451-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="b1451-123">Тем не менее не действие не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1451-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1451-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="b1451-124">Remarks</span></span>

<span data-ttu-id="b1451-125">Не используйте этот метод.</span><span class="sxs-lookup"><span data-stu-id="b1451-125">Do not use this method.</span></span> <span data-ttu-id="b1451-126">MAPI не поддерживает пароли для профилей.</span><span class="sxs-lookup"><span data-stu-id="b1451-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1451-127">См. также</span><span class="sxs-lookup"><span data-stu-id="b1451-127">See also</span></span>



[<span data-ttu-id="b1451-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1451-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

