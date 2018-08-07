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
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809368"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="d72cf-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="d72cf-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="d72cf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d72cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d72cf-105">Копирует службы сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="d72cf-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="d72cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d72cf-106">Parameters</span></span>

 <span data-ttu-id="d72cf-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="d72cf-107">_lpUID_</span></span>
  
> <span data-ttu-id="d72cf-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="d72cf-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="d72cf-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="d72cf-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="d72cf-110">[in] Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="d72cf-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="d72cf-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="d72cf-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="d72cf-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="d72cf-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="d72cf-113">Стандартный профиль раздел интерфейса, [IProfSect](iprofsectimapiprop.md)используется результаты передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="d72cf-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="d72cf-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="d72cf-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="d72cf-115">[in] Указатель на ИД интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _lpObjectDst_ .</span><span class="sxs-lookup"><span data-stu-id="d72cf-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="d72cf-116">В интерфейсе сеанса [IMAPISession](imapisessioniunknown.md)используется результаты передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="d72cf-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="d72cf-117">Параметр _lpInterfaceDst_ также может иметь значение IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="d72cf-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="d72cf-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="d72cf-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="d72cf-119">[in] Указатель на указатель на объект администрирования службы сеанса или сообщения.</span><span class="sxs-lookup"><span data-stu-id="d72cf-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="d72cf-120">Тип объекта, должен соответствовать идентификатор интерфейса, переданные в _lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="d72cf-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="d72cf-121">Допустимый объект указатели — LPMAPISESSION и LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="d72cf-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="d72cf-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d72cf-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="d72cf-123">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="d72cf-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="d72cf-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d72cf-124">_ulFlags_</span></span>
  
> <span data-ttu-id="d72cf-125">[in] Битовая маска флаги, который определяет, как скопировать службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d72cf-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="d72cf-126">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="d72cf-126">The following flags can be set:</span></span>
    
<span data-ttu-id="d72cf-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="d72cf-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="d72cf-128">Запросы на том, что служба сообщений всегда отображаются на листе свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d72cf-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d72cf-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="d72cf-130">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d72cf-130">S_OK</span></span> 
  
> <span data-ttu-id="d72cf-131">Служба сообщений успешно скопирована.</span><span class="sxs-lookup"><span data-stu-id="d72cf-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="d72cf-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="d72cf-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="d72cf-133">Служба сообщений уже в профиле и не допускает несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d72cf-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="d72cf-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d72cf-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d72cf-135">**MAPIUID** , на который указывает _lpUID_ не относится к существующей службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d72cf-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d72cf-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="d72cf-136">Remarks</span></span>

<span data-ttu-id="d72cf-137">Метод **IMsgServiceAdmin::CopyMsgService** копирует службы сообщений в профиль текущей конфигурации или другого профиля.</span><span class="sxs-lookup"><span data-stu-id="d72cf-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="d72cf-138">Профиль, который содержит службы сообщений для копирования и назначение не должны быть одного профиля, но они могут быть.</span><span class="sxs-lookup"><span data-stu-id="d72cf-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="d72cf-139">Служба сообщений функции точки входа не вызывается для операции копирования.</span><span class="sxs-lookup"><span data-stu-id="d72cf-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="d72cf-140">Служба скопированной сообщение имеет те же параметры конфигурации, что его исходный.</span><span class="sxs-lookup"><span data-stu-id="d72cf-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="d72cf-141">Чтобы изменить эти параметры, клиент должен вызвать метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d72cf-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d72cf-142">См. также</span><span class="sxs-lookup"><span data-stu-id="d72cf-142">See also</span></span>



[<span data-ttu-id="d72cf-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="d72cf-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="d72cf-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d72cf-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d72cf-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d72cf-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

