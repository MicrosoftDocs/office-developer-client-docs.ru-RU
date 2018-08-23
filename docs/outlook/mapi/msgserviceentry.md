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
ms.openlocfilehash: 954609cbc62039c0d60874bde83fde50d1d11c30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591669"
---
# <a name="msgserviceentry"></a><span data-ttu-id="0fbff-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="0fbff-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="0fbff-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fbff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fbff-105">Определяет прототип для сообщений службы функцию точки входа для поддержки конфигурации службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0fbff-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0fbff-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0fbff-106">Header file:</span></span>  <br/> |<span data-ttu-id="0fbff-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="0fbff-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="0fbff-108">Функция реализован:</span><span class="sxs-lookup"><span data-stu-id="0fbff-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="0fbff-109">Службы сообщений</span><span class="sxs-lookup"><span data-stu-id="0fbff-109">Message services</span></span>  <br/> |
|<span data-ttu-id="0fbff-110">Вызывается функция:</span><span class="sxs-lookup"><span data-stu-id="0fbff-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="0fbff-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0fbff-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0fbff-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fbff-112">Parameters</span></span>

 <span data-ttu-id="0fbff-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="0fbff-113">_hInstance_</span></span>
  
> <span data-ttu-id="0fbff-114">[in] Дескриптор экземпляра службы providerDLL.</span><span class="sxs-lookup"><span data-stu-id="0fbff-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="0fbff-115">Дескриптор обычно используется для извлечения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fbff-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="0fbff-116">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="0fbff-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="0fbff-117">[in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="0fbff-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="0fbff-118">Служба сообщений может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**.</span><span class="sxs-lookup"><span data-stu-id="0fbff-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="0fbff-119">_lpMAPISup_</span><span class="sxs-lookup"><span data-stu-id="0fbff-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="0fbff-120">[in] Указатель на [IMAPISupport: IUnknown](imapisupportiunknown.md) реализация интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0fbff-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="0fbff-121">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0fbff-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="0fbff-122">[in] От реализации значение, используемое для передачи в функцию или ноль, сведения о пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="0fbff-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="0fbff-123">Параметр _ulUIParam_ является дескриптор родительского окна для диалогового окна конфигурации и типа HWND (приведения к ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="0fbff-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="0fbff-124">Нулевое значение указывает, что нет родительского окна.</span><span class="sxs-lookup"><span data-stu-id="0fbff-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="0fbff-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0fbff-125">_ulFlags_</span></span>
  
> <span data-ttu-id="0fbff-126">[in] Битовая маска, указывающее параметры для функции входа службы флагов.</span><span class="sxs-lookup"><span data-stu-id="0fbff-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="0fbff-127">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="0fbff-127">The following flags can be set:</span></span>
    
<span data-ttu-id="0fbff-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0fbff-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0fbff-129">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="0fbff-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0fbff-130">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0fbff-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="0fbff-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="0fbff-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="0fbff-132">Пользовательский интерфейс конфигурации службы должны отображаться текущей конфигурации, но не разрешать пользователям изменять его.</span><span class="sxs-lookup"><span data-stu-id="0fbff-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="0fbff-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="0fbff-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="0fbff-134">Разрешает диалоговое окно настройки будет отображаться, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="0fbff-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="0fbff-135">Если для флага SERVICE_UI_ALLOWED, диалоговое окно должно отображаться только в том случае, если массива значение свойства _lpProps_ пуст или не содержит допустимое конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0fbff-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="0fbff-136">Если SERVICE_UI_ALLOWED не установлен, диалоговое окно может по-прежнему отображается, если установлен флаг SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="0fbff-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="0fbff-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="0fbff-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="0fbff-138">Запросы, что диалоговое окно конфигурации для поставщика active Directory отображаться поверх других диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="0fbff-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="0fbff-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="0fbff-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="0fbff-140">Требуется служба сообщений для отображения диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0fbff-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="0fbff-141">Если флаг SERVICE_UI_ALWAYS не установлен, диалоговое окно настройки может по-прежнему отображается, если установлен флаг SERVICE_UI_ALLOWED и сведений о конфигурации допустимый недоступен из массива значение свойства _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="0fbff-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="0fbff-142">SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS должен иметь значение Разрешить пользовательского интерфейса для отображения.</span><span class="sxs-lookup"><span data-stu-id="0fbff-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="0fbff-143">_ulContext_</span><span class="sxs-lookup"><span data-stu-id="0fbff-143">_ulContext_</span></span>
  
> <span data-ttu-id="0fbff-144">[in] Операция конфигурации, в настоящее время выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="0fbff-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="0fbff-145">Параметр _ulContext_ будет содержать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0fbff-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="0fbff-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="0fbff-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="0fbff-147">Изменения в конфигурацию службы должны выполняться в профиле.</span><span class="sxs-lookup"><span data-stu-id="0fbff-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="0fbff-148">Если значение флага SERVICE_UI_ALWAYS, службы должны отображать диалоговое окно ее настройки.</span><span class="sxs-lookup"><span data-stu-id="0fbff-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="0fbff-149">Диалоговое окно также должно отображаться, если установлен флаг SERVICE_UI_ALLOWED и параметр _lpProps_ пуст или не содержит данных недопустимой конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="0fbff-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="0fbff-150">Если _lpProps_ содержит допустимых данных, диалоговое окно не должно отображаться и службы следует использовать эти данные для внесения изменений конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0fbff-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="0fbff-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="0fbff-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="0fbff-152">Службы добавляется в профиль.</span><span class="sxs-lookup"><span data-stu-id="0fbff-152">The service is being added to a profile.</span></span> <span data-ttu-id="0fbff-153">Если установлен параметр SERVICE_UI_ALWAYS или SERVICE_UI_ALLOWED флаг службы должны отображать диалоговое окно ее настройки.</span><span class="sxs-lookup"><span data-stu-id="0fbff-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="0fbff-154">Если ни один из флаг установлен, следует не удается службу.</span><span class="sxs-lookup"><span data-stu-id="0fbff-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="0fbff-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="0fbff-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="0fbff-156">Служба удаляется из профиля.</span><span class="sxs-lookup"><span data-stu-id="0fbff-156">The service is being removed from a profile.</span></span> <span data-ttu-id="0fbff-157">После получения это событие, службу должен возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="0fbff-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="0fbff-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="0fbff-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="0fbff-159">Служба установлена на рабочей станции пользователя из сети, гибкий диск или другой внешний носитель.</span><span class="sxs-lookup"><span data-stu-id="0fbff-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="0fbff-160">После получения это событие, служба обычно возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="0fbff-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="0fbff-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="0fbff-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="0fbff-162">Запрашивает создание дополнительного экземпляра поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="0fbff-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="0fbff-163">Если служба поддерживает эту операцию, он должен вызвать [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="0fbff-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="0fbff-164">Если служба не поддерживает эту операцию, он может вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0fbff-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="0fbff-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="0fbff-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="0fbff-166">Запросы на том, что служба удаляет экземпляр поставщика.</span><span class="sxs-lookup"><span data-stu-id="0fbff-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="0fbff-167">Если служба поддерживает эту операцию, он должен вызвать [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="0fbff-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="0fbff-168">Если служба не поддерживает эту операцию, он может вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="0fbff-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="0fbff-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="0fbff-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="0fbff-170">Служба удалена.</span><span class="sxs-lookup"><span data-stu-id="0fbff-170">The service is being removed.</span></span> <span data-ttu-id="0fbff-171">После получения это событие, служба может выполнять все задачи очистки, которые необходимо выполнить до службы заканчивается и затем возвращает значение success.</span><span class="sxs-lookup"><span data-stu-id="0fbff-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="0fbff-172">Если пользователь отменил удаления, служба должна вернуть MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="0fbff-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="0fbff-173">_cValues_</span><span class="sxs-lookup"><span data-stu-id="0fbff-173">_cValues_</span></span>
  
> <span data-ttu-id="0fbff-174">[in] Число значений свойств в массиве указывает параметр _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="0fbff-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="0fbff-175">Значение параметра _cValues_ равно нулю, если передает без значений свойств MAPI.</span><span class="sxs-lookup"><span data-stu-id="0fbff-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="0fbff-176">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="0fbff-176">_lpProps_</span></span>
  
> <span data-ttu-id="0fbff-177">[in] Указатель на необязательный массив [SPropValue](spropvalue.md) структуры, указывающее значения свойств, поддерживаемых поставщиком, которые будут использовать функцию во время настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0fbff-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="0fbff-178">Функция использует этот параметр только в том случае, если параметр _ulContext_ имеет значение MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="0fbff-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="0fbff-179">Этот параметр обычно используется для передачи путь к файлу для службы на основе файла, например из службы адресной книги.</span><span class="sxs-lookup"><span data-stu-id="0fbff-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="0fbff-180">Если флаг MSG_SERVICE_CONFIGURE не передается в параметре _ulFlags_ , параметр _lpProps_ должен быть нулю.</span><span class="sxs-lookup"><span data-stu-id="0fbff-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="0fbff-181">_lpProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="0fbff-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="0fbff-182">[in] Указатель на интерфейс [IProviderAdmin:IUnknown](iprovideradminiunknown.md) , можно использовать функцию для поиска разделов профиля для определенного поставщика в текущей службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="0fbff-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="0fbff-183">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="0fbff-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="0fbff-184">[out] Указатель на структуру [MAPIERROR](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="0fbff-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="0fbff-185">Структура выделяется с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0fbff-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="0fbff-186">Все элементы являются необязательными, несмотря на то, что большинство структур будет содержать строку сообщения допустимый ошибка _lpszError_ участника.</span><span class="sxs-lookup"><span data-stu-id="0fbff-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="0fbff-187">Если присутствуют _lpszComponent_ или _lpszError_ элементы структуры, их памяти в конечном счете освобождения с помощью одного вызова [MAPIFreeBuffer](mapifreebuffer.md) на базовую структуру.</span><span class="sxs-lookup"><span data-stu-id="0fbff-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0fbff-188">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="0fbff-188">Return value</span></span>

<span data-ttu-id="0fbff-189">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="0fbff-189">S_OK</span></span> 
  
> <span data-ttu-id="0fbff-190">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0fbff-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0fbff-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="0fbff-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="0fbff-192">Поставщик услуг не был настроен.</span><span class="sxs-lookup"><span data-stu-id="0fbff-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="0fbff-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0fbff-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0fbff-194">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0fbff-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="0fbff-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0fbff-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0fbff-196">Поставщик не поддерживает изменения в объекты или не поддерживает уведомление об изменениях.</span><span class="sxs-lookup"><span data-stu-id="0fbff-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="0fbff-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0fbff-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0fbff-198">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0fbff-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0fbff-199">Замечания</span><span class="sxs-lookup"><span data-stu-id="0fbff-199">Remarks</span></span>

<span data-ttu-id="0fbff-200">Функция, которая определена с помощью прототипа функции **MSGSERVICEENTRY** включает сообщения службы для настройки сами или выполнить другие действия, зависящие от службы.</span><span class="sxs-lookup"><span data-stu-id="0fbff-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="0fbff-201">Функции в основном предоставляющей диалоговое окно, в котором пользователь может изменить параметры, относящиеся к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="0fbff-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="0fbff-202">Он также может поддерживать программной конфигурации с помощью массива значение свойства, переданной в параметре _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="0fbff-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="0fbff-203">Программная конфигурация является необязательным, если служба не поддерживает мастер профиля, для которого является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0fbff-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="0fbff-204">MAPI вызывает эта точка входа из приложения панели управления или в ответ на вызов [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) или [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="0fbff-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="0fbff-205">MAPI помещает без ограничений на имя функции, что служба сообщений с помощью прототип **MSGSERVICEENTRY** , но предпочитает имя **на неизвестную запись сервиса**.</span><span class="sxs-lookup"><span data-stu-id="0fbff-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="0fbff-206">Ограничения на порядковый номер для функции нет и одного поставщика DLL-Библиотека может содержать несколько функций.</span><span class="sxs-lookup"><span data-stu-id="0fbff-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="0fbff-207">Тем не менее только одна из функции может быть задано **на неизвестную запись сервиса**.</span><span class="sxs-lookup"><span data-stu-id="0fbff-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="0fbff-208">Служба сообщений можно использовать функцию [BuildDisplayTable](builddisplaytable.md) и метод [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) для упрощения реализации диалогового окна конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0fbff-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="0fbff-209">Это позволяет пользователю отменить операцию MSG_SERVICE_UNINSTALL.</span><span class="sxs-lookup"><span data-stu-id="0fbff-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="0fbff-210">В этом случае функции **на неизвестную запись сервиса** должен проверить, с пользователем, убедитесь, что служба не следует удалять и возвращает MAPI_E_USER_CANCEL, если служба останется установленной.</span><span class="sxs-lookup"><span data-stu-id="0fbff-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="0fbff-211">Функции, основанной на прототип **MSGSERVICEENTRY** возвращает одно из перечисленных значений HRESULT.</span><span class="sxs-lookup"><span data-stu-id="0fbff-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="0fbff-212">MAPI переадресует это значение при ответе на вызов клиента [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="0fbff-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="0fbff-213">Службы сообщений, которые экспортировать функции входа службы необходимо включить свойства **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) и **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) в разделе службы сообщений MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="0fbff-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

