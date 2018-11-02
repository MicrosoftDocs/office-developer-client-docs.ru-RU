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
ms.openlocfilehash: e09a1de5f85edd7e352a090c573fed9ca16f017f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565552"
---
# <a name="imapistatuschangepassword"></a><span data-ttu-id="0b5d0-103">IMAPIStatus::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="0b5d0-103">IMAPIStatus::ChangePassword</span></span>

  
  
<span data-ttu-id="0b5d0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b5d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b5d0-105">Изменение пароля поставщика услуг без отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-105">Modifies a service provider's password without displaying a user interface.</span></span> <span data-ttu-id="0b5d0-106">Этот метод при необходимости поддерживается в состоянии объекты, которые реализуют поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-106">This method is optionally supported in status objects that service providers implement.</span></span>
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0b5d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b5d0-107">Parameters</span></span>

 <span data-ttu-id="0b5d0-108">_lpOldPass_</span><span class="sxs-lookup"><span data-stu-id="0b5d0-108">_lpOldPass_</span></span>
  
> <span data-ttu-id="0b5d0-109">[in] Указатель на старый пароль.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-109">[in] A pointer to the old password.</span></span>
    
 <span data-ttu-id="0b5d0-110">_lpNewPass_</span><span class="sxs-lookup"><span data-stu-id="0b5d0-110">_lpNewPass_</span></span>
  
> <span data-ttu-id="0b5d0-111">[in] Указатель на новый пароль.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-111">[in] A pointer to the new password.</span></span>
    
 <span data-ttu-id="0b5d0-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0b5d0-112">_ulFlags_</span></span>
  
> <span data-ttu-id="0b5d0-113">[in] Битовая маска флаги, который определяет формат паролей.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-113">[in] A bitmask of flags that controls the format of the passwords.</span></span> <span data-ttu-id="0b5d0-114">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0b5d0-114">The following flag can be set:</span></span>
    
<span data-ttu-id="0b5d0-115">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b5d0-115">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0b5d0-116">Пароли, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-116">The passwords are in Unicode format.</span></span> <span data-ttu-id="0b5d0-117">Если флаг MAPI_UNICODE не установлен, пароли, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-117">If the MAPI_UNICODE flag is not set, the passwords are in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0b5d0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b5d0-118">Return value</span></span>

<span data-ttu-id="0b5d0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b5d0-119">S_OK</span></span> 
  
> <span data-ttu-id="0b5d0-120">Изменение пароля прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-120">The password modification was successful.</span></span>
    
<span data-ttu-id="0b5d0-121">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0b5d0-121">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0b5d0-122">Старый пароль, на который указывает _lpOldPass_ является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-122">The old password pointed to by  _lpOldPass_ is invalid.</span></span> 
    
<span data-ttu-id="0b5d0-123">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0b5d0-123">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0b5d0-124">Состояние объект не поддерживает эту операцию, как указано в отсутствие флага STATUS_CHANGE_PASSWORD в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-124">The status object does not support this operation, as indicated by the absence of the STATUS_CHANGE_PASSWORD flag in the status object's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b5d0-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b5d0-125">Remarks</span></span>

<span data-ttu-id="0b5d0-126">Не все объекты состояния поддерживают метод **IMAPIStatus::ChangePassword** .</span><span class="sxs-lookup"><span data-stu-id="0b5d0-126">Not all status objects support the **IMAPIStatus::ChangePassword** method.</span></span> <span data-ttu-id="0b5d0-127">Поддерживается только поставщиков услуг, клиентам необходимо ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-127">It is supported only by service providers that require clients to enter a password.</span></span> <span data-ttu-id="0b5d0-128">Ни один из состояния объекты, внедряемые MAPI не поддерживает операцию смены пароля.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-128">None of the status objects that MAPI implements support the password change operation.</span></span> 
  
 <span data-ttu-id="0b5d0-129">**Изменение пароля** программным способом, изменяет пароль без взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-129">**ChangePassword** modifies a password programmatically, without user interaction.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0b5d0-130">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="0b5d0-130">Notes to implementers</span></span>

<span data-ttu-id="0b5d0-131">Поставщики удаленного транспорта реализовать **Изменение пароля** , указанный здесь.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-131">Remote transport providers implement **ChangePassword** as specified here.</span></span> <span data-ttu-id="0b5d0-132">Существует не особенности.</span><span class="sxs-lookup"><span data-stu-id="0b5d0-132">There are no special considerations.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b5d0-133">См. также</span><span class="sxs-lookup"><span data-stu-id="0b5d0-133">See also</span></span>



[<span data-ttu-id="0b5d0-134">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="0b5d0-134">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="0b5d0-135">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0b5d0-135">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

