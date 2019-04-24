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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270191"
---
# <a name="launchwizardentry"></a><span data-ttu-id="f8517-103">LAUNCHWIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="f8517-103">LAUNCHWIZARDENTRY</span></span>

  
  
<span data-ttu-id="f8517-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8517-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8517-105">Определяет функцию, которая запускает приложение мастера профилей в целях добавления одной или нескольких служб сообщений в профиль.</span><span class="sxs-lookup"><span data-stu-id="f8517-105">Defines a function that starts the Profile Wizard application for the purpose of adding one or more message services to a profile.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f8517-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f8517-106">Header file:</span></span>  <br/> |<span data-ttu-id="f8517-107">Мапивз. h</span><span class="sxs-lookup"><span data-stu-id="f8517-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="f8517-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f8517-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="f8517-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f8517-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f8517-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="f8517-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="f8517-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="f8517-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a><span data-ttu-id="f8517-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8517-112">Parameters</span></span>

 <span data-ttu-id="f8517-113">_Хпарентвнд_</span><span class="sxs-lookup"><span data-stu-id="f8517-113">_hParentWnd_</span></span>
  
> <span data-ttu-id="f8517-114">возврата Дескриптор родительского окна вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="f8517-114">[in] A handle to the caller's parent window.</span></span> <span data-ttu-id="f8517-115">Если у вызывающего абонента нет родительского окна, параметр _хпарентвнд_ должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="f8517-115">If the caller does not have a parent window, the  _hParentWnd_ parameter should be NULL.</span></span> 
    
 <span data-ttu-id="f8517-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8517-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f8517-117">возврата Битовая маска флагов, указывающих параметры для мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="f8517-117">[in] Bitmask of flags indicating options for the Profile Wizard.</span></span> <span data-ttu-id="f8517-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f8517-118">The following flags can be set:</span></span>
    
<span data-ttu-id="f8517-119">МАПИ_ПВ_АДД_СЕРВИЦЕ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="f8517-119">MAPI_PW_ADD_SERVICE_ONLY</span></span> 
  
> <span data-ttu-id="f8517-120">С помощью мастера профилей можно добавить только службы сообщений, перечисленные с помощью параметра _лппсзсервиценаметоадд_ , и не отображать его страницу для выбора служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="f8517-120">The Profile Wizard is to add only the message services listed through the  _lppszServiceNameToAdd_ parameter, and not display its page for selecting message services.</span></span> 
    
<span data-ttu-id="f8517-121">МАПИ_ПВ_ФИРСТ_ПРОФИЛЕ</span><span class="sxs-lookup"><span data-stu-id="f8517-121">MAPI_PW_FIRST_PROFILE</span></span> 
  
> <span data-ttu-id="f8517-122">Профиль, который необходимо создать, является первым для этой рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="f8517-122">The profile to be created is the first one for this workstation.</span></span> 
    
<span data-ttu-id="f8517-123">МАПИ_ПВ_ХИДЕ_СЕРВИЦЕС_ЛИСТ</span><span class="sxs-lookup"><span data-stu-id="f8517-123">MAPI_PW_HIDE_SERVICES_LIST</span></span> 
  
> <span data-ttu-id="f8517-124">Не отображается страница мастера профилей для выбора служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="f8517-124">The Profile Wizard's page for selecting message services should not be displayed.</span></span> 
    
<span data-ttu-id="f8517-125">МАПИ_ПВ_ЛАУНЧЕД_БИ_КОНФИГ</span><span class="sxs-lookup"><span data-stu-id="f8517-125">MAPI_PW_LAUNCHED_BY_CONFIG</span></span> 
  
> <span data-ttu-id="f8517-126">Мастер профилей запущен приложением настройки панели управления.</span><span class="sxs-lookup"><span data-stu-id="f8517-126">The Profile Wizard was launched by the Control Panel configuration application.</span></span> 
    
