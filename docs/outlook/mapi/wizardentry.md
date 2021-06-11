---
title: WIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WIZARDENTRY
api_type:
- COM
ms.assetid: e807c6b5-06cd-4ade-9d9e-69ba6abd1614
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 907984a80dbb6c5464f95def1481d002f9d6638a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430681"
---
# <a name="wizardentry"></a><span data-ttu-id="50748-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="50748-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="50748-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50748-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50748-105">Определяет функцию точки входа поставщика услуг, которую мастер профилей вызывает для получения достаточного количества сведений для отображения листов свойств конфигурации поставщика.</span><span class="sxs-lookup"><span data-stu-id="50748-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50748-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="50748-106">Header file:</span></span>  <br/> |<span data-ttu-id="50748-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="50748-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="50748-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="50748-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="50748-109">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="50748-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="50748-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="50748-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="50748-111">Мастер профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="50748-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="50748-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="50748-112">Parameters</span></span>

 <span data-ttu-id="50748-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="50748-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="50748-114">[in] Экземпляр обработки DLL поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="50748-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="50748-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="50748-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="50748-116">[вышел] Указатель на строку, которая содержит полное имя диалогового ресурса, которое должно отображаться мастером профилей во время настройки.</span><span class="sxs-lookup"><span data-stu-id="50748-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="50748-117">Максимальный размер строки, включая терминатор NULL, — 32 символа.</span><span class="sxs-lookup"><span data-stu-id="50748-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="50748-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="50748-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="50748-119">[вышел] Указатель на стандартную процедуру Windows диалоговое окно, которое будет вызвано мастером профилей, чтобы уведомить поставщика о различных событиях.</span><span class="sxs-lookup"><span data-stu-id="50748-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="50748-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="50748-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="50748-121">[in] Указатель на реализацию интерфейса свойств, который предоставляет доступ к свойствам конфигурации.</span><span class="sxs-lookup"><span data-stu-id="50748-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="50748-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="50748-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="50748-123">[in] Указатель на объект поддержки MAPI, применимый к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="50748-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50748-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50748-124">Return value</span></span>

<span data-ttu-id="50748-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="50748-125">S_OK</span></span> 
  
> <span data-ttu-id="50748-126">Функция **WIZARDENTRY** поставщика услуг была вызвана успешно.</span><span class="sxs-lookup"><span data-stu-id="50748-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="50748-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="50748-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="50748-128">Ошибка неожиданного или неизвестного происхождения не позволяет завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="50748-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50748-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="50748-129">Remarks</span></span>

<span data-ttu-id="50748-130">Мастер профилей вызывает функцию **WIZARDENTRY,** когда она готова отображать пользовательский интерфейс конфигурации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="50748-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="50748-131">Когда мастер профилей завершает настройку всех поставщиков, он записывает свойства конфигурации в профиль, вызывая [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="50748-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="50748-132">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="50748-132">Notes to implementers</span></span>

<span data-ttu-id="50748-133">Имя функции **WIZARDENTRY** должно быть размещено в записи WIZARD_ENTRY_NAME MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="50748-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="50748-134">Имя ресурса — это имя диалогового ресурса, который будет отрисовки в области мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="50748-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="50748-135">Ресурс, который передается обратно, должен содержать все страницы в одном диалоговом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="50748-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="50748-136">Когда мастер профилей получает этот ресурс, он игнорирует стиль диалогов, но не стили управления, и создает все элементы управления в качестве детей страницы Мастер профилей.</span><span class="sxs-lookup"><span data-stu-id="50748-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="50748-137">Все элементы управления изначально скрыты.</span><span class="sxs-lookup"><span data-stu-id="50748-137">All controls are initially hidden.</span></span> <span data-ttu-id="50748-138">Поставщики должны убедиться, что координаты их элементов управления являются нулем или нулем и не превышают максимальную ширину 200 диалогов и максимальную высоту 150 диалогов.</span><span class="sxs-lookup"><span data-stu-id="50748-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="50748-139">Идентификаторы управления ниже 400 зарезервированы для мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="50748-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="50748-140">Мастер профилей отображает название поставщика в жирном тексте над пользовательским интерфейсом поставщика.</span><span class="sxs-lookup"><span data-stu-id="50748-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="50748-141">Указатель интерфейса свойств, поставленный в  _параметре lpMAPIProp,_ должен быть сохранен поставщиком для будущей ссылки.</span><span class="sxs-lookup"><span data-stu-id="50748-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="50748-142">Мастер профилей имеет дело только с самым базовым набором свойств, и поставщик может использовать реализацию интерфейса свойств, чтобы включить дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="50748-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="50748-143">Во время настройки поставщики должны добавить свои свойства конфигурации в объект, реализующий интерфейс свойства.</span><span class="sxs-lookup"><span data-stu-id="50748-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="50748-144">После настройки всех поставщиков мастер профилей добавляет эти свойства в профиль.</span><span class="sxs-lookup"><span data-stu-id="50748-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="50748-145">Дополнительные сведения об использовании этой функции см. в дополнительных [сведениях о поддержке конфигурации службы сообщений.](supporting-message-service-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="50748-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

