---
title: имсгсервицеадминконфигуремсгсервице
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
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="5c393-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="5c393-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="5c393-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c393-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c393-105">Перестраивает службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c393-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="5c393-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c393-106">Parameters</span></span>

 <span data-ttu-id="5c393-107">_лпуид_</span><span class="sxs-lookup"><span data-stu-id="5c393-107">_lpUID_</span></span>
  
> <span data-ttu-id="5c393-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для настраиваемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c393-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="5c393-109">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="5c393-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="5c393-110">возврата Дескриптор родительского окна на странице свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5c393-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="5c393-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5c393-111">_ulFlags_</span></span>
  
> <span data-ttu-id="5c393-112">возврата Битовая маска флагов, которые управляют отображением страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="5c393-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="5c393-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5c393-113">The following flags can be set:</span></span>
    
<span data-ttu-id="5c393-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c393-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5c393-115">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="5c393-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="5c393-116">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5c393-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="5c393-117">MSG_SERVICE_UI_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="5c393-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="5c393-118">Служба сообщений должна отображать страницу свойств конфигурации, но не позволяет пользователю изменить его.</span><span class="sxs-lookup"><span data-stu-id="5c393-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="5c393-119">Большинство служб сообщений игнорируют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="5c393-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="5c393-120">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="5c393-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="5c393-121">Служба сообщений должна отображать страницу свойств конфигурации только в том случае, если служба настроена не полностью.</span><span class="sxs-lookup"><span data-stu-id="5c393-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="5c393-122">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="5c393-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="5c393-123">Служба сообщений должна всегда отображать страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5c393-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="5c393-124">Если параметр SERVICE_UI_ALWAYS не задан, страница свойств конфигурации по-прежнему может отображаться, если SERVICE_UI_ALLOWED заданы, а сведения о конфигурации недоступны в массиве значений свойств в параметре _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="5c393-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="5c393-125">Для отображения страницы свойств необходимо задать SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="5c393-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="5c393-126">_квалуес_</span><span class="sxs-lookup"><span data-stu-id="5c393-126">_cValues_</span></span>
  
> <span data-ttu-id="5c393-127">возврата Количество значений свойств в структуре [спропвалуе](spropvalue.md) , на которую указывает _лппропс_.</span><span class="sxs-lookup"><span data-stu-id="5c393-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="5c393-128">_лппропс_</span><span class="sxs-lookup"><span data-stu-id="5c393-128">_lpProps_</span></span>
  
> <span data-ttu-id="5c393-129">возврата Указатель на массив значений свойств, описывающих свойства, отображаемые на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="5c393-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="5c393-130">Параметр _лппропс_ не должен иметь значение null, если службу сообщений следует настроить без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5c393-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5c393-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c393-131">Return value</span></span>

<span data-ttu-id="5c393-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c393-132">S_OK</span></span> 
  
> <span data-ttu-id="5c393-133">Служба сообщений успешно настроена.</span><span class="sxs-lookup"><span data-stu-id="5c393-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="5c393-134">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="5c393-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="5c393-135">Ошибка, характерная для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c393-135">An error specific to a message service.</span></span> <span data-ttu-id="5c393-136">Чтобы получить структуру [мапиеррор](mapierror.md) , описывающую ошибку, клиентское приложение должно вызвать метод [Имсгсервицеадмин:: GetLastError](imsgserviceadmin-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5c393-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="5c393-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5c393-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5c393-138">**Мапиуид** , на который указывает _лпуид_ , не отвечает тому, что используется в существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c393-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="5c393-139">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="5c393-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="5c393-140">Служба сообщений не имеет функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="5c393-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="5c393-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="5c393-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="5c393-142">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="5c393-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5c393-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c393-143">Remarks</span></span>

<span data-ttu-id="5c393-144">Метод **имсгсервицеадмин:: конфигуремсгсервице** позволяет настроить службу сообщений со страницей свойств конфигурации или без нее.</span><span class="sxs-lookup"><span data-stu-id="5c393-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="5c393-145">Чтобы разрешить конфигурацию без отображения страницы свойств, службы сообщений обычно подготовят файл заголовков, включающий константы для всех обязательных и необязательных свойств и их значений.</span><span class="sxs-lookup"><span data-stu-id="5c393-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="5c393-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5c393-146">Notes to callers</span></span>

<span data-ttu-id="5c393-147">Чтобы получить структуру **мапиуид** для службы сообщений для настройки, извлеките столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из строки службы сообщений в таблице служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c393-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="5c393-148">Для получения дополнительных сведений обратитесь к процедуре, описанной в методе [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="5c393-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="5c393-149">Службу сообщений можно настроить без отображения страницы свойств для пользователя, только если у вас есть дополнительные сведения о значениях свойств, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="5c393-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="5c393-150">Если вы настраиваете службу сообщений без отображения страницы свойств, передайте допустимые значения свойств в параметр _лппропс_ и не задавайте флажки MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="5c393-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="5c393-151">Если вы получаете все или некоторые сведения о конфигурации от пользователя с помощью страницы свойств, задайте SERVICE_UI_ALLOWED в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5c393-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="5c393-152">Если вы используете сведения о существующем свойстве только для установки параметров по умолчанию и пользователь может изменять параметры, установите SERVICE_UI_ALWAYS в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="5c393-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5c393-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5c393-153">MFCMAPI reference</span></span>

<span data-ttu-id="5c393-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5c393-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5c393-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5c393-155">**File**</span></span>|<span data-ttu-id="5c393-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5c393-156">**Function**</span></span>|<span data-ttu-id="5c393-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5c393-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c393-158">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="5c393-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="5c393-159">храддсервицетопрофиле</span><span class="sxs-lookup"><span data-stu-id="5c393-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="5c393-160">MFCMAPI использует метод **имсгсервицеадмин:: конфигуремсгсервице** для настройки службы, которая была добавлена в профиль.</span><span class="sxs-lookup"><span data-stu-id="5c393-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c393-161">См. также</span><span class="sxs-lookup"><span data-stu-id="5c393-161">See also</span></span>



[<span data-ttu-id="5c393-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5c393-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5c393-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5c393-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="5c393-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c393-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="5c393-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5c393-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

