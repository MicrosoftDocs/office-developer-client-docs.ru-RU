---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404402"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="8afa4-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="8afa4-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="8afa4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8afa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8afa4-105">Создает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="8afa4-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8afa4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="8afa4-106">Parameters</span></span>

 <span data-ttu-id="8afa4-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="8afa4-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="8afa4-108">[in] Указатель на имя нового профиля.</span><span class="sxs-lookup"><span data-stu-id="8afa4-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="8afa4-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="8afa4-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="8afa4-110">[in] Указатель на пароль нового профиля.</span><span class="sxs-lookup"><span data-stu-id="8afa4-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="8afa4-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8afa4-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="8afa4-112">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="8afa4-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="8afa4-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8afa4-113">_ulFlags_</span></span>
  
> <span data-ttu-id="8afa4-114">[in] Битмаски флагов, которые контролируют, как создается профиль.</span><span class="sxs-lookup"><span data-stu-id="8afa4-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="8afa4-115">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="8afa4-115">The following flags can be set:</span></span>
    
<span data-ttu-id="8afa4-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="8afa4-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="8afa4-117">MAPI должна заполнить новый профиль службами сообщений, включенными в раздел [Службы по умолчанию] файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8afa4-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="8afa4-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8afa4-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8afa4-119">Можно отобразить листы свойств конфигурации каждого из поставщиков в добавленных службах сообщений.</span><span class="sxs-lookup"><span data-stu-id="8afa4-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8afa4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8afa4-120">Return value</span></span>

<span data-ttu-id="8afa4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8afa4-121">S_OK</span></span> 
  
> <span data-ttu-id="8afa4-122">Был создан новый профиль.</span><span class="sxs-lookup"><span data-stu-id="8afa4-122">The new profile was created.</span></span>
    
<span data-ttu-id="8afa4-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8afa4-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8afa4-124">Указанный новый профиль уже существует.</span><span class="sxs-lookup"><span data-stu-id="8afa4-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8afa4-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="8afa4-125">Remarks</span></span>

<span data-ttu-id="8afa4-126">Метод **IProfAdmin::CreateProfile** создает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="8afa4-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8afa4-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="8afa4-127">Notes to callers</span></span>

<span data-ttu-id="8afa4-128">Вы можете вызвать **CreateProfile** во время установки приложения или в любое время во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="8afa4-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="8afa4-129">Когда этот метод вызван во время установки, многие параметры конфигурации приходят из файла конфигурации Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8afa4-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="8afa4-130">Когда этот метод вызван во время активного сеанса, параметры приходят от пользователя, которому подсказывался ряд листов свойств.</span><span class="sxs-lookup"><span data-stu-id="8afa4-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="8afa4-131">Если флаг MAPI_DEFAULT_SERVICES установлен в параметре  _ulFlags,_ **CreateProfile** вызывает функцию точки входа службы сообщений для каждой службы сообщений в разделе [Службы по умолчанию] в файле Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8afa4-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="8afa4-132">Каждая функция точки входа службы сообщений называется с параметром  _ulContext,_ заданным MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="8afa4-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="8afa4-133">Если заданы MAPI_DIALOG и MAPI_DEFAULT_SERVICES флаги, значения  _ulUIParam_ и  _ulFlags_ также передаются функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="8afa4-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="8afa4-134">Функции точки входа службы сообщений называются только после того, как в профиль будут добавлены все доступные сведения из файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="8afa4-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="8afa4-135">Имя нового профиля и его пароль могут иметь длину до 64 символов и включать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="8afa4-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="8afa4-136">Все буквы, включая символы акцента и символы подчеркнуть.</span><span class="sxs-lookup"><span data-stu-id="8afa4-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="8afa4-137">Встроенные пробелы, но не ведущие и не ведущие.</span><span class="sxs-lookup"><span data-stu-id="8afa4-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="8afa4-138">Параметр  _lpszPassword должен_ быть NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="8afa4-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8afa4-139">См. также</span><span class="sxs-lookup"><span data-stu-id="8afa4-139">See also</span></span>



[<span data-ttu-id="8afa4-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="8afa4-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="8afa4-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="8afa4-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="8afa4-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="8afa4-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="8afa4-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8afa4-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

