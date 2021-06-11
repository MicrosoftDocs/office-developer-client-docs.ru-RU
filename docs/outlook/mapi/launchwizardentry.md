---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437387"
---
# <a name="launchwizardentry"></a><span data-ttu-id="5e6be-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="5e6be-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="5e6be-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e6be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e6be-105">Определяет функцию, которая запускает приложение Мастер профилей для добавления одной или более служб сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="5e6be-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e6be-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5e6be-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e6be-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="5e6be-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="5e6be-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="5e6be-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5e6be-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e6be-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e6be-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="5e6be-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5e6be-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="5e6be-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="5e6be-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5e6be-112">Parameters</span></span>

 <span data-ttu-id="5e6be-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="5e6be-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="5e6be-114">[in] Ручка родительского окна вызываемого.</span><span class="sxs-lookup"><span data-stu-id="5e6be-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="5e6be-115">Если у вызываемого нет родительского окна,  _параметром hParentWnd_ должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5e6be-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="5e6be-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e6be-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5e6be-117">[in] Bitmask флагов с указанием параметров мастера профиля.</span><span class="sxs-lookup"><span data-stu-id="5e6be-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="5e6be-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5e6be-118">The following flags can be set:</span></span>
    
<span data-ttu-id="5e6be-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="5e6be-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="5e6be-120">Мастер профилей должен добавлять только службы сообщений, перечисленные через параметр  _lppszServiceNameToAdd,_ а не отображать свою страницу для выбора служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="5e6be-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="5e6be-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="5e6be-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="5e6be-122">Созданный профиль является первым для этой рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="5e6be-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="5e6be-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="5e6be-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="5e6be-124">Страница мастера профилей для выбора служб сообщений не должна отображаться.</span><span class="sxs-lookup"><span data-stu-id="5e6be-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="5e6be-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="5e6be-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="5e6be-126">Мастер профилей был запущен приложением конфигурации панели управления.</span><span class="sxs-lookup"><span data-stu-id="5e6be-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="5e6be-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="5e6be-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="5e6be-128">Должны отображаться только диалоговые окна конфигурации поставщиков услуг, а страницы мастера профилей не отображаются.</span><span class="sxs-lookup"><span data-stu-id="5e6be-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="5e6be-129">Этот флаг можно установить, только если MAPI_PW_ADD_SERVICE_ONLY заданной.</span><span class="sxs-lookup"><span data-stu-id="5e6be-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="5e6be-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="5e6be-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="5e6be-131">[in] Указатель на массив строк, содержащий имена служб сообщений, которые будут добавлены в профиль.</span><span class="sxs-lookup"><span data-stu-id="5e6be-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="5e6be-132">Массив должен завершиться со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="5e6be-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="5e6be-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="5e6be-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="5e6be-134">[in] Размер буфера, на который указывает параметр _lpszNewProfileName._</span><span class="sxs-lookup"><span data-stu-id="5e6be-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="5e6be-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="5e6be-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="5e6be-136">[вышел] Указатель на буфер строки, где функция на основе **LAUNCHWIZARDENTRY** возвращает имя созданного профиля.</span><span class="sxs-lookup"><span data-stu-id="5e6be-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e6be-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e6be-137">Return value</span></span>

<span data-ttu-id="5e6be-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e6be-138">S_OK</span></span> 
  
> <span data-ttu-id="5e6be-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5e6be-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="5e6be-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="5e6be-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="5e6be-141">Ошибка неожиданного или неизвестного происхождения не позволяет завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="5e6be-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="5e6be-142">К числу возможных вариантов относятся неисполнение инициализации подсистемы MAPI для мастера профилей, невозможность доступа к профилю по умолчанию и возврат ошибок из диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5e6be-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e6be-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e6be-143">Remarks</span></span>

<span data-ttu-id="5e6be-144">Реализация прототипа функции **LAUNCHWIZARDENTRY** MAPI является точкой входа в приложение Мастер профилей MAPI.</span><span class="sxs-lookup"><span data-stu-id="5e6be-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="5e6be-145">MAPI называет эту точку **входа LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="5e6be-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="5e6be-146">Когда флаг MAPI_PW_ADD_SERVICE_ONLY в параметре  _ulFlags,_ применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="5e6be-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="5e6be-147">Флаг MAPI_PW_LAUNCHED_BY_CONFIG отобразится на странице приветствия.</span><span class="sxs-lookup"><span data-stu-id="5e6be-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="5e6be-148">Флаги MAPI_PW_HIDE_SERVICES_LIST и MAPI_PW_PROVIDER_UI_ONLY полезны только при отсутствие профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5e6be-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="5e6be-149">В этом случае эти флаги определяют, какая страница мастера профилей должна отображаться.</span><span class="sxs-lookup"><span data-stu-id="5e6be-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="5e6be-150">Если профиль по умолчанию существует, ни одна из страниц мастера профилей не должна отображаться.</span><span class="sxs-lookup"><span data-stu-id="5e6be-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="5e6be-151">Если профиль по умолчанию существует, через параметр  _lppszServiceNameToAdd_ перечислены только одна служба сообщений, и эта служба сообщений уже находится в профиле по умолчанию, мастер профилей возвращает S_OK, ничего не добавляя в профиль.</span><span class="sxs-lookup"><span data-stu-id="5e6be-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="5e6be-152">Чтобы каждая служба сообщений была добавлена в профиль, мастер профилей вызывает функцию точки входа службы на основе прототипа [MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="5e6be-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="5e6be-153">Чтобы каждый поставщик услуг, выбранный из службы сообщений, добавляемой в профиль, вызывает функцию точки входа поставщика на основе прототипа [WIZARDENTRY.](wizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="5e6be-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="5e6be-154">Во время интерактивной конфигурации каждое событие пользователя на страницах свойств заставляет мастера профиля вызывать функцию вызова поставщика на основе прототипа [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md)</span><span class="sxs-lookup"><span data-stu-id="5e6be-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="5e6be-155">Если поставщик услуг, добавляемый в профиль, поддерживает страницы мастера профилей, он должен разрешить программную конфигурацию профиля.</span><span class="sxs-lookup"><span data-stu-id="5e6be-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

