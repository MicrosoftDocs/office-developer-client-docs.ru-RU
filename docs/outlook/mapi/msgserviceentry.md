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
# <a name="msgserviceentry"></a><span data-ttu-id="d15d9-103">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="d15d9-103">MSGSERVICEENTRY</span></span>

  
  
<span data-ttu-id="d15d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d15d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d15d9-105">Определяет прототип функции точки входа службы сообщений для поддержки конфигурации службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d15d9-105">Defines a prototype for a message service entry point function to support message service configuration.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d15d9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d15d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="d15d9-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="d15d9-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="d15d9-108">Определенная функция реализована следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d15d9-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="d15d9-109">Службы сообщений</span><span class="sxs-lookup"><span data-stu-id="d15d9-109">Message services</span></span>  <br/> |
|<span data-ttu-id="d15d9-110">Определенная функция, вызываемая:</span><span class="sxs-lookup"><span data-stu-id="d15d9-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="d15d9-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="d15d9-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d15d9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d15d9-112">Parameters</span></span>

 <span data-ttu-id="d15d9-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="d15d9-113">_hInstance_</span></span>
  
> <span data-ttu-id="d15d9-114">возврата Дескриптор экземпляра службы Провидердлл.</span><span class="sxs-lookup"><span data-stu-id="d15d9-114">[in] Handle of the instance of the service providerDLL.</span></span> <span data-ttu-id="d15d9-115">Дескриптор обычно используется для извлечения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d15d9-115">The handle is typically used to retrieve resources.</span></span> 
    
 <span data-ttu-id="d15d9-116">_лпмаллок_</span><span class="sxs-lookup"><span data-stu-id="d15d9-116">_lpMalloc_</span></span>
  
> <span data-ttu-id="d15d9-117">возврата Указатель на объект распределителя памяти, который предоставляет интерфейс для **выделения** OLE.</span><span class="sxs-lookup"><span data-stu-id="d15d9-117">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d15d9-118">При работе с определенными интерфейсами, такими как **IStream**, службе сообщений может потребоваться использовать этот метод распределения.</span><span class="sxs-lookup"><span data-stu-id="d15d9-118">The message service may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="d15d9-119">_лпмаписуп_</span><span class="sxs-lookup"><span data-stu-id="d15d9-119">_lpMAPISup_</span></span>
  
> <span data-ttu-id="d15d9-120">возврата Указатель на [имаписуппорт:](imapisupportiunknown.md) реализация интерфейса IUnknown.</span><span class="sxs-lookup"><span data-stu-id="d15d9-120">[in] Pointer to an [IMAPISupport : IUnknown](imapisupportiunknown.md) interface implementation.</span></span> 
    
 <span data-ttu-id="d15d9-121">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="d15d9-121">_ulUIParam_</span></span>
  
> <span data-ttu-id="d15d9-122">возврата Зависящее от реализации значение, используемое для передачи сведений о пользовательском интерфейсе в функцию или ноль.</span><span class="sxs-lookup"><span data-stu-id="d15d9-122">[in] An implementation-specific value used for passing user interface information to a function or zero.</span></span> <span data-ttu-id="d15d9-123">Параметр _улуипарам_ является дескриптором родительского окна для диалогового окна Configuration и имеет тип HWND (приведение к ULONG_PTR).</span><span class="sxs-lookup"><span data-stu-id="d15d9-123">The  _ulUIParam_ parameter is the parent window handle for the configuration dialog box and is of type HWND (cast to a ULONG_PTR).</span></span> <span data-ttu-id="d15d9-124">Нулевое значение указывает, что родительское окно отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d15d9-124">A value of zero indicates that there is no parent window.</span></span> 
    
 <span data-ttu-id="d15d9-125">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d15d9-125">_ulFlags_</span></span>
  
> <span data-ttu-id="d15d9-126">возврата Битовая маска флагов, указывающих параметры функции записи службы.</span><span class="sxs-lookup"><span data-stu-id="d15d9-126">[in] Bitmask of flags indicating options for the service entry function.</span></span> <span data-ttu-id="d15d9-127">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d15d9-127">The following flags can be set:</span></span>
    
