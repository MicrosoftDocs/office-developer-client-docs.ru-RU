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
ms.openlocfilehash: 01cc8a8a54137b72091abab3671c08b526ef9e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809549"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="05989-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="05989-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="05989-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05989-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05989-105">Добавление поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="05989-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="05989-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="05989-106">Parameters</span></span>

 <span data-ttu-id="05989-107">_lpszProvider_</span><span class="sxs-lookup"><span data-stu-id="05989-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="05989-108">[in] Указатель на имя поставщика для добавления.</span><span class="sxs-lookup"><span data-stu-id="05989-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="05989-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="05989-109">_cValues_</span></span>
  
> <span data-ttu-id="05989-110">[in] Количество значений свойств, на который указывает параметр _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="05989-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="05989-111">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="05989-111">_lpProps_</span></span>
  
> <span data-ttu-id="05989-112">[in] Указатель на массив значений свойств, с описанием свойства поставщика для добавления.</span><span class="sxs-lookup"><span data-stu-id="05989-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="05989-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="05989-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="05989-114">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="05989-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="05989-115">Если флаг MAPI_DIALOG установлен в параметре _ulFlags_ используется параметр _ulUIParam_ .</span><span class="sxs-lookup"><span data-stu-id="05989-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="05989-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="05989-116">_ulFlags_</span></span>
  
> <span data-ttu-id="05989-117">[in] Битовая маска флаги, который управляет добавлением поставщика.</span><span class="sxs-lookup"><span data-stu-id="05989-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="05989-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="05989-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="05989-119">MAPI_DIALOG: Отображает диалоговое окно для запроса сведений о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="05989-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="05989-120">MAPI_UNICODE: Свойства name и строка поставщика, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="05989-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="05989-121">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="05989-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="05989-122">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="05989-122">_lpUID_</span></span>
  
> <span data-ttu-id="05989-123">[out] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор, представляющий поставщика для добавления.</span><span class="sxs-lookup"><span data-stu-id="05989-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="05989-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="05989-124">Return value</span></span>

<span data-ttu-id="05989-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="05989-125">S_OK</span></span> 
  
> <span data-ttu-id="05989-126">Поставщик был успешно добавлена в службу сообщения.</span><span class="sxs-lookup"><span data-stu-id="05989-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="05989-127">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="05989-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="05989-128">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="05989-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="05989-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="05989-129">Remarks</span></span>

<span data-ttu-id="05989-130">Метод **IProviderAdmin::CreateProvider** добавляет поставщика услуг службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="05989-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="05989-131">Параметр _lpszProvider_ должен указывать имя поставщика, к которой принадлежит служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="05989-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="05989-132">**CreateProvider** не проверяет, соответствует ли имя имя поставщика в службе; Если переданный имя не соответствует имени службы, вызов выполняется успешно, но результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="05989-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="05989-133">Большинство служб сообщения не разрешать поставщиков добавить или удалить профиль во время работы.</span><span class="sxs-lookup"><span data-stu-id="05989-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="05989-134">Когда все доступные сведения о службе поставщика был добавлен к профилю из файла Mapisvc.inf **CreateProvider** вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , задайте значение MSG_SERVICE_ PROVIDER_CREATE.</span><span class="sxs-lookup"><span data-stu-id="05989-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="05989-135">Если в параметре метода **CreateProvider** _ulFlags_ MAPI_DIALOG, значения в параметрах _ulUIParam_ и _ulFlags_ также передаются в функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="05989-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="05989-136">Эти дополнительные параметры включения поставщика услуг открыть окно свойств, поэтому пользователь может ввести параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="05989-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="05989-137">См. также</span><span class="sxs-lookup"><span data-stu-id="05989-137">See also</span></span>

- [<span data-ttu-id="05989-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="05989-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="05989-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="05989-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="05989-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="05989-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="05989-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05989-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

