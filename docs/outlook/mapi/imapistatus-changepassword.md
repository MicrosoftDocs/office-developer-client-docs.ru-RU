---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410359"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="d76fc-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="d76fc-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="d76fc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d76fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d76fc-105">Изменяет пароль поставщика услуг без отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d76fc-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="d76fc-106">При желании этот метод поддерживается в объектах состояния, реализуемых поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="d76fc-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d76fc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d76fc-107">Parameters</span></span>

 <span data-ttu-id="d76fc-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="d76fc-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="d76fc-109">[in] Указатель на старый пароль.</span><span class="sxs-lookup"><span data-stu-id="d76fc-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="d76fc-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="d76fc-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="d76fc-111">[in] Указатель на новый пароль.</span><span class="sxs-lookup"><span data-stu-id="d76fc-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="d76fc-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d76fc-112">_ulFlags_</span></span>
  
> <span data-ttu-id="d76fc-113">[in] Битоваяmas флагов, которая управляет форматом паролей.</span><span class="sxs-lookup"><span data-stu-id="d76fc-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="d76fc-114">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d76fc-114">The following flag can be set:</span></span>
    
<span data-ttu-id="d76fc-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d76fc-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d76fc-116">Пароли имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d76fc-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="d76fc-117">Если флаг MAPI_UNICODE не установлен, пароли имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="d76fc-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d76fc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d76fc-118">Return value</span></span>

<span data-ttu-id="d76fc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d76fc-119">S_OK</span></span> 
  
> <span data-ttu-id="d76fc-120">Изменение пароля было успешным.</span><span class="sxs-lookup"><span data-stu-id="d76fc-120">The password modification was successful.</span></span>
    
<span data-ttu-id="d76fc-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d76fc-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d76fc-122">Старый пароль, на который указывает  _lpOldPass,_ недействителен.</span><span class="sxs-lookup"><span data-stu-id="d76fc-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="d76fc-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d76fc-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d76fc-124">Объект состояния не поддерживает эту операцию, на что указывает отсутствие флага STATUS_CHANGE_PASSWORD в свойстве **PR_RESOURCE_METHODS** объекта status [(PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d76fc-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d76fc-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="d76fc-125">Remarks</span></span>

<span data-ttu-id="d76fc-126">Не все объекты состояния поддерживают метод **IMAPIStatus::ChangePassword.**</span><span class="sxs-lookup"><span data-stu-id="d76fc-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="d76fc-127">Она поддерживается только поставщиками услуг, которые требуют ввода пароля клиентами.</span><span class="sxs-lookup"><span data-stu-id="d76fc-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="d76fc-128">Ни один из объектов состояния, реализуемого MAPI, не поддерживает операцию смены пароля.</span><span class="sxs-lookup"><span data-stu-id="d76fc-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="d76fc-129">**ChangePassword** изменяет пароль программным путем без участия пользователя.</span><span class="sxs-lookup"><span data-stu-id="d76fc-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d76fc-130">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d76fc-130">Notes to implementers</span></span>

<span data-ttu-id="d76fc-131">Поставщики удаленных транспортных услуг **реализуют ChangePassword,** как указано здесь.</span><span class="sxs-lookup"><span data-stu-id="d76fc-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="d76fc-132">Нет особых соображений.</span><span class="sxs-lookup"><span data-stu-id="d76fc-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d76fc-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d76fc-133">See also</span></span>



[<span data-ttu-id="d76fc-134">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="d76fc-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="d76fc-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d76fc-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