<span data-ttu-id="d15d9-128">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d15d9-128">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d15d9-129">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d15d9-129">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d15d9-130">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d15d9-130">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="d15d9-131">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="d15d9-131">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="d15d9-132">Пользовательский интерфейс конфигурации службы должен отображать текущую конфигурацию, но не разрешать пользователю его изменять.</span><span class="sxs-lookup"><span data-stu-id="d15d9-132">The service's configuration user interface should display the current configuration but not allow the user to change it.</span></span> 
    
<span data-ttu-id="d15d9-133">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="d15d9-133">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="d15d9-134">Разрешает отображение диалогового окна конфигурации при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d15d9-134">Permits a configuration dialog box to be displayed if necessary.</span></span> <span data-ttu-id="d15d9-135">Если установлен флаг SERVICE_UI_ALLOWED, диалоговое окно должно отображаться только в том случае, если массив значений свойства _лппропс_ пуст или не содержит допустимой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d15d9-135">When the SERVICE_UI_ALLOWED flag is set, the dialog box should be displayed only if the  _lpProps_ property value array is empty or does not contain a valid configuration.</span></span> <span data-ttu-id="d15d9-136">Если SERVICE_UI_ALLOWED не задано, диалоговое окно по-прежнему может отображаться, если установлен флаг SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="d15d9-136">If SERVICE_UI_ALLOWED is not set, a dialog box might still be displayed if the SERVICE_UI_ALWAYS flag is set.</span></span> 
    
<span data-ttu-id="d15d9-137">UI_CURRENT_PROVIDER_FIRST</span><span class="sxs-lookup"><span data-stu-id="d15d9-137">UI_CURRENT_PROVIDER_FIRST</span></span> 
  
> <span data-ttu-id="d15d9-138">Запрашивает отображение диалогового окна Конфигурация для активного поставщика поверх других диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="d15d9-138">Requests that the configuration dialog box for the active provider be displayed on top of other dialog boxes.</span></span> 
    
<span data-ttu-id="d15d9-139">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="d15d9-139">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="d15d9-140">Служба сообщений должна отображать диалоговое окно конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d15d9-140">Requires the message service to display a configuration dialog box.</span></span> <span data-ttu-id="d15d9-141">Если флаг SERVICE_UI_ALWAYS не установлен, диалоговое окно конфигурации по-прежнему может отображаться, если установлен флаг SERVICE_UI_ALLOWED, а сведения о конфигурации недоступны в массиве значений свойства _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="d15d9-141">If the SERVICE_UI_ALWAYS flag is not set, a configuration dialog box might still be displayed if the SERVICE_UI_ALLOWED flag is set and valid configuration information is not available from the  _lpProps_ property value array.</span></span> <span data-ttu-id="d15d9-142">Для отображения пользовательского интерфейса необходимо задать SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="d15d9-142">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set to allow a user interface to be displayed.</span></span> 
    
 <span data-ttu-id="d15d9-143">_улконтекст_</span><span class="sxs-lookup"><span data-stu-id="d15d9-143">_ulContext_</span></span>
  
> <span data-ttu-id="d15d9-144">возврата Операция конфигурации, выполняемая в настоящее время MAPI.</span><span class="sxs-lookup"><span data-stu-id="d15d9-144">[in] The configuration operation that MAPI is currently performing.</span></span> <span data-ttu-id="d15d9-145">Параметр _улконтекст_ будет содержать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d15d9-145">The  _ulContext_ parameter will contain one of the following values:</span></span> 
    
<span data-ttu-id="d15d9-146">MSG_SERVICE_CONFIGURE</span><span class="sxs-lookup"><span data-stu-id="d15d9-146">MSG_SERVICE_CONFIGURE</span></span> 
  
