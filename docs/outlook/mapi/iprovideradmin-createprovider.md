---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430807"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="6b6e7-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="6b6e7-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="6b6e7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b6e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b6e7-105">Добавляет поставщика услуг в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-105">Adds a service provider to the message service.</span></span> 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a><span data-ttu-id="6b6e7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6b6e7-106">Parameters</span></span>

 <span data-ttu-id="6b6e7-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="6b6e7-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="6b6e7-108">[in] Указатель на имя поставщика для добавления.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="6b6e7-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="6b6e7-109">_cValues_</span></span>
  
> <span data-ttu-id="6b6e7-110">[in] Количество значений свойств, на которые указывает параметр _lpProps._</span><span class="sxs-lookup"><span data-stu-id="6b6e7-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="6b6e7-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="6b6e7-111">_lpProps_</span></span>
  
> <span data-ttu-id="6b6e7-112">[in] Указатель на массив значений свойств, описывая свойства, которые должен добавить поставщик.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="6b6e7-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6b6e7-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6b6e7-114">[in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="6b6e7-115">Параметр _ulUIParam_ используется, если флаг MAPI_DIALOG в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6b6e7-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6b6e7-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b6e7-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6b6e7-117">[in] Битмаска флагов, которые контролируют добавление поставщика.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="6b6e7-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6b6e7-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="6b6e7-119">MAPI_DIALOG: отображает диалоговое окно для запроса сведений о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="6b6e7-120">MAPI_UNICODE. Свойства имени и строки поставщика находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="6b6e7-121">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="6b6e7-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="6b6e7-122">_lpUID_</span></span>
  
> <span data-ttu-id="6b6e7-123">[вышел] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор, который представляет поставщика для добавления.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b6e7-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b6e7-124">Return value</span></span>

<span data-ttu-id="6b6e7-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b6e7-125">S_OK</span></span> 
  
> <span data-ttu-id="6b6e7-126">Поставщик успешно добавлен в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="6b6e7-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6b6e7-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6b6e7-128">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b6e7-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b6e7-129">Remarks</span></span>

<span data-ttu-id="6b6e7-130">Метод **IProviderAdmin::CreateProvider** добавляет поставщика услуг в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="6b6e7-131">Параметр  _lpszProvider должен_ указать имя поставщика, который принадлежит службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="6b6e7-132">**CreateProvider** не проверяет, соответствует ли имя поставщика в службе; если переданное имя не совпадает с именем службы, вызов удался, но результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="6b6e7-133">Большинство служб сообщений не позволяют добавлять или удалять поставщиков во время использования профиля.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="6b6e7-134">После того как в профиль из файла Mapisvc.inf были добавлены все доступные сведения о поставщике услуг, **CreateProvider** вызывает функцию точки входа службы сообщений с параметром  _ulContext,_ заданным MSG_SERVICE_PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="6b6e7-135">Если MAPI_DIALOG задан в параметре _ulFlags_ метода **CreateProvider,** значения _ulUIParam_ и _ulFlags_ также передаются функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="6b6e7-136">Эти дополнительные параметры позволяют поставщику услуг отображать свой лист свойств, чтобы пользователь может ввести параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6b6e7-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b6e7-137">См. также</span><span class="sxs-lookup"><span data-stu-id="6b6e7-137">See also</span></span>

- [<span data-ttu-id="6b6e7-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6b6e7-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="6b6e7-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="6b6e7-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="6b6e7-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="6b6e7-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="6b6e7-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b6e7-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

