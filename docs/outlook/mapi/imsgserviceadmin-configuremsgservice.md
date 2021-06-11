---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422189"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="ebf86-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="ebf86-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="ebf86-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ebf86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ebf86-105">Перенастройка службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebf86-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="ebf86-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ebf86-106">Parameters</span></span>

 <span data-ttu-id="ebf86-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="ebf86-107">_lpUID_</span></span>
  
> <span data-ttu-id="ebf86-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebf86-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="ebf86-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ebf86-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="ebf86-110">[in] Ручка родительского окна листа свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ebf86-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="ebf86-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ebf86-111">_ulFlags_</span></span>
  
> <span data-ttu-id="ebf86-112">[in] Битмашка флагов, контролируемая отображением листа свойств.</span><span class="sxs-lookup"><span data-stu-id="ebf86-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="ebf86-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ebf86-113">The following flags can be set:</span></span>
    
<span data-ttu-id="ebf86-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ebf86-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ebf86-115">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="ebf86-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="ebf86-116">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="ebf86-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="ebf86-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="ebf86-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="ebf86-118">Служба сообщений должна отображать свой лист свойств конфигурации, но не позволяет пользователю изменять его.</span><span class="sxs-lookup"><span data-stu-id="ebf86-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="ebf86-119">Большинство служб сообщений игнорируют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="ebf86-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="ebf86-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="ebf86-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="ebf86-121">Служба сообщений должна отображать свой лист свойств конфигурации только в том случае, если служба не настроена полностью.</span><span class="sxs-lookup"><span data-stu-id="ebf86-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="ebf86-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="ebf86-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="ebf86-123">Служба сообщений всегда должна отображать свой лист свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ebf86-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="ebf86-124">Если SERVICE_UI_ALWAYS не задан, лист свойства конфигурации по-прежнему может отображаться, если SERVICE_UI_ALLOWED установлен и допустимые сведения о конфигурации недоступны из массива значений свойств в параметре _lpProps._</span><span class="sxs-lookup"><span data-stu-id="ebf86-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="ebf86-125">Необходимо SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS для отображения листа свойств.</span><span class="sxs-lookup"><span data-stu-id="ebf86-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="ebf86-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="ebf86-126">_cValues_</span></span>
  
> <span data-ttu-id="ebf86-127">[in] Количество значений свойств в [структуре SPropValue,](spropvalue.md) на которые указывает _lpProps._</span><span class="sxs-lookup"><span data-stu-id="ebf86-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="ebf86-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="ebf86-128">_lpProps_</span></span>
  
> <span data-ttu-id="ebf86-129">[in] Указатель на массив значений свойств, описывая свойства, отображаемые в листе свойств.</span><span class="sxs-lookup"><span data-stu-id="ebf86-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="ebf86-130">Параметр  _lpProps не_ должен быть NULL, если служба сообщений должна быть настроена без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ebf86-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ebf86-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebf86-131">Return value</span></span>

<span data-ttu-id="ebf86-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="ebf86-132">S_OK</span></span> 
  
> <span data-ttu-id="ebf86-133">Служба сообщений была успешно настроена.</span><span class="sxs-lookup"><span data-stu-id="ebf86-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="ebf86-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="ebf86-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="ebf86-135">Ошибка, специфическая для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebf86-135">An error specific to a message service.</span></span> <span data-ttu-id="ebf86-136">Чтобы получить структуру [MAPIERROR,](mapierror.md) описываемую ошибку, клиентский приложение должно вызвать [метод IMsgServiceAdmin::GetLastError.](imsgserviceadmin-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="ebf86-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="ebf86-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ebf86-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ebf86-138">**MapIUID,** на который указывает _lpUID,_ не соответствует существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebf86-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="ebf86-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="ebf86-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="ebf86-140">Служба сообщений не имеет функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="ebf86-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="ebf86-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ebf86-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="ebf86-142">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в листе свойств.</span><span class="sxs-lookup"><span data-stu-id="ebf86-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ebf86-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="ebf86-143">Remarks</span></span>

<span data-ttu-id="ebf86-144">Метод **IMsgServiceAdmin::ConfigureMsgService** позволяет настраивать службу сообщений с листом свойств конфигурации или без нее.</span><span class="sxs-lookup"><span data-stu-id="ebf86-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="ebf86-145">Чтобы разрешить конфигурацию без отображения листа свойств, службы сообщений обычно готовят файл загона, который включает константы для всех необходимых и необязательных свойств и их значений.</span><span class="sxs-lookup"><span data-stu-id="ebf86-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ebf86-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ebf86-146">Notes to callers</span></span>

<span data-ttu-id="ebf86-147">Чтобы получить структуру **MAPIUID** для настройки службы **сообщений, извлекаем** столбец PR_SERVICE_UID [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ebf86-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="ebf86-148">Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="ebf86-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="ebf86-149">Вы можете настроить службу сообщений без отображения листа свойств пользователю только в том случае, если у вас есть дополнительные сведения о значениях свойств, которые необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="ebf86-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="ebf86-150">При настройке службы сообщений без отображения листа свойств передай допустимые значения свойств в  _параметре lpProps_ и не задай MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS флагов.</span><span class="sxs-lookup"><span data-stu-id="ebf86-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="ebf86-151">Если вы получаете все или некоторые сведения о конфигурации от пользователя с помощью листа свойств, установите SERVICE_UI_ALLOWED  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ebf86-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="ebf86-152">Если вы используете существующие сведения о свойстве только для создания параметров по умолчанию и пользователь может изменить параметры, установите SERVICE_UI_ALWAYS  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ebf86-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ebf86-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ebf86-153">MFCMAPI reference</span></span>

<span data-ttu-id="ebf86-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ebf86-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ebf86-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ebf86-155">**File**</span></span>|<span data-ttu-id="ebf86-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ebf86-156">**Function**</span></span>|<span data-ttu-id="ebf86-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ebf86-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ebf86-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="ebf86-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ebf86-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="ebf86-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="ebf86-160">MFCMAPI использует **метод IMsgServiceAdmin::ConfigureMsgService** для настройки службы, добавленной в профиль.</span><span class="sxs-lookup"><span data-stu-id="ebf86-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ebf86-161">См. также</span><span class="sxs-lookup"><span data-stu-id="ebf86-161">See also</span></span>



[<span data-ttu-id="ebf86-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ebf86-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ebf86-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ebf86-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ebf86-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ebf86-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="ebf86-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ebf86-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