> <span data-ttu-id="d15d9-147">В профиль необходимо внести изменения в конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="d15d9-147">Changes to the service's configuration should be made in the profile.</span></span> <span data-ttu-id="d15d9-148">Если установлен флаг SERVICE_UI_ALWAYS, служба должна отображать диалоговое окно настройки.</span><span class="sxs-lookup"><span data-stu-id="d15d9-148">If the SERVICE_UI_ALWAYS flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="d15d9-149">Диалоговое окно также должно отображаться, если установлен флаг SERVICE_UI_ALLOWED и параметр _лппропс_ пуст или не содержит допустимых данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d15d9-149">The dialog box should also be displayed if the SERVICE_UI_ALLOWED flag is set and the  _lpProps_ parameter is empty or does not contain valid configuration data.</span></span> <span data-ttu-id="d15d9-150">Если _лппропс_ содержит допустимые данные, диалоговое окно не должно отображаться, и служба должна использовать эти данные для внесения изменений в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d15d9-150">If  _lpProps_ contains valid data, no dialog box should be displayed and the service should use this data for making the configuration change.</span></span> 
    
<span data-ttu-id="d15d9-151">MSG_SERVICE_CREATE</span><span class="sxs-lookup"><span data-stu-id="d15d9-151">MSG_SERVICE_CREATE</span></span> 
  
> <span data-ttu-id="d15d9-152">Служба добавляется в профиль.</span><span class="sxs-lookup"><span data-stu-id="d15d9-152">The service is being added to a profile.</span></span> <span data-ttu-id="d15d9-153">Если установлен флаг SERVICE_UI_ALWAYS или SERVICE_UI_ALLOWED, служба должна отображать диалоговое окно настройки.</span><span class="sxs-lookup"><span data-stu-id="d15d9-153">If either the SERVICE_UI_ALWAYS or SERVICE_UI_ALLOWED flag is set, the service should display its configuration dialog box.</span></span> <span data-ttu-id="d15d9-154">Если не задан ни один из этих флагов, произойдет ошибка службы.</span><span class="sxs-lookup"><span data-stu-id="d15d9-154">If neither flag is set, the service should fail.</span></span> 
    
<span data-ttu-id="d15d9-155">MSG_SERVICE_DELETE</span><span class="sxs-lookup"><span data-stu-id="d15d9-155">MSG_SERVICE_DELETE</span></span> 
  
> <span data-ttu-id="d15d9-156">Служба удаляется из профиля.</span><span class="sxs-lookup"><span data-stu-id="d15d9-156">The service is being removed from a profile.</span></span> <span data-ttu-id="d15d9-157">После получения этого события служба должна возвратить S_OK.</span><span class="sxs-lookup"><span data-stu-id="d15d9-157">After receiving this event, the service should return S_OK.</span></span>
    
<span data-ttu-id="d15d9-158">MSG_SERVICE_INSTALL</span><span class="sxs-lookup"><span data-stu-id="d15d9-158">MSG_SERVICE_INSTALL</span></span> 
  
> <span data-ttu-id="d15d9-159">Служба установлена на рабочую станцию пользователя с помощью сети, гибкого диска или другого внешнего носителя.</span><span class="sxs-lookup"><span data-stu-id="d15d9-159">The service has been installed to the user's workstation from a network, floppy disk, or other external medium.</span></span> <span data-ttu-id="d15d9-160">После получения этого события служба обычно возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="d15d9-160">After receiving this event, the service usually returns S_OK.</span></span> 
    
<span data-ttu-id="d15d9-161">MSG_SERVICE_PROVIDER_CREATE</span><span class="sxs-lookup"><span data-stu-id="d15d9-161">MSG_SERVICE_PROVIDER_CREATE</span></span> 
  
> <span data-ttu-id="d15d9-162">Запрос создания службой дополнительного экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="d15d9-162">Requests that the service create an additional instance of a provider.</span></span> <span data-ttu-id="d15d9-163">Если служба поддерживает эту операцию, она должна вызывать [ипровидерадмин:: креатепровидер](iprovideradmin-createprovider.md).</span><span class="sxs-lookup"><span data-stu-id="d15d9-163">If the service supports this operation, it should call [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md).</span></span> <span data-ttu-id="d15d9-164">Если служба не поддерживает эту операцию, она может возвратить MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="d15d9-164">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="d15d9-165">MSG_SERVICE_PROVIDER_DELETE</span><span class="sxs-lookup"><span data-stu-id="d15d9-165">MSG_SERVICE_PROVIDER_DELETE</span></span> 
  