<span data-ttu-id="f8517-127">МАПИ_ПВ_ПРОВИДЕР_УИ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="f8517-127">MAPI_PW_PROVIDER_UI_ONLY</span></span> 
  
> <span data-ttu-id="f8517-128">Должны отображаться только диалоговые окна настройки поставщиков услуг, и не должны отображаться страницы мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="f8517-128">Only the service providers's configuration dialog boxes should be displayed and the Profile Wizard's pages should not appear.</span></span> <span data-ttu-id="f8517-129">Этот флаг можно задать, только если установлен флаг МАПИ_ПВ_АДД_СЕРВИЦЕ_ОНЛИ.</span><span class="sxs-lookup"><span data-stu-id="f8517-129">This flag can only be set if the MAPI_PW_ADD_SERVICE_ONLY flag is set.</span></span> 
    
 <span data-ttu-id="f8517-130">_Лппсзсервиценаметоадд_</span><span class="sxs-lookup"><span data-stu-id="f8517-130">_lppszServiceNameToAdd_</span></span>
  
> <span data-ttu-id="f8517-131">возврата Указатель на массив строк, содержащий имена служб сообщений, которые необходимо добавить в профиль.</span><span class="sxs-lookup"><span data-stu-id="f8517-131">[in] Pointer to an array of strings that contains the names of the message services to be added to the profile.</span></span> <span data-ttu-id="f8517-132">Массив должен завершаться значением NULL.</span><span class="sxs-lookup"><span data-stu-id="f8517-132">The array must terminate with a NULL value.</span></span> 
    
 <span data-ttu-id="f8517-133">_Кббуффермакс_</span><span class="sxs-lookup"><span data-stu-id="f8517-133">_cbBufferMax_</span></span>
  
> <span data-ttu-id="f8517-134">возврата Размер буфера, на который указывает параметр _лпсзневпрофиленаме_ .</span><span class="sxs-lookup"><span data-stu-id="f8517-134">[in] Size of the buffer pointed to by the  _lpszNewProfileName_ parameter.</span></span> 
    
 <span data-ttu-id="f8517-135">_Лпсзневпрофиленаме_</span><span class="sxs-lookup"><span data-stu-id="f8517-135">_lpszNewProfileName_</span></span>
  
> <span data-ttu-id="f8517-136">вышли Указатель на буфер строки, в котором функция на основе **лаунчвизардентри** возвращает имя созданного профиля.</span><span class="sxs-lookup"><span data-stu-id="f8517-136">[out] Pointer to a string buffer where the function based on **LAUNCHWIZARDENTRY** returns the name of the created profile.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f8517-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8517-137">Return value</span></span>

<span data-ttu-id="f8517-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8517-138">S_OK</span></span> 
  
> <span data-ttu-id="f8517-139">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f8517-139">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f8517-140">МАПИ_Е_КАЛЛ_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="f8517-140">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f8517-141">Не удалось завершить операцию из — из — из — из — из — из — из неизвестного источника.</span><span class="sxs-lookup"><span data-stu-id="f8517-141">An error of unexpected or unknown origin prevented the operation from completing.</span></span> <span data-ttu-id="f8517-142">Возможные варианты: сбой инициализации подсистемы MAPI для мастера профилей, невозможность доступа к профилю по умолчанию, а также возвращение ошибки из диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f8517-142">Possibilities include failure to initialize the MAPI subsystem for the Profile Wizard, inability to access the default profile, and an error return from the dialog box.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8517-143">Замечания</span><span class="sxs-lookup"><span data-stu-id="f8517-143">Remarks</span></span>

