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
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="175ba-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="175ba-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="175ba-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="175ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="175ba-105">Копирует службу сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="175ba-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="175ba-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="175ba-106">Parameters</span></span>

 <span data-ttu-id="175ba-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="175ba-107">_lpUID_</span></span>
  
> <span data-ttu-id="175ba-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="175ba-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="175ba-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="175ba-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="175ba-110">[in] Этот параметр является неподготовленным.</span><span class="sxs-lookup"><span data-stu-id="175ba-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="175ba-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="175ba-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="175ba-112">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, используемый для доступа к разделу профиля службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="175ba-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="175ba-113">Передача NULL приводит к стандартному интерфейсу раздела профиля [IProfSect,](iprofsectimapiprop.md)который используется.</span><span class="sxs-lookup"><span data-stu-id="175ba-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="175ba-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="175ba-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="175ba-115">[in] Указатель на IID, который представляет интерфейс, используемый для доступа к объекту, на который указывает параметр _lpObjectDst._</span><span class="sxs-lookup"><span data-stu-id="175ba-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="175ba-116">Передача NULL приводит к использования интерфейса [сеанса IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="175ba-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="175ba-117">Для  _параметра lpInterfaceDst_ также можно установить IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="175ba-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="175ba-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="175ba-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="175ba-119">[in] Указатель на указатель на объект администрирования сеанса или службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="175ba-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="175ba-120">Тип объекта должен соответствовать идентификатору интерфейса, переданного _в lpInterfaceDst._</span><span class="sxs-lookup"><span data-stu-id="175ba-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="175ba-121">Допустимые указатели объектов — LPMAPISESSION и LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="175ba-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="175ba-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="175ba-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="175ba-123">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span><span class="sxs-lookup"><span data-stu-id="175ba-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="175ba-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="175ba-124">_ulFlags_</span></span>
  
> <span data-ttu-id="175ba-125">[in] Битоваяmas флагов, которая управляет копированием службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="175ba-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="175ba-126">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="175ba-126">The following flags can be set:</span></span>
    
<span data-ttu-id="175ba-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="175ba-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="175ba-128">Запрашивает, чтобы служба сообщений всегда отображала таблицу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="175ba-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="175ba-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="175ba-129">Return value</span></span>

<span data-ttu-id="175ba-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="175ba-130">S_OK</span></span> 
  
> <span data-ttu-id="175ba-131">Служба сообщений успешно скопирована.</span><span class="sxs-lookup"><span data-stu-id="175ba-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="175ba-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="175ba-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="175ba-133">Служба сообщений уже находится в профиле и не разрешает несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="175ba-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="175ba-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="175ba-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="175ba-135">**MAPIUID, на** который указывает _lpUID,_ не относится к существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="175ba-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="175ba-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="175ba-136">Remarks</span></span>

<span data-ttu-id="175ba-137">Метод **IMsgServiceAdmin::CopyMsgService** копирует службу сообщений в профиль, активный профиль или другой профиль.</span><span class="sxs-lookup"><span data-stu-id="175ba-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="175ba-138">Профиль, содержащий службу сообщений для копирования и назначения, не должен быть тем же профилем, но может быть.</span><span class="sxs-lookup"><span data-stu-id="175ba-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="175ba-139">Функция точки входа службы сообщений не вызвана для операции копирования.</span><span class="sxs-lookup"><span data-stu-id="175ba-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="175ba-140">Скопированная служба сообщений имеет те же параметры конфигурации, что и исходный.</span><span class="sxs-lookup"><span data-stu-id="175ba-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="175ba-141">Чтобы изменить эти параметры, клиент должен вызвать метод [IMsgServiceAdmin::ConfigureMsgService.](imsgserviceadmin-configuremsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="175ba-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="175ba-142">См. также</span><span class="sxs-lookup"><span data-stu-id="175ba-142">See also</span></span>



[<span data-ttu-id="175ba-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="175ba-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="175ba-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="175ba-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="175ba-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="175ba-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