> <span data-ttu-id="d15d9-166">Запрашивает удаление экземпляра поставщика службой.</span><span class="sxs-lookup"><span data-stu-id="d15d9-166">Requests that the service delete a provider instance.</span></span> <span data-ttu-id="d15d9-167">Если служба поддерживает эту операцию, она должна вызывать [ипровидерадмин::D елетепровидер](iprovideradmin-deleteprovider.md).</span><span class="sxs-lookup"><span data-stu-id="d15d9-167">If the service supports this operation, it should call [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md).</span></span> <span data-ttu-id="d15d9-168">Если служба не поддерживает эту операцию, она может возвратить MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="d15d9-168">If the service does not support this operation, it can return MAPI_E_NO_SUPPORT.</span></span>
    
<span data-ttu-id="d15d9-169">MSG_SERVICE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="d15d9-169">MSG_SERVICE_UNINSTALL</span></span> 
  
> <span data-ttu-id="d15d9-170">Служба удаляется.</span><span class="sxs-lookup"><span data-stu-id="d15d9-170">The service is being removed.</span></span> <span data-ttu-id="d15d9-171">После получения этого события служба может выполнять какие – либо задачи очистки, которые необходимо выполнить, прежде чем служба завершится, а затем вернется со значением Success.</span><span class="sxs-lookup"><span data-stu-id="d15d9-171">After receiving this event, the service can perform any cleanup tasks that should be done before the service ends and then return with a success value.</span></span> <span data-ttu-id="d15d9-172">Если пользователь отменяет удаление, служба должна возвратить MAPI_E_USER_CANCEL.</span><span class="sxs-lookup"><span data-stu-id="d15d9-172">If the user cancels the removal, the service should return MAPI_E_USER_CANCEL.</span></span> 
    
 <span data-ttu-id="d15d9-173">_квалуес_</span><span class="sxs-lookup"><span data-stu-id="d15d9-173">_cValues_</span></span>
  
> <span data-ttu-id="d15d9-174">возврата Количество значений свойств в массиве, на которое указывает параметр _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="d15d9-174">[in] Count of property values in the array pointed to by the  _lpProps_ parameter.</span></span> <span data-ttu-id="d15d9-175">Если MAPI не передает значения свойств, значение параметра _квалуес_ равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d15d9-175">The value of the  _cValues_ parameter is zero if MAPI is passing no property values.</span></span> 
    
 <span data-ttu-id="d15d9-176">_лппропс_</span><span class="sxs-lookup"><span data-stu-id="d15d9-176">_lpProps_</span></span>
  
> <span data-ttu-id="d15d9-177">возврата Указатель на необязательный массив структуры [спропвалуе](spropvalue.md) , указывающий значения для свойств, поддерживаемых поставщиком, которые функция будет использовать при настройке службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d15d9-177">[in] Pointer to an optional array of [SPropValue](spropvalue.md) structures indicating values for provider-supported properties that the function will use in configuring the message service.</span></span> <span data-ttu-id="d15d9-178">Функция использует этот параметр только в том случае, если для параметра _улконтекст_ задано значение MSG_SERVICE_CONFIGURE.</span><span class="sxs-lookup"><span data-stu-id="d15d9-178">The function only uses this parameter if the  _ulContext_ parameter is set to MSG_SERVICE_CONFIGURE.</span></span> <span data-ttu-id="d15d9-179">Этот параметр обычно используется для передачи пути к файлу для службы на основе файлов, например, службе личной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d15d9-179">This parameter is commonly used to pass the path to a file for a file-based service, such as a personal address book service.</span></span> <span data-ttu-id="d15d9-180">Если флаг MSG_SERVICE_CONFIGURE не передается в параметре _ulFlags_ , параметр _лппропс_ должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="d15d9-180">If the MSG_SERVICE_CONFIGURE flag is not passed in the  _ulFlags_ parameter, the  _lpProps_ parameter must be zero.</span></span> 
    
 <span data-ttu-id="d15d9-181">_лппровидерадмин_</span><span class="sxs-lookup"><span data-stu-id="d15d9-181">_lpProviderAdmin_</span></span>
  