<span data-ttu-id="f8517-144">Реализация функции MAPI для прототипа функции **лаунчвизардентри** — точка входа в приложение мастера профилей MAPI.</span><span class="sxs-lookup"><span data-stu-id="f8517-144">The MAPI implementation of the **LAUNCHWIZARDENTRY** function prototype is the entry point into the MAPI Profile Wizard application.</span></span> <span data-ttu-id="f8517-145">MAPI Names указывает эту точку входа **лаунчвизард**.</span><span class="sxs-lookup"><span data-stu-id="f8517-145">MAPI names this entry point **LaunchWizard**.</span></span> 
  
<span data-ttu-id="f8517-146">Если в параметре _ulFlags_ ЗАДАН флаг мапи_пв_адд_сервице_онли, применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="f8517-146">When the MAPI_PW_ADD_SERVICE_ONLY flag is set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="f8517-147">Флаг МАПИ_ПВ_ЛАУНЧЕД_БИ_КОНФИГ запрещает отображение страницы приветствия.</span><span class="sxs-lookup"><span data-stu-id="f8517-147">The MAPI_PW_LAUNCHED_BY_CONFIG flag inhibits the welcome page from being displayed.</span></span> 
    
- <span data-ttu-id="f8517-148">Флаги МАПИ_ПВ_ХИДЕ_СЕРВИЦЕС_ЛИСТ и МАПИ_ПВ_ПРОВИДЕР_УИ_ОНЛИ можно использовать только в том случае, если профиль по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="f8517-148">The MAPI_PW_HIDE_SERVICES_LIST and MAPI_PW_PROVIDER_UI_ONLY flags are useful only when there is no default profile.</span></span> <span data-ttu-id="f8517-149">В этом случае эти флаги определяют, какую страницу мастера профилей следует отображать.</span><span class="sxs-lookup"><span data-stu-id="f8517-149">In this case these flags determine which Profile Wizard page is to be displayed.</span></span> 
    
- <span data-ttu-id="f8517-150">Если профиль по умолчанию существует, не будут отображаться никакие страницы мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="f8517-150">If a default profile exists, none of the Profile Wizard pages are to be displayed.</span></span> 
    
- <span data-ttu-id="f8517-151">Если профиль по умолчанию существует, только одна служба сообщений перечислена через параметр _лппсзсервиценаметоадд_ , и эта служба сообщений уже включена в профиль по умолчанию, мастер профилей ВОЗВРАЩАЕТ значение S_OK без добавления в профиль.</span><span class="sxs-lookup"><span data-stu-id="f8517-151">If a default profile exists, only one message service is listed through the  _lppszServiceNameToAdd_ parameter, and that message service is already in the default profile, the Profile Wizard returns S_OK without adding anything to the profile.</span></span> 
    
<span data-ttu-id="f8517-152">Для каждой службы сообщений, добавляемой в профиль, мастер профилей вызывает функцию точки входа службы на основе прототипа [мсгсервицеентри](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="f8517-152">For every message service to be added to the profile, the Profile Wizard calls the service's entry point function based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="f8517-153">Для каждого поставщика услуг, выбранного из службы сообщений, добавляемого в профиль, мастер профилей вызывает функцию точки входа поставщика на основе прототипа [визардентри](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="f8517-153">For each service provider selected from a message service to be added to the profile, the Profile Wizard calls the provider's entry point function based on the [WIZARDENTRY](wizardentry.md) prototype.</span></span> <span data-ttu-id="f8517-154">Во время интерактивной конфигурации каждое событие пользователя на страницах свойств заставляет мастер профилей вызывать функцию обратного вызова поставщика на основе прототипа [сервицевизарддлгпрок](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="f8517-154">During interactive configuration, every user event in the property pages causes the Profile Wizard to call the provider's callback function based on the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
  
<span data-ttu-id="f8517-155">Если поставщик услуг, добавляемый в профиль, поддерживает страницы мастера профилей, он должен разрешить программную конфигурацию профиля.</span><span class="sxs-lookup"><span data-stu-id="f8517-155">If a service provider being added to the profile supports the Profile Wizard pages, it must allow programmatic configuration of the profile.</span></span>
  

