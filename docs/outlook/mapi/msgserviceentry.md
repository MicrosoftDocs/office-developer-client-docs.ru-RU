---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427880"
---
# <a name="msgserviceentry"></a><span data-ttu-id="f33da-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="f33da-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="f33da-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f33da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f33da-105">Определяет прототип функции точки входа службы сообщений для поддержки конфигурации службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f33da-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f33da-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f33da-106">Header file:</span></span>  <br/> |<span data-ttu-id="f33da-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="f33da-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="f33da-108">Определенные функции, реализованные в:</span><span class="sxs-lookup"><span data-stu-id="f33da-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="f33da-109">Службы сообщений</span><span class="sxs-lookup"><span data-stu-id="f33da-109">Message services</span></span>  <br/> |
|<span data-ttu-id="f33da-110">Определенная функция, вызванная:</span><span class="sxs-lookup"><span data-stu-id="f33da-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="f33da-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="f33da-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="f33da-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f33da-112">Parameters</span></span>

 <span data-ttu-id="f33da-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="f33da-113">_hInstance_</span></span>
  
> <span data-ttu-id="f33da-114">[in] Ручка экземпляра поставщика услугDLL.</span><span class="sxs-lookup"><span data-stu-id="f33da-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="f33da-115">Ручка обычно используется для получения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f33da-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="f33da-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="f33da-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="f33da-117">[in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE **IMalloc.**</span><span class="sxs-lookup"><span data-stu-id="f33da-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="f33da-118">Службе сообщений может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.**</span><span class="sxs-lookup"><span data-stu-id="f33da-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="f33da-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="f33da-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="f33da-120">[in] Указатель на [реализацию интерфейса IMAPISupport: IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f33da-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="f33da-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f33da-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="f33da-122">[in] Значение, определенное для реализации, используемого для передачи сведений об интерфейсе пользователя в функцию или ноль.</span><span class="sxs-lookup"><span data-stu-id="f33da-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="f33da-123">Параметр  _ulUIParam_ является родительской ручкой окна для диалогового окна конфигурации и имеет тип HWND (отлит в ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="f33da-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="f33da-124">Значение нуля указывает на отсутствие родительского окна.</span><span class="sxs-lookup"><span data-stu-id="f33da-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="f33da-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f33da-125">_ulFlags_</span></span>
  
> <span data-ttu-id="f33da-126">[in] Bitmask флагов с указанием параметров для функции входа в службу.</span><span class="sxs-lookup"><span data-stu-id="f33da-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="f33da-127">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f33da-127">The following flags can be set:</span></span>
    
<span data-ttu-id="f33da-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f33da-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f33da-129">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="f33da-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f33da-130">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f33da-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="f33da-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="f33da-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="f33da-132">Пользовательский интерфейс конфигурации службы должен отображать текущую конфигурацию, но не позволять пользователю изменять ее.</span><span class="sxs-lookup"><span data-stu-id="f33da-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="f33da-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="f33da-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="f33da-134">Позволяет отображать диалоговое окно конфигурации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f33da-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="f33da-135">Когда заданная SERVICE_UI_ALLOWED, диалоговое окно должно отображаться только в том случае, если массив свойств  _lpProps_ пуст или не содержит допустимую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f33da-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="f33da-136">Если SERVICE_UI_ALLOWED не установлено, диалоговое окно может по-прежнему отображаться, если SERVICE_UI_ALWAYS установлен флаг.</span><span class="sxs-lookup"><span data-stu-id="f33da-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="f33da-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="f33da-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="f33da-138">Запросы, чтобы диалоговое окно конфигурации для активного поставщика отображалось поверх других диалоговых полей.</span><span class="sxs-lookup"><span data-stu-id="f33da-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="f33da-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="f33da-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="f33da-140">Требуется, чтобы служба сообщений отображала диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f33da-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="f33da-141">Если флаг SERVICE_UI_ALWAYS не установлен, диалоговое окно конфигурации может по-прежнему отображаться, если флаг SERVICE_UI_ALLOWED установлен и допустимые сведения о конфигурации недоступны из массива значений _свойства lpProps._</span><span class="sxs-lookup"><span data-stu-id="f33da-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="f33da-142">Необходимо SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS, чтобы разрешить отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f33da-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="f33da-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="f33da-143">_ulContext_</span></span>
  