> <span data-ttu-id="d15d9-182">возврата Указатель на [ипровидерадмин: интерфейс IUnknown](iprovideradminiunknown.md) , который функция может использовать для определения местонахождения разделов профилей для определенного поставщика в текущей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="d15d9-182">[in] Pointer to an [IProviderAdmin:IUnknown](iprovideradminiunknown.md) interface that the function can use to locate profile sections for a specific provider in the current message service.</span></span> 
    
 <span data-ttu-id="d15d9-183">_лппмапиеррор_</span><span class="sxs-lookup"><span data-stu-id="d15d9-183">_lppMapiError_</span></span>
  
> <span data-ttu-id="d15d9-184">вышли Указатель на структуру [мапиеррор](mapierror.md) .</span><span class="sxs-lookup"><span data-stu-id="d15d9-184">[out] Pointer to a [MAPIERROR](mapierror.md) structure.</span></span> <span data-ttu-id="d15d9-185">Структура выделяется с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d15d9-185">The structure is allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> <span data-ttu-id="d15d9-186">Все элементы являются необязательными, несмотря на то что большинство структур содержит допустимую строку сообщения об ошибке в элементе _лпсзеррор_ .</span><span class="sxs-lookup"><span data-stu-id="d15d9-186">All members are optional, although most structures will contain a valid error message string in the  _lpszError_ member.</span></span> <span data-ttu-id="d15d9-187">Если присутствуют члены _лпсзкомпонент_ или _лпсзеррор_ структуры, их память, в конечном итоге, должна быть освобождена одним вызовом [мапифрибуффер](mapifreebuffer.md) в базовой структуре.</span><span class="sxs-lookup"><span data-stu-id="d15d9-187">If the  _lpszComponent_ or  _lpszError_ members of the structure are present, their memory must eventually be freed by a single call to [MAPIFreeBuffer](mapifreebuffer.md) on the base structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d15d9-188">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d15d9-188">Return value</span></span>

<span data-ttu-id="d15d9-189">S_OK</span><span class="sxs-lookup"><span data-stu-id="d15d9-189">S_OK</span></span> 
  
> <span data-ttu-id="d15d9-190">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d15d9-190">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="d15d9-191">MAPI_E_UNCONFIGURED</span><span class="sxs-lookup"><span data-stu-id="d15d9-191">MAPI_E_UNCONFIGURED</span></span> 
  
> <span data-ttu-id="d15d9-192">Поставщик услуг не настроен.</span><span class="sxs-lookup"><span data-stu-id="d15d9-192">The service provider has not been configured.</span></span> 
    
<span data-ttu-id="d15d9-193">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d15d9-193">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d15d9-194">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d15d9-194">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
<span data-ttu-id="d15d9-195">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d15d9-195">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d15d9-196">Поставщик либо не поддерживает изменения в его объектах, либо не поддерживает уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="d15d9-196">The provider either does not support changes to its objects or does not support notification of changes.</span></span> 
    
<span data-ttu-id="d15d9-197">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d15d9-197">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d15d9-198">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="d15d9-198">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d15d9-199">Примечания</span><span class="sxs-lookup"><span data-stu-id="d15d9-199">Remarks</span></span>

