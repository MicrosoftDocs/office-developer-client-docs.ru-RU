---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587707"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="bbfd6-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfd6-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="bbfd6-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbfd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbfd6-105">Устанавливает или удаляет профиль клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bbfd6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbfd6-106">Parameters</span></span>

 <span data-ttu-id="bbfd6-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="bbfd6-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="bbfd6-108">[in] Указатель на имя профиля, который будет по умолчанию, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="bbfd6-109">Установка _lpszProfileName_ значение NULL указывает, что **SetDefaultProfile** следует удалить существующий профиль по умолчанию, вследствие чего клиенту без значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="bbfd6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bbfd6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="bbfd6-111">[in] Битовая маска флагов, определяющее тип string, на который указывает _lpszProfileName_.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="bbfd6-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="bbfd6-112">The following flag can be set:</span></span>
    
<span data-ttu-id="bbfd6-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bbfd6-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="bbfd6-114">Имя профиля — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="bbfd6-115">Если флаг MAPI_UNICODE не установлен, в формате ANSI — это имя профиля.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bbfd6-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bbfd6-116">Return value</span></span>

<span data-ttu-id="bbfd6-117">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bbfd6-117">S_OK</span></span> 
  
> <span data-ttu-id="bbfd6-118">Профиль по умолчанию было успешно установлено или удалено.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="bbfd6-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="bbfd6-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="bbfd6-120">Указанный профиль не существует.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbfd6-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="bbfd6-121">Remarks</span></span>

<span data-ttu-id="bbfd6-122">Метод **IProfAdmin::SetDefaultProfile** устанавливает определенный профиль в качестве профиля по умолчанию клиента или очищает текущего профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="bbfd6-123">Профиль по умолчанию является профиль, используемый автоматически при каждом клиент начинает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="bbfd6-124">**SetDefaultProfile** также устанавливает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) нового профиля по умолчанию имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="bbfd6-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbfd6-125">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bbfd6-125">Notes to callers</span></span>

<span data-ttu-id="bbfd6-126">Чтобы начать сеанс с профилем по умолчанию, передача флаг MAPI_USE_DEFAULT функции [MAPILogonEx](mapilogonex.md) .</span><span class="sxs-lookup"><span data-stu-id="bbfd6-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bbfd6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bbfd6-127">See also</span></span>



[<span data-ttu-id="bbfd6-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="bbfd6-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="bbfd6-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="bbfd6-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="bbfd6-130">Каноническое свойство PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfd6-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="bbfd6-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbfd6-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

