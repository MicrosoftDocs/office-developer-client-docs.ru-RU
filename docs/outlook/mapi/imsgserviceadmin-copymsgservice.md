---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432123"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="0da57-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="0da57-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="0da57-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0da57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0da57-105">Копирует службу сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="0da57-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0da57-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="0da57-106">Parameters</span></span>

 <span data-ttu-id="0da57-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="0da57-107">_lpUID_</span></span>
  
> <span data-ttu-id="0da57-108">[in] Указатель на [структуру MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="0da57-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="0da57-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="0da57-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="0da57-110">[in] Этот параметр был обесценив.</span><span class="sxs-lookup"><span data-stu-id="0da57-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="0da57-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="0da57-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="0da57-112">[in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к разделу профилей службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="0da57-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="0da57-113">Передача NULL приводит к стандартному интерфейсу раздела профилей [IProfSect,](iprofsectimapiprop.md)который используется.</span><span class="sxs-lookup"><span data-stu-id="0da57-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="0da57-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="0da57-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="0da57-115">[in] Указатель на IID, который представляет интерфейс, используемый для доступа к объекту, на который указывает _параметр lpObjectDst._</span><span class="sxs-lookup"><span data-stu-id="0da57-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="0da57-116">Передача NULL приводит к интерфейсу [сеанса, используется IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="0da57-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="0da57-117">Параметр  _lpInterfaceDst_ также может быть задан для IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="0da57-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="0da57-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="0da57-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="0da57-119">[in] Указатель на указатель на объект администрирования сеанса или службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0da57-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="0da57-120">Тип объекта должен соответствовать идентификатору интерфейса, переданным _в lpInterfaceDst._</span><span class="sxs-lookup"><span data-stu-id="0da57-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="0da57-121">Допустимые указатели объектов LPMAPISESSION и LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="0da57-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="0da57-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0da57-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="0da57-123">[in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом.</span><span class="sxs-lookup"><span data-stu-id="0da57-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="0da57-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0da57-124">_ulFlags_</span></span>
  
> <span data-ttu-id="0da57-125">[in] Битмаски флагов, которые контролируют копирование службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0da57-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="0da57-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="0da57-126">The following flags can be set:</span></span>
    
<span data-ttu-id="0da57-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="0da57-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="0da57-128">Запрашивает, чтобы служба сообщений всегда отображала лист свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0da57-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0da57-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0da57-129">Return value</span></span>

<span data-ttu-id="0da57-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="0da57-130">S_OK</span></span> 
  
> <span data-ttu-id="0da57-131">Служба сообщений успешно скопирована.</span><span class="sxs-lookup"><span data-stu-id="0da57-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="0da57-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0da57-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0da57-133">Служба сообщений уже находится в профиле и не позволяет использовать несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="0da57-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="0da57-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="0da57-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="0da57-135">**MapIUID,** на который указывает _lpUID,_ не относится к существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="0da57-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0da57-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="0da57-136">Remarks</span></span>

<span data-ttu-id="0da57-137">Метод **IMsgServiceAdmin::CopyMsgService** копирует службу сообщений в профиль, активный профиль или другой профиль.</span><span class="sxs-lookup"><span data-stu-id="0da57-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="0da57-138">Профиль, содержащий скопированную службу сообщений и пункт назначения, не должен быть таким же профилем, но может быть.</span><span class="sxs-lookup"><span data-stu-id="0da57-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="0da57-139">Функция точки входа службы сообщений не называется для операции копирования.</span><span class="sxs-lookup"><span data-stu-id="0da57-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="0da57-140">Скопированная служба сообщений имеет те же параметры конфигурации, что и оригинал.</span><span class="sxs-lookup"><span data-stu-id="0da57-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="0da57-141">Чтобы изменить эти параметры, клиент должен вызвать [метод IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="0da57-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0da57-142">См. также</span><span class="sxs-lookup"><span data-stu-id="0da57-142">See also</span></span>



[<span data-ttu-id="0da57-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="0da57-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="0da57-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0da57-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0da57-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0da57-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