<span data-ttu-id="d15d9-200">Функция, определенная с помощью прототипа функции **мсгсервицеентри** , позволяет службам сообщений настраивать себя или выполнять другие действия, зависящие от службы.</span><span class="sxs-lookup"><span data-stu-id="d15d9-200">A function defined using the **MSGSERVICEENTRY** function prototype enables message services to configure themselves or to perform other service-specific actions.</span></span> <span data-ttu-id="d15d9-201">Функция в основном предводит диалоговое окно, в котором пользователь может изменять параметры, характерные для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d15d9-201">The function primarily furnishes a dialog box in which the user can change settings specific to the message service.</span></span> <span data-ttu-id="d15d9-202">Кроме того, он может поддерживать программную конфигурацию с помощью массива значений свойства, переданного в параметре _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="d15d9-202">It can also support programmatic configuration by using the property value array passed in the  _lpProps_ parameter.</span></span> <span data-ttu-id="d15d9-203">Программная конфигурация является необязательной, если служба не поддерживает мастер профилей, для которого он необходим.</span><span class="sxs-lookup"><span data-stu-id="d15d9-203">Programmatic configuration is optional unless the service supports the Profile Wizard, for which it is required.</span></span> 
  
<span data-ttu-id="d15d9-204">MAPI вызывает эту точку входа из приложения панели управления или в ответ на вызов клиентского приложения [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) или [Имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="d15d9-204">MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="d15d9-205">MAPI не накладывает ограничений на имя функции, которую служба сообщений использует для прототипа **мсгсервицеентри** , но предпочитает имя **сервицеентри**.</span><span class="sxs-lookup"><span data-stu-id="d15d9-205">MAPI places no restriction on the function name that a message service uses for the **MSGSERVICEENTRY** prototype but prefers the name **ServiceEntry**.</span></span> <span data-ttu-id="d15d9-206">Для функции отсутствует ограничение по порядковому номеру, а одна библиотека DLL поставщика может содержать более одной функции.</span><span class="sxs-lookup"><span data-stu-id="d15d9-206">There is no restriction on the ordinal for the function, and a single provider DLL can contain more than one function.</span></span> <span data-ttu-id="d15d9-207">Однако только одна из этих функций может называться **сервицеентри**.</span><span class="sxs-lookup"><span data-stu-id="d15d9-207">However, only one of the functions can be named **ServiceEntry**.</span></span> 
  
<span data-ttu-id="d15d9-208">Служба сообщений может использовать функцию [буилддисплайтабле](builddisplaytable.md) и метод [Имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md) для упрощения реализации диалогового окна настройки.</span><span class="sxs-lookup"><span data-stu-id="d15d9-208">A message service can use the [BuildDisplayTable](builddisplaytable.md) function and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method to simplify configuration dialog box implementation.</span></span> 
  
<span data-ttu-id="d15d9-209">Пользователь может отменить MSG_SERVICE_UNINSTALL операцию.</span><span class="sxs-lookup"><span data-stu-id="d15d9-209">It is possible for a user to cancel a MSG_SERVICE_UNINSTALL operation.</span></span> <span data-ttu-id="d15d9-210">В этом случае функция **сервицеентри** должна проанализировать пользователя, чтобы убедиться, что служба не должна быть удалена и возвращать MAPI_E_USER_CANCEL, если служба остается установленной.</span><span class="sxs-lookup"><span data-stu-id="d15d9-210">In this case, the **ServiceEntry** function should check with the user to verify that the service should not be removed and return MAPI_E_USER_CANCEL if the service remains installed.</span></span> 
  
<span data-ttu-id="d15d9-211">Функция, основанная на прототипе **мсгсервицеентри** , возвращает одно из значений HRESULT, перечисленных в списке.</span><span class="sxs-lookup"><span data-stu-id="d15d9-211">A function based on the **MSGSERVICEENTRY** prototype returns one of the HRESULT values listed.</span></span> <span data-ttu-id="d15d9-212">MAPI пересылает это значение при ответе на вызов клиента в [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="d15d9-212">MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> 
  
<span data-ttu-id="d15d9-213">Службы сообщений, в которых экспортируется функция записи службы, должны включать свойства **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) и **PR_SERVICE_ENTRY_NAME** ([PIDTAGSERVICEENTRYNAME](pidtagserviceentryname-canonical-property.md)) в разделе Служба сообщений в Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="d15d9-213">Message services that export a service entry function must include the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) and **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) properties in the message service section of MAPISVC.INF.</span></span> 
  

