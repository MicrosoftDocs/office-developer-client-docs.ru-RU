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
ms.openlocfilehash: a599a6fe5093e52e50d33a1761df5689b7335138
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568296"
---
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="3799e-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="3799e-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="3799e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3799e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3799e-105">Устанавливает службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3799e-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="3799e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3799e-106">Parameters</span></span>

 <span data-ttu-id="3799e-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="3799e-107">_lpUID_</span></span>
  
> <span data-ttu-id="3799e-108">[in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для настройки.</span><span class="sxs-lookup"><span data-stu-id="3799e-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="3799e-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3799e-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="3799e-110">[in] Дескриптор родительского окна окно свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3799e-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="3799e-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3799e-111">_ulFlags_</span></span>
  
> <span data-ttu-id="3799e-112">[in] Битовая маска флаги, определяющее отображение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="3799e-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="3799e-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="3799e-113">The following flags can be set:</span></span>
    
<span data-ttu-id="3799e-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3799e-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3799e-115">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="3799e-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="3799e-116">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="3799e-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="3799e-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="3799e-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="3799e-118">Служба сообщений следует открыть окно свойств конфигурации, но не включать изменения пользователем.</span><span class="sxs-lookup"><span data-stu-id="3799e-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="3799e-119">Большинство служб сообщение пропустить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="3799e-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="3799e-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="3799e-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="3799e-121">Служба сообщений следует открыть окно свойств конфигурации только в том случае, если служба не завершена.</span><span class="sxs-lookup"><span data-stu-id="3799e-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="3799e-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="3799e-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="3799e-123">Служба сообщений всегда должен открыть окно свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3799e-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="3799e-124">Если SERVICE_UI_ALWAYS не задано, свойств конфигурации может по-прежнему отображается, если установлено SERVICE_UI_ALLOWED и сведений о конфигурации допустимый недоступен из массива значение свойства с помощью параметра _lpProps_ .</span><span class="sxs-lookup"><span data-stu-id="3799e-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="3799e-125">SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS должно иметь значение для свойств для отображения.</span><span class="sxs-lookup"><span data-stu-id="3799e-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="3799e-126">_cValues_</span><span class="sxs-lookup"><span data-stu-id="3799e-126">_cValues_</span></span>
  
> <span data-ttu-id="3799e-127">[in] Число значений свойств в структуре [SPropValue](spropvalue.md) , на который указывает _lpProps_.</span><span class="sxs-lookup"><span data-stu-id="3799e-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="3799e-128">_lpProps_</span><span class="sxs-lookup"><span data-stu-id="3799e-128">_lpProps_</span></span>
  
> <span data-ttu-id="3799e-129">[in] Указатель на массив значений свойств, которые описывают свойства для отображения в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="3799e-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="3799e-130">Параметр _lpProps_ не должен быть NULL, если служба сообщений, необходимо настроить без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3799e-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3799e-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3799e-131">Return value</span></span>

<span data-ttu-id="3799e-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="3799e-132">S_OK</span></span> 
  
> <span data-ttu-id="3799e-133">Служба сообщений успешно настроено.</span><span class="sxs-lookup"><span data-stu-id="3799e-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="3799e-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="3799e-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="3799e-135">Ошибка специально для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3799e-135">An error specific to a message service.</span></span> <span data-ttu-id="3799e-136">Чтобы получить структура [MAPIERROR](mapierror.md) с описанием ошибки, клиентское приложение следует вызовите метод [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3799e-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="3799e-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3799e-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3799e-138">**MAPIUID** , на который указывает _lpUID_ не совпадает с существующей службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3799e-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="3799e-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="3799e-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="3799e-140">Служба сообщений не имеет функцию точки входа.</span><span class="sxs-lookup"><span data-stu-id="3799e-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="3799e-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="3799e-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="3799e-142">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="3799e-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3799e-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="3799e-143">Remarks</span></span>

<span data-ttu-id="3799e-144">Метод **IMsgServiceAdmin::ConfigureMsgService** позволяет службы сообщений, который требуется настроить, независимо от настройки свойств.</span><span class="sxs-lookup"><span data-stu-id="3799e-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="3799e-145">Чтобы разрешить конфигурации без отображение листа свойств, службы сообщений обычно Подготовьте файл заголовка, который включает в себя константы для все необходимые и дополнительные свойства и их значения.</span><span class="sxs-lookup"><span data-stu-id="3799e-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3799e-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3799e-146">Notes to callers</span></span>

<span data-ttu-id="3799e-147">Для получения **MAPIUID** структуру для настройки службы сообщений, извлечь столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3799e-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="3799e-148">Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3799e-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="3799e-149">Для настройки службы сообщение без отображения свойств пользователю только в том случае, если у вас есть Дополнительные сведения о значения свойств должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="3799e-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="3799e-150">При настройке службы сообщений без отображения свойств, передайте допустимыми значениями свойства с помощью параметра _lpProps_ и не задано флаги MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="3799e-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="3799e-151">Если вы получаете все или некоторые сведения о конфигурации от пользователя через страницу свойств необходимо задайте SERVICE_UI_ALLOWED в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="3799e-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="3799e-152">Если использовать существующие сведения о свойствах только для установки параметров по умолчанию, и пользователь может изменять параметры, задайте SERVICE_UI_ALWAYS в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="3799e-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3799e-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3799e-153">MFCMAPI reference</span></span>

<span data-ttu-id="3799e-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3799e-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3799e-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3799e-155">**File**</span></span>|<span data-ttu-id="3799e-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3799e-156">**Function**</span></span>|<span data-ttu-id="3799e-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3799e-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3799e-158">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="3799e-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="3799e-159">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="3799e-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="3799e-160">Mfcmapi (en) использует метод **IMsgServiceAdmin::ConfigureMsgService** для настройки службы, который был добавлен в профиль.</span><span class="sxs-lookup"><span data-stu-id="3799e-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3799e-161">См. также</span><span class="sxs-lookup"><span data-stu-id="3799e-161">See also</span></span>



[<span data-ttu-id="3799e-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="3799e-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="3799e-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3799e-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3799e-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3799e-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="3799e-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3799e-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