> <span data-ttu-id="f33da-144">[in] Операция конфигурации, которую в настоящее время выполняет MAPI.</span><span class="sxs-lookup"><span data-stu-id="f33da-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="f33da-145">Параметр  _ulContext будет_ содержать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f33da-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="f33da-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="f33da-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="f33da-147">Изменения в конфигурации службы должны быть внесены в профиле.</span><span class="sxs-lookup"><span data-stu-id="f33da-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="f33da-148">Если флаг SERVICE_UI_ALWAYS установлен, служба должна отобразить диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f33da-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="f33da-149">Диалоговое окно также должно отображаться, если флаг SERVICE_UI_ALLOWED установлен, а параметр  _lpProps_ пуст или не содержит допустимые данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f33da-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="f33da-150">Если  _lpProps содержит_ допустимые данные, диалоговое окно не должно отображаться, и служба должна использовать эти данные для изменения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f33da-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="f33da-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="f33da-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="f33da-152">Служба добавляется в профиль.</span><span class="sxs-lookup"><span data-stu-id="f33da-152">The service is being added to a profile.</span></span> <span data-ttu-id="f33da-153">Если заданная SERVICE_UI_ALWAYS или SERVICE_UI_ALLOWED, служба должна отображать диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f33da-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="f33da-154">Если ни один флаг не установлен, служба должна сбой.</span><span class="sxs-lookup"><span data-stu-id="f33da-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="f33da-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="f33da-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="f33da-156">Служба удаляется из профиля.</span><span class="sxs-lookup"><span data-stu-id="f33da-156">The service is being removed from a profile.</span></span> <span data-ttu-id="f33da-157">После получения этого события служба должна вернуться S_OK.</span><span class="sxs-lookup"><span data-stu-id="f33da-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="f33da-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="f33da-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="f33da-159">Служба установлена на рабочей станции пользователя с сетевого, дискетного диска или другого внешнего носителя.</span><span class="sxs-lookup"><span data-stu-id="f33da-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="f33da-160">После получения этого события служба обычно возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="f33da-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="f33da-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="f33da-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="f33da-162">Запросы на создание службой дополнительного экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="f33da-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="f33da-163">Если служба поддерживает эту операцию, она должна вызвать [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="f33da-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="f33da-164">Если служба не поддерживает эту операцию, она может MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f33da-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="f33da-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="f33da-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="f33da-166">Запрашивает, чтобы служба удалила экземпляр поставщика.</span><span class="sxs-lookup"><span data-stu-id="f33da-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="f33da-167">Если служба поддерживает эту операцию, она должна вызвать [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="f33da-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="f33da-168">Если служба не поддерживает эту операцию, она может MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="f33da-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="f33da-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="f33da-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="f33da-170">Служба удаляется.</span><span class="sxs-lookup"><span data-stu-id="f33da-170">The service is being removed.</span></span> <span data-ttu-id="f33da-171">После получения этого события служба может выполнять любые задачи очистки, которые должны выполняться до окончания службы, а затем возвращаются со значением успешности.</span><span class="sxs-lookup"><span data-stu-id="f33da-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="f33da-172">Если пользователь отменяет удаление, служба должна MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="f33da-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="f33da-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="f33da-173">_cValues_</span></span>
  
> <span data-ttu-id="f33da-174">[in] Количество значений свойств в массиве, на который указывает _параметр lpProps._</span><span class="sxs-lookup"><span data-stu-id="f33da-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="f33da-175">Значение параметра  _cValues_ нулевое, если MAPI не передает значения свойств.</span><span class="sxs-lookup"><span data-stu-id="f33da-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="f33da-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="f33da-176">_lpProps_</span></span>
  
