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
# <a name="wizardentry"></a><span data-ttu-id="8b856-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="8b856-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="8b856-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b856-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b856-105">Определяет функцию точки входа поставщика услуг, которая вызывается мастером профилей для получения достаточной информации для отображения страниц свойств конфигурации поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b856-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b856-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8b856-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b856-107">Мапивз. h</span><span class="sxs-lookup"><span data-stu-id="8b856-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="8b856-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8b856-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="8b856-109">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="8b856-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="8b856-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="8b856-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="8b856-111">Мастер профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="8b856-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="8b856-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b856-112">Parameters</span></span>

 <span data-ttu-id="8b856-113">_Хпровидердллинстанце_</span><span class="sxs-lookup"><span data-stu-id="8b856-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="8b856-114">возврата Дескриптор экземпляра DLL поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8b856-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="8b856-115">_Лпксресаурценаме_</span><span class="sxs-lookup"><span data-stu-id="8b856-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="8b856-116">вышли Указатель на строку, которая содержит полное имя ресурса диалога, который должен отображаться мастером профилей во время настройки.</span><span class="sxs-lookup"><span data-stu-id="8b856-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="8b856-117">Максимальный размер строки, включая знак завершения NULL, составляет 32 символов.</span><span class="sxs-lookup"><span data-stu-id="8b856-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="8b856-118">_Лппдлгпрок_</span><span class="sxs-lookup"><span data-stu-id="8b856-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="8b856-119">вышли Указатель на стандартную процедуру диалогового окна Windows, которая будет вызываться мастером профилей для уведомления поставщика о различных событиях.</span><span class="sxs-lookup"><span data-stu-id="8b856-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="8b856-120">_Лпмапипроп_</span><span class="sxs-lookup"><span data-stu-id="8b856-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="8b856-121">возврата Указатель на реализацию интерфейса свойств, который предоставляет доступ к свойствам конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8b856-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="8b856-122">_Лпмаписуппортобжект_</span><span class="sxs-lookup"><span data-stu-id="8b856-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="8b856-123">возврата Указатель на объект поддержки MAPI, применяемый к этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="8b856-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b856-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b856-124">Return value</span></span>

<span data-ttu-id="8b856-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b856-125">S_OK</span></span> 
  
> <span data-ttu-id="8b856-126">Функция **визардентри** поставщика услуг успешно вызвана.</span><span class="sxs-lookup"><span data-stu-id="8b856-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="8b856-127">МАПИ_Е_КАЛЛ_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="8b856-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="8b856-128">Не удалось завершить операцию из — из — из — из — из — из — из неизвестного источника.</span><span class="sxs-lookup"><span data-stu-id="8b856-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b856-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b856-129">Remarks</span></span>

<span data-ttu-id="8b856-130">Мастер профилей вызывает функцию на основе **визардентри** , когда она готова отобразить пользовательский интерфейс конфигурации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8b856-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="8b856-131">После завершения настройки всех поставщиков мастер профилей записывает свойства конфигурации в профиль, вызывая [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="8b856-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8b856-132">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8b856-132">Notes to implementers</span></span>

<span data-ttu-id="8b856-133">Имя функции на основе **визардентри** должно быть расположено в записи ВИЗАРД_ЕНТРИ_НАМЕ в Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="8b856-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="8b856-134">Имя ресурса это имя ресурса диалога, который будет отображаться на панели мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="8b856-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="8b856-135">Передаваемый им ресурс должен содержать все страницы в отдельном ресурсе диалога.</span><span class="sxs-lookup"><span data-stu-id="8b856-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="8b856-136">Когда мастер профилей получит этот ресурс, он игнорирует стиль диалогового окна, но не стили элемента управления, и создает все элементы управления как дочерние на странице мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="8b856-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="8b856-137">Все элементы управления изначально скрыты.</span><span class="sxs-lookup"><span data-stu-id="8b856-137">All controls are initially hidden.</span></span> <span data-ttu-id="8b856-138">Поставщики должны убедиться в том, что координаты для своих элементов управления имеют нулевое или нулевое значение, и что они не превышают максимальную ширину 200 и максимальную высоту единиц диалогового окна 150.</span><span class="sxs-lookup"><span data-stu-id="8b856-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="8b856-139">Идентификаторы элементов управления ниже 400 зарезервированы для мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="8b856-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="8b856-140">Мастер профилей отображает заголовок поставщика в полужирном тексте над пользовательским интерфейсом поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b856-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="8b856-141">Указатель интерфейса свойства, указанный в параметре _лпмапипроп_ , должен храниться у поставщика для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="8b856-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="8b856-142">Мастер профилей работает только с наиболее базовым набором свойств, и поставщик может использовать реализацию интерфейса свойства для включения дополнительных свойств.</span><span class="sxs-lookup"><span data-stu-id="8b856-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="8b856-143">Во время настройки поставщики должны добавить свои свойства конфигурации в объект, реализующий интерфейс свойства.</span><span class="sxs-lookup"><span data-stu-id="8b856-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="8b856-144">После настройки всех поставщиков мастер профилей добавляет эти свойства в профиль.</span><span class="sxs-lookup"><span data-stu-id="8b856-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="8b856-145">Дополнительные сведения о том, как использовать эту функцию, см в разделе [Поддержка конфигурации службы сообщений](supporting-message-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="8b856-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

