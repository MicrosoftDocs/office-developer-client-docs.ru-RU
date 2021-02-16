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
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="a1f03-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="a1f03-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="a1f03-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1f03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1f03-105">Перенастройка службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a1f03-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="a1f03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1f03-106">Parameters</span></span>

 <span data-ttu-id="a1f03-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="a1f03-107">_lpUID_</span></span>
  
> <span data-ttu-id="a1f03-108">[in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений, которую необходимо настроить.</span><span class="sxs-lookup"><span data-stu-id="a1f03-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="a1f03-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a1f03-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="a1f03-110">[in] Окне родительского окна таблицы свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a1f03-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="a1f03-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1f03-111">_ulFlags_</span></span>
  
> <span data-ttu-id="a1f03-112">[in] Битоваяmas флагов, которая управляет отображением листа свойств.</span><span class="sxs-lookup"><span data-stu-id="a1f03-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="a1f03-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="a1f03-113">The following flags can be set:</span></span>
    
<span data-ttu-id="a1f03-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a1f03-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a1f03-115">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="a1f03-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a1f03-116">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a1f03-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="a1f03-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="a1f03-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="a1f03-118">Служба сообщений должна отобразить свою таблицу свойств конфигурации, но не позволить пользователю изменить ее.</span><span class="sxs-lookup"><span data-stu-id="a1f03-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="a1f03-119">Большинство служб сообщений игнорируют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="a1f03-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="a1f03-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="a1f03-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="a1f03-121">Таблица свойств конфигурации службы сообщений должна отображаться только в том случае, если служба не настроена полностью.</span><span class="sxs-lookup"><span data-stu-id="a1f03-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="a1f03-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="a1f03-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="a1f03-123">Служба сообщений всегда должна отображать свою таблицу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a1f03-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="a1f03-124">Если SERVICE_UI_ALWAYS не задан, лист свойств конфигурации по-прежнему может отображаться, если SERVICE_UI_ALLOWED задан и допустимые сведения о конфигурации недоступны из массива значений свойств в параметре _lpProps._</span><span class="sxs-lookup"><span data-stu-id="a1f03-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="a1f03-125">Для SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS необходимо настроить таблицу свойств.</span><span class="sxs-lookup"><span data-stu-id="a1f03-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="a1f03-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="a1f03-126">_cValues_</span></span>
  
> <span data-ttu-id="a1f03-127">[in] Количество значений свойств в [структуре SPropValue,](spropvalue.md) на которые указывает _lpProps._</span><span class="sxs-lookup"><span data-stu-id="a1f03-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="a1f03-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="a1f03-128">_lpProps_</span></span>
  
> <span data-ttu-id="a1f03-129">[in] Указатель на массив значений свойств, которые описывают свойства, отображаемую на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="a1f03-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="a1f03-130">Параметр  _lpProps_ не должен иметь NULL, если служба сообщений должна быть настроена без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a1f03-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a1f03-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1f03-131">Return value</span></span>

<span data-ttu-id="a1f03-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1f03-132">S_OK</span></span> 
  
> <span data-ttu-id="a1f03-133">Служба сообщений успешно настроена.</span><span class="sxs-lookup"><span data-stu-id="a1f03-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="a1f03-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="a1f03-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="a1f03-135">Ошибка, относяная к службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="a1f03-135">An error specific to a message service.</span></span> <span data-ttu-id="a1f03-136">Чтобы получить [структуру MAPIERROR,](mapierror.md) описываемую ошибку, клиентский приложение должно вызвать метод [IMsgServiceAdmin::GetLastError.](imsgserviceadmin-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="a1f03-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="a1f03-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a1f03-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a1f03-138">**MAPIUID, на** который указывает _lpUID,_ не совпадает с интерфейсом MAPIUID существующей службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a1f03-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="a1f03-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="a1f03-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="a1f03-140">Служба сообщений не имеет функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="a1f03-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="a1f03-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a1f03-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a1f03-142">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="a1f03-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a1f03-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1f03-143">Remarks</span></span>

<span data-ttu-id="a1f03-144">Метод **IMsgServiceAdmin::ConfigureMsgService** позволяет настроить службу сообщений с листом свойств конфигурации или без нее.</span><span class="sxs-lookup"><span data-stu-id="a1f03-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="a1f03-145">Чтобы разрешить настройку без отображения листа свойств, службы сообщений обычно подготавливают файл загона, который содержит константы для всех необходимых и необязательных свойств и их значений.</span><span class="sxs-lookup"><span data-stu-id="a1f03-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1f03-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a1f03-146">Notes to callers</span></span>

<span data-ttu-id="a1f03-147">Чтобы получить структуру **MAPIUID** для службы сообщений, необходимо получить столбец **PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="a1f03-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="a1f03-148">Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md)</span><span class="sxs-lookup"><span data-stu-id="a1f03-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="a1f03-149">Вы можете настроить службу сообщений, не отображая лист свойств для пользователя, только если у вас есть дополнительные сведения о значениях свойств, которые необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="a1f03-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="a1f03-150">Если служба сообщений настраивается без отображения листа свойств, передав допустимые значения свойств в  _параметре lpProps_ и не устанавливая флаги MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="a1f03-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="a1f03-151">Если вы получаете все или некоторые сведения о конфигурации от пользователя с помощью листа свойств, установите SERVICE_UI_ALLOWED _в ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a1f03-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="a1f03-152">Если сведения о существующем свойстве используются только для установки параметров по умолчанию и пользователь может изменить эти параметры, установите SERVICE_UI_ALWAYS в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="a1f03-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1f03-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a1f03-153">MFCMAPI reference</span></span>

<span data-ttu-id="a1f03-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a1f03-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1f03-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a1f03-155">**File**</span></span>|<span data-ttu-id="a1f03-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a1f03-156">**Function**</span></span>|<span data-ttu-id="a1f03-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a1f03-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1f03-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a1f03-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a1f03-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="a1f03-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="a1f03-160">MFCMAPI использует метод **IMsgServiceAdmin::ConfigureMsgService** для настройки службы, добавленной в профиль.</span><span class="sxs-lookup"><span data-stu-id="a1f03-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1f03-161">См. также</span><span class="sxs-lookup"><span data-stu-id="a1f03-161">See also</span></span>



[<span data-ttu-id="a1f03-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a1f03-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a1f03-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a1f03-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="a1f03-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1f03-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="a1f03-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a1f03-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

