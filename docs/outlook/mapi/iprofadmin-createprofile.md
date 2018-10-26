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
ms.openlocfilehash: 92d5dcdf3e5e3fbdb7490d777a24976c9ae4af1a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582793"
---
# <a name="iprofadmincreateprofile"></a><span data-ttu-id="435fb-103">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="435fb-103">IProfAdmin::CreateProfile</span></span>

  
  
<span data-ttu-id="435fb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="435fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="435fb-105">Создает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="435fb-105">Creates a new profile.</span></span>
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="435fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="435fb-106">Parameters</span></span>

 <span data-ttu-id="435fb-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="435fb-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="435fb-108">[in] Указатель на имя нового профиля.</span><span class="sxs-lookup"><span data-stu-id="435fb-108">[in] A pointer to the name of the new profile.</span></span>
    
 <span data-ttu-id="435fb-109">_lpszPassword_</span><span class="sxs-lookup"><span data-stu-id="435fb-109">_lpszPassword_</span></span>
  
> <span data-ttu-id="435fb-110">[in] Указатель на пароль нового профиля.</span><span class="sxs-lookup"><span data-stu-id="435fb-110">[in] A pointer to the password of the new profile.</span></span> 
    
 <span data-ttu-id="435fb-111">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="435fb-111">_ulUIParam_</span></span>
  
> <span data-ttu-id="435fb-112">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="435fb-112">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="435fb-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="435fb-113">_ulFlags_</span></span>
  
> <span data-ttu-id="435fb-114">[in] Битовая маска флаги, который определяет способ создания профилей.</span><span class="sxs-lookup"><span data-stu-id="435fb-114">[in] A bitmask of flags that controls how the profile is created.</span></span> <span data-ttu-id="435fb-115">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="435fb-115">The following flags can be set:</span></span>
    
<span data-ttu-id="435fb-116">MAPI_DEFAULT_SERVICES</span><span class="sxs-lookup"><span data-stu-id="435fb-116">MAPI_DEFAULT_SERVICES</span></span> 
  
> <span data-ttu-id="435fb-117">MAPI должен заполнить новый профиль с помощью службы сообщений, которые включены в разделе [службы по умолчанию] файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="435fb-117">MAPI should populate the new profile with the message services that are included in the [Default Services] section of the Mapisvc.inf file.</span></span>
    
<span data-ttu-id="435fb-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="435fb-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="435fb-119">Отображения свойств конфигурации всех поставщиков в службах сообщение будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="435fb-119">The configuration property sheets of each of the providers in the message services to be added can be displayed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="435fb-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="435fb-120">Return value</span></span>

<span data-ttu-id="435fb-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="435fb-121">S_OK</span></span> 
  
> <span data-ttu-id="435fb-122">Был создан новый профиль.</span><span class="sxs-lookup"><span data-stu-id="435fb-122">The new profile was created.</span></span>
    
<span data-ttu-id="435fb-123">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="435fb-123">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="435fb-124">Указанный новый профиль уже существует.</span><span class="sxs-lookup"><span data-stu-id="435fb-124">The specified new profile already exists.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="435fb-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="435fb-125">Remarks</span></span>

<span data-ttu-id="435fb-126">Метод **IProfAdmin::CreateProfile** создает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="435fb-126">The **IProfAdmin::CreateProfile** method creates a new profile.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="435fb-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="435fb-127">Notes to callers</span></span>

<span data-ttu-id="435fb-128">Можно вызвать **CreateProfile** во время установки приложения или в любой момент во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="435fb-128">You can call **CreateProfile** at application installation time or at any time during a session.</span></span> <span data-ttu-id="435fb-129">Когда этот метод вызывается во время установки, многие из параметров конфигурации поступают из конфигурации файла Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="435fb-129">When this method is called at installation time, many of the configuration settings come from the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="435fb-130">Когда этот метод вызывается во время активного сеанса, параметры поступают от пользователя, который будет запрашиваться ряд свойств.</span><span class="sxs-lookup"><span data-stu-id="435fb-130">When this method is called during an active session, the settings come from the user who is prompted through a series of property sheets.</span></span> 
  
<span data-ttu-id="435fb-131">Если в параметре _ulFlags_ флаг MAPI_DEFAULT_SERVICES, **CreateProfile** вызывает функцию точки входа службы сообщений для каждой службы сообщений в разделе [службы по умолчанию] в файле Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="435fb-131">If the MAPI_DEFAULT_SERVICES flag is set in the  _ulFlags_ parameter, **CreateProfile** calls the message service entry point function for each message service in the [Default Services] section in the Mapisvc.inf file.</span></span> <span data-ttu-id="435fb-132">Каждой функции точки входа службы сообщений вызывается с параметром _ulContext_ установлено значение MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="435fb-132">Each message service entry point function is called with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
  
<span data-ttu-id="435fb-133">Если установлены флаги MAPI_DIALOG и MAPI_DEFAULT_SERVICES, значения в параметрах _ulUIParam_ и _ulFlags_ также передаются в функцию точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="435fb-133">If both the MAPI_DIALOG and MAPI_DEFAULT_SERVICES flags are set, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the message service entry point function.</span></span> <span data-ttu-id="435fb-134">Функции точка входа службы сообщений, называются только после все доступные сведения из файла Mapisvc.inf был добавлен к профилю.</span><span class="sxs-lookup"><span data-stu-id="435fb-134">The message service entry point functions are called only after all available information from the Mapisvc.inf file has been added to the profile.</span></span> 
  
<span data-ttu-id="435fb-135">Имя нового профиля и его пароль может быть длиной до 64 символов и может содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="435fb-135">The name of the new profile and its password can be up to 64 characters in length and can include the following characters:</span></span>
  
- <span data-ttu-id="435fb-136">Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="435fb-136">All alphanumeric characters, including accent characters and the underscore character.</span></span>
    
- <span data-ttu-id="435fb-137">Пробелы, но не начальных и конечных пробелов.</span><span class="sxs-lookup"><span data-stu-id="435fb-137">Embedded spaces, but not leading or trailing spaces.</span></span>
    
<span data-ttu-id="435fb-138">Параметр _lpszPassword_ должен быть NULL или указатель на строку нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="435fb-138">The  _lpszPassword_ parameter must be NULL or a pointer to a zero-length string.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="435fb-139">См. также</span><span class="sxs-lookup"><span data-stu-id="435fb-139">See also</span></span>



[<span data-ttu-id="435fb-140">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="435fb-140">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="435fb-141">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="435fb-141">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="435fb-142">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="435fb-142">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="435fb-143">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="435fb-143">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

