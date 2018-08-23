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
ms.openlocfilehash: 3d78b4e6a4a0cc3363edefc84e7ae80dbe72c510
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590360"
---
# <a name="wizardentry"></a><span data-ttu-id="d61a8-103">WIZARDENTRY</span><span class="sxs-lookup"><span data-stu-id="d61a8-103">WIZARDENTRY</span></span>

  
  
<span data-ttu-id="d61a8-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d61a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d61a8-105">Определяет точку функцию запись службы поставщика, которая вызывает мастер профиля для извлечения достаточно сведений для отображения страницы свойств конфигурации поставщика.</span><span class="sxs-lookup"><span data-stu-id="d61a8-105">Defines a service provider entry point function which the Profile Wizard calls to retrieve enough information to display the provider's configuration property sheets.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d61a8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d61a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="d61a8-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="d61a8-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="d61a8-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="d61a8-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d61a8-109">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d61a8-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="d61a8-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="d61a8-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d61a8-111">Мастер профилей MAPI</span><span class="sxs-lookup"><span data-stu-id="d61a8-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
ULONG WIZARDENTRY(
  HINSTANCE hProviderDLLInstance,
  LPSTR FAR * lpcsResourceName,
  DLGPROC FAR * lppDlgProc,
  LPMAPIPROP lpMAPIProp,
  LPMAPISUPPORTOBJECT lpMapiSupportObject
);
```

## <a name="parameters"></a><span data-ttu-id="d61a8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d61a8-112">Parameters</span></span>

 <span data-ttu-id="d61a8-113">_hProviderDLLInstance_</span><span class="sxs-lookup"><span data-stu-id="d61a8-113">_hProviderDLLInstance_</span></span>
  
> <span data-ttu-id="d61a8-114">[in] Дескриптор экземпляра DLL поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d61a8-114">[in] Instance handle of the service provider's DLL.</span></span> 
    
 <span data-ttu-id="d61a8-115">_lpcsResourceName_</span><span class="sxs-lookup"><span data-stu-id="d61a8-115">_lpcsResourceName_</span></span>
  
> <span data-ttu-id="d61a8-116">[out] Указатель на строку, содержащую полное имя ресурса диалоговое окно, которое должно отображаться в мастере профилей во время настройки.</span><span class="sxs-lookup"><span data-stu-id="d61a8-116">[out] Pointer to a string that contains the full name of the dialog resource that should be displayed by the Profile Wizard during configuration.</span></span> <span data-ttu-id="d61a8-117">Максимальный размер строки, включая символ конца строки составляет 32 символов.</span><span class="sxs-lookup"><span data-stu-id="d61a8-117">The maximum size of the string, including the NULL terminator, is 32 characters.</span></span> 
    
 <span data-ttu-id="d61a8-118">_lppDlgProc_</span><span class="sxs-lookup"><span data-stu-id="d61a8-118">_lppDlgProc_</span></span>
  
> <span data-ttu-id="d61a8-119">[out] Указатель на стандартный Windows процедуру диалогового окна, который будет вызываться мастер профиля для уведомления поставщика различные события.</span><span class="sxs-lookup"><span data-stu-id="d61a8-119">[out] Pointer to a standard Windows dialog box procedure that will be called by the Profile Wizard to notify the provider of various events.</span></span> 
    
 <span data-ttu-id="d61a8-120">_lpMAPIProp_</span><span class="sxs-lookup"><span data-stu-id="d61a8-120">_lpMAPIProp_</span></span>
  
> <span data-ttu-id="d61a8-121">[in] Указатель на реализацию интерфейса свойства, который предоставляет доступ к свойствам конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d61a8-121">[in] Pointer to a property interface implementation that provides access to the configuration properties.</span></span> 
    
 <span data-ttu-id="d61a8-122">_lpMapiSupportObject_</span><span class="sxs-lookup"><span data-stu-id="d61a8-122">_lpMapiSupportObject_</span></span>
  
> <span data-ttu-id="d61a8-123">[in] Указатель на объект поддержки MAPI, которые применяются для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="d61a8-123">[in] Pointer to the MAPI support object applicable to this session.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d61a8-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d61a8-124">Return value</span></span>

<span data-ttu-id="d61a8-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d61a8-125">S_OK</span></span> 
  
> <span data-ttu-id="d61a8-126">Функция поставщика услуг **WIZARDENTRY** вызван успешно.</span><span class="sxs-lookup"><span data-stu-id="d61a8-126">The service provider's **WIZARDENTRY** function was called successfully.</span></span> 
    
<span data-ttu-id="d61a8-127">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="d61a8-127">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="d61a8-128">Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="d61a8-128">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d61a8-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="d61a8-129">Remarks</span></span>

<span data-ttu-id="d61a8-130">Мастер профиля вызывает функцию **WIZARDENTRY** на основе, когда он будет готов для отображения пользовательского интерфейса конфигурации поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="d61a8-130">The Profile Wizard calls the **WIZARDENTRY** based function when it is ready to display the service provider's configuration user interface.</span></span> <span data-ttu-id="d61a8-131">После завершения настройки всех поставщиков мастера профилей, он записывает данные свойства конфигурации профиле путем вызова [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="d61a8-131">When the Profile Wizard is finished configuring all providers, it writes the configuration properties to the profile by calling [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d61a8-132">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d61a8-132">Notes to implementers</span></span>

<span data-ttu-id="d61a8-133">Имя функции **WIZARDENTRY** на основе должны находиться в запись WIZARD_ENTRY_NAME в MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="d61a8-133">The name of the **WIZARDENTRY** based function must be placed in the WIZARD_ENTRY_NAME entry in MAPISVC.INF.</span></span> 
  
<span data-ttu-id="d61a8-134">Имя ресурса является, что ресурса диалогового окна, которое будет отображаться в области мастер профилей.</span><span class="sxs-lookup"><span data-stu-id="d61a8-134">The resource name is that of the dialog resource that will be rendered in the pane of the Profile Wizard.</span></span> <span data-ttu-id="d61a8-135">Ресурс, который передается обратная должны содержать все страницы в одном диалоговом окне ресурса.</span><span class="sxs-lookup"><span data-stu-id="d61a8-135">The resource that is passed back needs to contain all the pages in a single dialog resource.</span></span> <span data-ttu-id="d61a8-136">Когда мастер профиля получает этот ресурс, игнорирует диалоговое окно стиль, но не стилей элементов управления и создает все элементы управления в качестве дочерних элементов страница мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="d61a8-136">When the Profile Wizard receives this resource, it ignores the dialog style, but not the control styles, and creates all the controls as children of the Profile Wizard page.</span></span> <span data-ttu-id="d61a8-137">Все элементы управления изначально являются скрытыми.</span><span class="sxs-lookup"><span data-stu-id="d61a8-137">All controls are initially hidden.</span></span> <span data-ttu-id="d61a8-138">Поставщики следует сделать уверены в том, что координаты для элементов управления нулевой или с отсчетом от нуля и они не превышать Максимальная ширина 200 единиц диалогового окна и максимальная высота 150 единиц диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d61a8-138">Providers should make sure that the coordinates for their controls are zero or zero-based, and that they do not exceed a maximum width of 200 dialog units and a maximum height of 150 dialog units.</span></span> <span data-ttu-id="d61a8-139">Идентификаторы элементов управления под 400 зарезервированы для мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="d61a8-139">Control identifiers below 400 are reserved for the Profile Wizard.</span></span> <span data-ttu-id="d61a8-140">Мастер профиля отображает название поставщика полужирным шрифтом выше поставщика пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d61a8-140">The Profile Wizard displays the provider's title in bold text above the provider's user interface.</span></span> 
  
<span data-ttu-id="d61a8-141">Указатель интерфейса свойство, указанное в параметре _lpMAPIProp_ должны храниться поставщиком для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="d61a8-141">The property interface pointer supplied in the  _lpMAPIProp_ parameter should be retained by the provider for future reference.</span></span> <span data-ttu-id="d61a8-142">Мастер профиля работает с самого базового набора свойств, и поставщик может использовать свойство реализации интерфейса, чтобы включить дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="d61a8-142">The Profile Wizard deals with only the most basic set of properties, and the provider can use the property interface implementation to include additional properties.</span></span> <span data-ttu-id="d61a8-143">Во время настройки поставщики следует добавить объект, реализующий интерфейс свойство их свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d61a8-143">During configuration, providers should add their configuration properties to the object implementing the property interface.</span></span> <span data-ttu-id="d61a8-144">После настройки всех поставщиков профилей мастер добавляет эти свойства профиля.</span><span class="sxs-lookup"><span data-stu-id="d61a8-144">After all providers have been configured, the Profile Wizard adds these properties to the profile.</span></span> 
  
<span data-ttu-id="d61a8-145">Дополнительные сведения об использовании этой функции [Поддержки конфигурации службы сообщений](supporting-message-service-configuration.md)см.</span><span class="sxs-lookup"><span data-stu-id="d61a8-145">For more information about how to use this function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md).</span></span> 
  

