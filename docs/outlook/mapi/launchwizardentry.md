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
ms.openlocfilehash: f2cc9a6f97fa51a255f8c24c2bb52c912aef7718
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566252"
---
# <a name="launchwizardentry"></a><span data-ttu-id="56e5e-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="56e5e-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="56e5e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56e5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56e5e-105">Определяет функцию, которая запускает мастер профиля приложения для добавления одной или нескольких служб сообщения в профиль.</span><span class="sxs-lookup"><span data-stu-id="56e5e-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56e5e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="56e5e-106">Header file:</span></span>  <br/> |<span data-ttu-id="56e5e-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="56e5e-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="56e5e-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="56e5e-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="56e5e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="56e5e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="56e5e-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="56e5e-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="56e5e-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="56e5e-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="56e5e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="56e5e-112">Parameters</span></span>

 <span data-ttu-id="56e5e-113">_hParentWnd_</span><span class="sxs-lookup"><span data-stu-id="56e5e-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="56e5e-114">[in] Дескриптор родительского окна вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="56e5e-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="56e5e-115">Если вызывающий не имеет родительского окна, параметр _hParentWnd_ должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="56e5e-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="56e5e-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56e5e-116">_ulFlags_</span></span>
  
> <span data-ttu-id="56e5e-117">[in] Битовая маска, указывающее, параметры для мастера профиль флаги.</span><span class="sxs-lookup"><span data-stu-id="56e5e-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="56e5e-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="56e5e-118">The following flags can be set:</span></span>
    
<span data-ttu-id="56e5e-119">MAPI_PW_ADD_SERVICE_ONLY</span><span class="sxs-lookup"><span data-stu-id="56e5e-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="56e5e-120">Мастер профиля является добавление службы сообщений, перечисленных через параметр _lppszServiceNameToAdd_ и отображает его страницы для выбора службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="56e5e-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="56e5e-121">MAPI_PW_FIRST_PROFILE</span><span class="sxs-lookup"><span data-stu-id="56e5e-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="56e5e-122">Профиль будет создан является первым для данной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="56e5e-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="56e5e-123">MAPI_PW_HIDE_SERVICES_LIST</span><span class="sxs-lookup"><span data-stu-id="56e5e-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="56e5e-124">Страница мастера профиля для выбора службы сообщений не должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="56e5e-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="56e5e-125">MAPI_PW_LAUNCHED_BY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="56e5e-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="56e5e-126">В приложении настройки панели управления был запущен мастер профилей.</span><span class="sxs-lookup"><span data-stu-id="56e5e-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="56e5e-127">MAPI_PW_PROVIDER_UI_ONLY</span><span class="sxs-lookup"><span data-stu-id="56e5e-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="56e5e-128">Отображать только поставщиков услуг конфигурации диалоговых окон и страницах мастера профилей не должно быть.</span><span class="sxs-lookup"><span data-stu-id="56e5e-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="56e5e-129">Этот флаг могут быть установлены только в том случае, если установлен флаг MAPI_PW_ADD_SERVICE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="56e5e-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="56e5e-130">_lppszServiceNameToAdd_</span><span class="sxs-lookup"><span data-stu-id="56e5e-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="56e5e-131">[in] Указатель на массив строк, содержащий имена службы сообщений для добавления к профилю.</span><span class="sxs-lookup"><span data-stu-id="56e5e-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="56e5e-132">Массив должен завершать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="56e5e-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="56e5e-133">_cbBufferMax_</span><span class="sxs-lookup"><span data-stu-id="56e5e-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="56e5e-134">[in] Размер буфера, на который указывает параметр _lpszNewProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="56e5e-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="56e5e-135">_lpszNewProfileName_</span><span class="sxs-lookup"><span data-stu-id="56e5e-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="56e5e-136">[out] Указатель на буфер строки, где на основании **LAUNCHWIZARDENTRY** функция возвращает имя созданного профиля.</span><span class="sxs-lookup"><span data-stu-id="56e5e-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="56e5e-137">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="56e5e-137">Return value</span></span>

<span data-ttu-id="56e5e-138">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="56e5e-138">S_OK</span></span> 
  
> <span data-ttu-id="56e5e-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="56e5e-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="56e5e-140">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="56e5e-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="56e5e-141">Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="56e5e-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="56e5e-142">Возможны следующие варианты не удалось инициализировать подсистему MAPI для мастера профилей, невозможность доступа профиля по умолчанию и Ошибка возврата из диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="56e5e-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="56e5e-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="56e5e-143">Remarks</span></span>

<span data-ttu-id="56e5e-144">Реализация интерфейса MAPI прототип функции **LAUNCHWIZARDENTRY** является точка входа для приложения мастера профилей MAPI.</span><span class="sxs-lookup"><span data-stu-id="56e5e-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="56e5e-145">MAPI имена эта точка входа **LaunchWizard**.</span><span class="sxs-lookup"><span data-stu-id="56e5e-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="56e5e-146">Если в параметре _ulFlags_ флаг MAPI_PW_ADD_SERVICE_ONLY, применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="56e5e-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="56e5e-147">Флаг MAPI_PW_LAUNCHED_BY_CONFIG этот параметр запрещает начальная страница отображаются.</span><span class="sxs-lookup"><span data-stu-id="56e5e-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="56e5e-148">Флаги MAPI_PW_HIDE_SERVICES_LIST и MAPI_PW_PROVIDER_UI_ONLY полезны только в том случае, если профиль не по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56e5e-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="56e5e-149">В этом случае эти флаги определить, какой мастер профилей, будет отображаться страница.</span><span class="sxs-lookup"><span data-stu-id="56e5e-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="56e5e-150">Если с профилем по умолчанию, нет на страницах мастера профилей, для отображения.</span><span class="sxs-lookup"><span data-stu-id="56e5e-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="56e5e-151">Если с профилем по умолчанию, через параметр _lppszServiceNameToAdd_ указана только одно сообщение служба и служба сообщений уже профиля по умолчанию, мастер профиля возвращает значение S_OK, не добавляя все действия в профиль.</span><span class="sxs-lookup"><span data-stu-id="56e5e-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="56e5e-152">Для каждой службы сообщения добавляется к профилю мастер профилей вызывает функцию точки входа службы на основании прототип [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="56e5e-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="56e5e-153">Для каждого поставщика служб, выбранные из службы сообщений для добавления к профилю мастер профилей вызывает функцию точки входа поставщика на основании прототип [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="56e5e-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="56e5e-154">Во время интерактивного настройки мастер профиля для вызова функции обратного вызова поставщика, основанной на прототип [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) вызывает событие каждого пользователя в страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="56e5e-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="56e5e-155">Если поставщик услуг, добавляемый к профилю поддерживает на страницах мастера профилей, его необходимо разрешить программный настройки профиля.</span><span class="sxs-lookup"><span data-stu-id="56e5e-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

