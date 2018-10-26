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
ms.openlocfilehash: 791dfe094aa0ff1aab656b56fbdf7d59e880b92e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593734"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="347d5-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="347d5-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="347d5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="347d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="347d5-105">Копирует службы сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="347d5-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="347d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="347d5-106">Parameters</span></span>

 <span data-ttu-id="347d5-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="347d5-107">_lpUID_</span></span>
  
> <span data-ttu-id="347d5-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="347d5-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="347d5-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="347d5-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="347d5-110">[in] Этот параметр устарел.</span><span class="sxs-lookup"><span data-stu-id="347d5-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="347d5-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="347d5-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="347d5-112">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля службы сообщений для копирования.</span><span class="sxs-lookup"><span data-stu-id="347d5-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="347d5-113">Стандартный профиль раздел интерфейса, [IProfSect](iprofsectimapiprop.md)используется результаты передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="347d5-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="347d5-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="347d5-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="347d5-115">[in] Указатель на ИД интерфейса, который представляет интерфейс, который будет использоваться для доступа к объекту, на который указывает параметр _lpObjectDst_ .</span><span class="sxs-lookup"><span data-stu-id="347d5-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="347d5-116">В интерфейсе сеанса [IMAPISession](imapisessioniunknown.md)используется результаты передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="347d5-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="347d5-117">Параметр _lpInterfaceDst_ также может иметь значение IID_IMsgServiceAdmin.</span><span class="sxs-lookup"><span data-stu-id="347d5-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="347d5-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="347d5-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="347d5-119">[in] Указатель на указатель на объект администрирования службы сеанса или сообщения.</span><span class="sxs-lookup"><span data-stu-id="347d5-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="347d5-120">Тип объекта, должен соответствовать идентификатор интерфейса, переданные в _lpInterfaceDst_.</span><span class="sxs-lookup"><span data-stu-id="347d5-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="347d5-121">Допустимый объект указатели — LPMAPISESSION и LPSERVICEADMIN.</span><span class="sxs-lookup"><span data-stu-id="347d5-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="347d5-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="347d5-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="347d5-123">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="347d5-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="347d5-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="347d5-124">_ulFlags_</span></span>
  
> <span data-ttu-id="347d5-125">[in] Битовая маска флаги, который определяет, как скопировать службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="347d5-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="347d5-126">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="347d5-126">The following flags can be set:</span></span>
    
<span data-ttu-id="347d5-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="347d5-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="347d5-128">Запросы на том, что служба сообщений всегда отображаются на листе свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="347d5-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="347d5-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="347d5-129">Return value</span></span>

<span data-ttu-id="347d5-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="347d5-130">S_OK</span></span> 
  
> <span data-ttu-id="347d5-131">Служба сообщений успешно скопирована.</span><span class="sxs-lookup"><span data-stu-id="347d5-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="347d5-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="347d5-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="347d5-133">Служба сообщений уже в профиле и не допускает несколько экземпляров.</span><span class="sxs-lookup"><span data-stu-id="347d5-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="347d5-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="347d5-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="347d5-135">**MAPIUID** , на который указывает _lpUID_ не относится к существующей службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="347d5-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="347d5-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="347d5-136">Remarks</span></span>

<span data-ttu-id="347d5-137">Метод **IMsgServiceAdmin::CopyMsgService** копирует службы сообщений в профиль текущей конфигурации или другого профиля.</span><span class="sxs-lookup"><span data-stu-id="347d5-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="347d5-138">Профиль, который содержит службы сообщений для копирования и назначение не должны быть одного профиля, но они могут быть.</span><span class="sxs-lookup"><span data-stu-id="347d5-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="347d5-139">Служба сообщений функции точки входа не вызывается для операции копирования.</span><span class="sxs-lookup"><span data-stu-id="347d5-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="347d5-140">Служба скопированной сообщение имеет те же параметры конфигурации, что его исходный.</span><span class="sxs-lookup"><span data-stu-id="347d5-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="347d5-141">Чтобы изменить эти параметры, клиент должен вызвать метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="347d5-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="347d5-142">См. также</span><span class="sxs-lookup"><span data-stu-id="347d5-142">See also</span></span>



[<span data-ttu-id="347d5-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="347d5-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="347d5-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="347d5-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="347d5-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="347d5-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