> <span data-ttu-id="f33da-177">[in] Указатель на необязательный массив [структур SPropValue,](spropvalue.md) указывающий значения для свойств, поддерживаемых поставщиком, которые функция будет использовать при настройке службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f33da-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="f33da-178">Функция использует этот параметр только в том случае, если параметр  _ulContext_ задан для MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="f33da-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="f33da-179">Этот параметр обычно используется для того, чтобы передать путь к файлу для службы на основе файлов, например службы личной книги адресов.</span><span class="sxs-lookup"><span data-stu-id="f33da-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="f33da-180">Если флаг MSG_SERVICE_CONFIGURE не передается в  _параметре ulFlags,_ параметр  _lpProps_ должен быть нулем.</span><span class="sxs-lookup"><span data-stu-id="f33da-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="f33da-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="f33da-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="f33da-182">[in] Указатель на [интерфейс IProviderAdmin:IUnknown,](iprovideradminiunknown.md) который функция может использовать для поиска разделов профилей для конкретного поставщика в текущей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="f33da-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="f33da-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="f33da-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="f33da-184">[вышел] Указатель на [структуру MAPIERROR.](mapierror.md)</span><span class="sxs-lookup"><span data-stu-id="f33da-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="f33da-185">Структура выделяется функцией [MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="f33da-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="f33da-186">Все члены являются необязательными, хотя большинство структур будет содержать допустимую строку сообщения об ошибке в _члене lpszError._</span><span class="sxs-lookup"><span data-stu-id="f33da-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="f33da-187">Если  _члены структуры lpszComponent_ или  _lpszError_ присутствуют, их память в конечном итоге должна быть освобождена одним вызовом [в MAPIFreeBuffer](mapifreebuffer.md) в базовой структуре.</span><span class="sxs-lookup"><span data-stu-id="f33da-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f33da-188">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f33da-188">Return value</span></span>

<span data-ttu-id="f33da-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="f33da-189">S_OK</span></span> 
  
> <span data-ttu-id="f33da-190">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f33da-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f33da-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="f33da-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="f33da-192">Поставщик услуг не настроен.</span><span class="sxs-lookup"><span data-stu-id="f33da-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="f33da-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f33da-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f33da-194">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f33da-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="f33da-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f33da-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f33da-196">Поставщик либо не поддерживает изменения в своих объектах, либо не поддерживает уведомление об изменениях.</span><span class="sxs-lookup"><span data-stu-id="f33da-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="f33da-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f33da-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f33da-198">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="f33da-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f33da-199">Примечания</span><span class="sxs-lookup"><span data-stu-id="f33da-199">Remarks</span></span>

<span data-ttu-id="f33da-200">Функция, определяемая с помощью прототипа функции **MSGSERVICEENTRY,** позволяет службам сообщений настраивать себя или выполнять другие действия, определенные для служб.</span><span class="sxs-lookup"><span data-stu-id="f33da-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="f33da-201">Функция в основном обставлена диалоговое окно, в котором пользователь может изменять параметры, определенные службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="f33da-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="f33da-202">Он также может поддерживать программную конфигурацию с помощью массива значений свойств, переданного в _параметре lpProps._</span><span class="sxs-lookup"><span data-stu-id="f33da-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="f33da-203">Программная конфигурация необязательна, если служба не поддерживает мастер профилей, для которого это необходимо.</span><span class="sxs-lookup"><span data-stu-id="f33da-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="f33da-204">MAPI вызывает эту точку входа из приложения Панели управления или в ответ на клиентскую заявку, вызываемую [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) или [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="f33da-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="f33da-205">MAPI не ставит никаких ограничений на имя функции, которое служба сообщений использует для прототипа **MSGSERVICEENTRY,** но предпочитает имя **ServiceEntry.**</span><span class="sxs-lookup"><span data-stu-id="f33da-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="f33da-206">Существует никаких ограничений на ordinal для функции, и один поставщик DLL может содержать несколько функций.</span><span class="sxs-lookup"><span data-stu-id="f33da-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="f33da-207">Однако только одна из функций может быть названа **ServiceEntry**.</span><span class="sxs-lookup"><span data-stu-id="f33da-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="f33da-208">Служба сообщений может использовать функцию [BuildDisplayTable](builddisplaytable.md) и [метод IMAPISupport::D ConfigPropsheet](imapisupport-doconfigpropsheet.md) для упрощения реализации диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f33da-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="f33da-209">Пользователь может отменить операцию MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="f33da-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="f33da-210">В этом случае функции **ServiceEntry** следует проверить у пользователя, чтобы убедиться, что служба не должна быть удалена и MAPI_E_USER_CANCEL, если служба остается установленной.</span><span class="sxs-lookup"><span data-stu-id="f33da-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="f33da-211">Функция, основанная на прототипе **MSGSERVICEENTRY,** возвращает одно из перечисленных значений HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f33da-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="f33da-212">MAPI передает это значение при ответе на вызов клиента [в IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="f33da-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="f33da-213">Службы сообщений, которые экспортируют функцию входа **в службу,** должны включать свойства PR_SERVICE_DLL_NAME [(PidTagServiceDllName)](pidtagservicedllname-canonical-property.md)и **PR_SERVICE_ENTRY_NAME** [(PidTagServiceEntryName)](pidtagserviceentryname-canonical-property.md)в разделе служба сообщений MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="f33da-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

