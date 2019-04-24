---
title: Ипровидерадминкреатепровидер
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279558"
---
# <a name="iprovideradmincreateprovider"></a><span data-ttu-id="99b1b-103">IProviderAdmin::CreateProvider</span><span class="sxs-lookup"><span data-stu-id="99b1b-103">IProviderAdmin::CreateProvider</span></span>

<span data-ttu-id="99b1b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99b1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99b1b-105">Добавляет поставщика услуг в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="99b1b-105">Adds a service provider to the message service.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="99b1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99b1b-106">Parameters</span></span>

 <span data-ttu-id="99b1b-107">_Лпсзпровидер_</span><span class="sxs-lookup"><span data-stu-id="99b1b-107">_lpszProvider_</span></span>
  
> <span data-ttu-id="99b1b-108">возврата Указатель имени добавляемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="99b1b-108">[in] A pointer to the name of the provider to add.</span></span>
    
 <span data-ttu-id="99b1b-109">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="99b1b-109">_cValues_</span></span>
  
> <span data-ttu-id="99b1b-110">возврата Количество значений свойств, на которые указывает параметр _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="99b1b-110">[in] The count of property values pointed to by the  _lpProps_ parameter.</span></span> 
    
 <span data-ttu-id="99b1b-111">_Лппропс_</span><span class="sxs-lookup"><span data-stu-id="99b1b-111">_lpProps_</span></span>
  
> <span data-ttu-id="99b1b-112">возврата Указатель на массив значений свойств, описывающий свойства поставщика, который требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="99b1b-112">[in] A pointer to a property value array that describes the properties of the provider to add.</span></span>
    
 <span data-ttu-id="99b1b-113">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="99b1b-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="99b1b-114">возврата Дескриптор родительского окна любых диалоговых окон или окон, которые отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="99b1b-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="99b1b-115">Параметр _улуипарам_ используется, если установлен флаг мапи_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="99b1b-115">The  _ulUIParam_ parameter is used if the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="99b1b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99b1b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="99b1b-117">возврата Битовая маска флагов, управляющих добавлением поставщика.</span><span class="sxs-lookup"><span data-stu-id="99b1b-117">[in] A bitmask of flags that controls the provider addition.</span></span> <span data-ttu-id="99b1b-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="99b1b-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="99b1b-119">МАПИ_ДИАЛОГ: отображает диалоговое окно, в котором запрашиваются сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="99b1b-119">MAPI_DIALOG: Displays a dialog box to prompt for configuration information.</span></span>
      
  - <span data-ttu-id="99b1b-120">МАПИ_УНИКОДЕ: имя поставщика и строковые свойства имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="99b1b-120">MAPI_UNICODE: The provider name and string properties are in Unicode format.</span></span> <span data-ttu-id="99b1b-121">Если флаг МАПИ_УНИКОДЕ не установлен, эти строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="99b1b-121">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="99b1b-122">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="99b1b-122">_lpUID_</span></span>
  
> <span data-ttu-id="99b1b-123">вышли Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор, представляющий поставщика, которого требуется добавить.</span><span class="sxs-lookup"><span data-stu-id="99b1b-123">[out] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier that represents the provider to add.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="99b1b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99b1b-124">Return value</span></span>

<span data-ttu-id="99b1b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="99b1b-125">S_OK</span></span> 
  
> <span data-ttu-id="99b1b-126">Поставщик успешно добавлен в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="99b1b-126">The provider was successfully added to the message service.</span></span>
    
<span data-ttu-id="99b1b-127">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="99b1b-127">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="99b1b-128">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="99b1b-128">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="99b1b-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="99b1b-129">Remarks</span></span>

<span data-ttu-id="99b1b-130">Метод **ипровидерадмин:: креатепровидер** добавляет поставщика услуг в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="99b1b-130">The **IProviderAdmin::CreateProvider** method adds a service provider to the message service.</span></span> <span data-ttu-id="99b1b-131">Параметр _лпсзпровидер_ должен указать имя поставщика, который принадлежит службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="99b1b-131">The  _lpszProvider_ parameter must point to the name of a provider that belongs to the message service.</span></span> <span data-ttu-id="99b1b-132">**Креатепровидер** не проверяет, совпадает ли имя с именем поставщика в службе; Если переданное имя не отвечает имени службы, вызов завершается успешно, но результаты непредсказуемы.</span><span class="sxs-lookup"><span data-stu-id="99b1b-132">**CreateProvider** does not verify whether the name matches the name of a provider in the service; if the passed name does not match a service name, the call succeeds, but the results are unpredictable.</span></span> <span data-ttu-id="99b1b-133">Большинство служб сообщений не допускают Добавление или удаление поставщиков при использовании профиля.</span><span class="sxs-lookup"><span data-stu-id="99b1b-133">Most message services do not allow providers to be added or deleted while the profile is in use.</span></span> 
  
<span data-ttu-id="99b1b-134">После того как все доступные сведения о поставщике услуг добавлены в профиль из файла Mapisvc. INF, **креатепровидер** вызывает функцию точки входа службы сообщений с параметром _улконтекст_ , равным мсг_сервице_ ПРОВИДЕР_КРЕАТЕ.</span><span class="sxs-lookup"><span data-stu-id="99b1b-134">After all of the available information about the service provider has been added to the profile from the Mapisvc.inf file, **CreateProvider** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_PROVIDER_CREATE.</span></span> <span data-ttu-id="99b1b-135">Если МАПИ_ДИАЛОГ задано в параметре _ulFlags_ метода **креатепровидер** , значения в параметрах _улуипарам_ и _ulFlags_ также передаются в функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="99b1b-135">If MAPI_DIALOG is set in the **CreateProvider** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed to the entry point function.</span></span> <span data-ttu-id="99b1b-136">Эти дополнительные параметры позволяют поставщику услуг отображать свой лист свойств, чтобы пользователь мог вводить параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="99b1b-136">These additional parameters enable the service provider to display its property sheet so the user can enter configuration settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99b1b-137">См. также</span><span class="sxs-lookup"><span data-stu-id="99b1b-137">See also</span></span>

- [<span data-ttu-id="99b1b-138">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="99b1b-138">MAPIUID</span></span>](mapiuid.md)  
- [<span data-ttu-id="99b1b-139">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="99b1b-139">MSGSERVICEENTRY</span></span>](msgserviceentry.md)  
- [<span data-ttu-id="99b1b-140">SPropValue</span><span class="sxs-lookup"><span data-stu-id="99b1b-140">SPropValue</span></span>](spropvalue.md)  
- [<span data-ttu-id="99b1b-141">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99b1b-141">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

