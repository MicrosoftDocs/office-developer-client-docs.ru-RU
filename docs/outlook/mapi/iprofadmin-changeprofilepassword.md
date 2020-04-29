---
title: ипрофадминчанжепрофилепассворд
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
# <a name="iprofadminchangeprofilepassword"></a><span data-ttu-id="46143-103">IProfAdmin::ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="46143-103">IProfAdmin::ChangeProfilePassword</span></span>

  
  
<span data-ttu-id="46143-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46143-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46143-105">Устаревшие.</span><span class="sxs-lookup"><span data-stu-id="46143-105">Deprecated.</span></span> <span data-ttu-id="46143-106">Изменяет пароль для профиля.</span><span class="sxs-lookup"><span data-stu-id="46143-106">Changes the password for a profile.</span></span>
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="46143-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="46143-107">Parameters</span></span>

 <span data-ttu-id="46143-108">_лпсзпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="46143-108">_lpszProfileName_</span></span>
  
> <span data-ttu-id="46143-109">возврата Указатель на имя профиля, связанного с изменяемым паролем.</span><span class="sxs-lookup"><span data-stu-id="46143-109">[in] A pointer to the name of the profile associated with the password to be changed.</span></span>
    
 <span data-ttu-id="46143-110">_лпсзолдпассворд_</span><span class="sxs-lookup"><span data-stu-id="46143-110">_lpszOldPassword_</span></span>
  
> <span data-ttu-id="46143-111">возврата Указатель на текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="46143-111">[in] A pointer to the current password.</span></span>
    
 <span data-ttu-id="46143-112">_лпсзневпассворд_</span><span class="sxs-lookup"><span data-stu-id="46143-112">_lpszNewPassword_</span></span>
  
> <span data-ttu-id="46143-113">возврата Указатель на новый пароль.</span><span class="sxs-lookup"><span data-stu-id="46143-113">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="46143-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="46143-114">_ulFlags_</span></span>
  
> <span data-ttu-id="46143-115">возврата Битовая маска флагов, которые управляют типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="46143-115">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="46143-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="46143-116">The following flag can be set:</span></span>
    
<span data-ttu-id="46143-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46143-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="46143-118">Имя профиля и пароль имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="46143-118">The profile name and passwords are in Unicode format.</span></span> <span data-ttu-id="46143-119">Если флаг MAPI_UNICODE не установлен, эти строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="46143-119">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46143-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46143-120">Return value</span></span>

<span data-ttu-id="46143-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="46143-121">S_OK</span></span> 
  
> <span data-ttu-id="46143-122">При вызове этого метода он возвратит S_OK.</span><span class="sxs-lookup"><span data-stu-id="46143-122">If this method is called, it will return S_OK.</span></span> <span data-ttu-id="46143-123">Однако никакие действия не выполняются.</span><span class="sxs-lookup"><span data-stu-id="46143-123">However, no action will be taken.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46143-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="46143-124">Remarks</span></span>

<span data-ttu-id="46143-125">Не используйте этот метод.</span><span class="sxs-lookup"><span data-stu-id="46143-125">Do not use this method.</span></span> <span data-ttu-id="46143-126">MAPI не поддерживает пароли для профилей.</span><span class="sxs-lookup"><span data-stu-id="46143-126">MAPI does not support passwords for profiles.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46143-127">См. также</span><span class="sxs-lookup"><span data-stu-id="46143-127">See also</span></span>



[<span data-ttu-id="46143-128">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46143-128">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

