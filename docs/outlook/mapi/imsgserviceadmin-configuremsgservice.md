---
title: Имсгсервицеадминконфигуремсгсервице
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
# <a name="imsgserviceadminconfiguremsgservice"></a><span data-ttu-id="538f2-103">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="538f2-103">IMsgServiceAdmin::ConfigureMsgService</span></span>

  
  
<span data-ttu-id="538f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="538f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="538f2-105">Перестраивает службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="538f2-105">Reconfigures a message service.</span></span>
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a><span data-ttu-id="538f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="538f2-106">Parameters</span></span>

 <span data-ttu-id="538f2-107">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="538f2-107">_lpUID_</span></span>
  
> <span data-ttu-id="538f2-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для настраиваемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="538f2-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to configure.</span></span> 
    
 <span data-ttu-id="538f2-109">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="538f2-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="538f2-110">возврата Дескриптор родительского окна на странице свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="538f2-110">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="538f2-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="538f2-111">_ulFlags_</span></span>
  
> <span data-ttu-id="538f2-112">возврата Битовая маска флагов, которые управляют отображением страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="538f2-112">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="538f2-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="538f2-113">The following flags can be set:</span></span>
    
<span data-ttu-id="538f2-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="538f2-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="538f2-115">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="538f2-115">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="538f2-116">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="538f2-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="538f2-117">МСГ_СЕРВИЦЕ_УИ_РЕАД_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="538f2-117">MSG_SERVICE_UI_READ_ONLY</span></span> 
  
> <span data-ttu-id="538f2-118">Служба сообщений должна отображать страницу свойств конфигурации, но не позволяет пользователю изменить его.</span><span class="sxs-lookup"><span data-stu-id="538f2-118">The message service should display its configuration property sheet but not enable the user to change it.</span></span> <span data-ttu-id="538f2-119">Большинство служб сообщений игнорируют этот флаг.</span><span class="sxs-lookup"><span data-stu-id="538f2-119">Most message services ignore this flag.</span></span>
    
<span data-ttu-id="538f2-120">СЕРВИЦЕ_УИ_АЛЛОВЕД</span><span class="sxs-lookup"><span data-stu-id="538f2-120">SERVICE_UI_ALLOWED</span></span> 
  
> <span data-ttu-id="538f2-121">Служба сообщений должна отображать страницу свойств конфигурации только в том случае, если служба настроена не полностью.</span><span class="sxs-lookup"><span data-stu-id="538f2-121">The message service should display its configuration property sheet only if the service is not completely configured.</span></span>
    
<span data-ttu-id="538f2-122">СЕРВИЦЕ_УИ_АЛВАЙС</span><span class="sxs-lookup"><span data-stu-id="538f2-122">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="538f2-123">Служба сообщений должна всегда отображать страницу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="538f2-123">The message service must always display its configuration property sheet.</span></span> <span data-ttu-id="538f2-124">Если СЕРВИЦЕ_УИ_АЛВАЙС не задано, страница свойств конфигурации может отображаться, если СЕРВИЦЕ_УИ_АЛЛОВЕД задано, а сведения о конфигурации недоступны из массива значений свойств в параметре _лппропс_ .</span><span class="sxs-lookup"><span data-stu-id="538f2-124">If SERVICE_UI_ALWAYS is not set, a configuration property sheet can still be displayed if SERVICE_UI_ALLOWED is set and valid configuration information is not available from the property value array in the  _lpProps_ parameter.</span></span> <span data-ttu-id="538f2-125">Для отображения страницы свойств необходимо задать значение СЕРВИЦЕ_УИ_АЛЛОВЕД или СЕРВИЦЕ_УИ_АЛВАЙС.</span><span class="sxs-lookup"><span data-stu-id="538f2-125">Either SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS must be set for a property sheet to be displayed.</span></span> 
    
 <span data-ttu-id="538f2-126">_Квалуес_</span><span class="sxs-lookup"><span data-stu-id="538f2-126">_cValues_</span></span>
  
> <span data-ttu-id="538f2-127">возврата Количество значений свойств в структуре [спропвалуе](spropvalue.md) , на которую указывает _лппропс_.</span><span class="sxs-lookup"><span data-stu-id="538f2-127">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by  _lpProps_.</span></span> 
    
 <span data-ttu-id="538f2-128">_Лппропс_</span><span class="sxs-lookup"><span data-stu-id="538f2-128">_lpProps_</span></span>
  
> <span data-ttu-id="538f2-129">возврата Указатель на массив значений свойств, описывающих свойства, отображаемые на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="538f2-129">[in] A pointer to an array of property values that describe the properties to display in the property sheet.</span></span> <span data-ttu-id="538f2-130">Параметр _лппропс_ не должен иметь значение null, если службу сообщений следует настроить без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="538f2-130">The  _lpProps_ parameter should not be NULL if the message service should be configured without a user interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="538f2-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="538f2-131">Return value</span></span>

<span data-ttu-id="538f2-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="538f2-132">S_OK</span></span> 
  
> <span data-ttu-id="538f2-133">Служба сообщений успешно настроена.</span><span class="sxs-lookup"><span data-stu-id="538f2-133">The message service was successfully configured.</span></span>
    
<span data-ttu-id="538f2-134">МАПИ_Е_ЕКСТЕНДЕД_ЕРРОР</span><span class="sxs-lookup"><span data-stu-id="538f2-134">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="538f2-135">Ошибка, характерная для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="538f2-135">An error specific to a message service.</span></span> <span data-ttu-id="538f2-136">Чтобы получить структуру [мапиеррор](mapierror.md) , описывающую ошибку, клиентское приложение должно вызвать метод [Имсгсервицеадмин:: GetLastError](imsgserviceadmin-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="538f2-136">To get the [MAPIERROR](mapierror.md) structure that describes the error, the client application should call the [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="538f2-137">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="538f2-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="538f2-138">**Мапиуид** , на который указывает _лпуид_ , не отвечает тому, что используется в существующей службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="538f2-138">The **MAPIUID** pointed to by  _lpUID_ does not match that of an existing message service.</span></span> 
    
<span data-ttu-id="538f2-139">МАПИ_Е_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="538f2-139">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="538f2-140">Служба сообщений не имеет функции точки входа.</span><span class="sxs-lookup"><span data-stu-id="538f2-140">The message service does not have an entry point function.</span></span>
    
<span data-ttu-id="538f2-141">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="538f2-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="538f2-142">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="538f2-142">The user canceled the operation, typically by clicking the **Cancel** button in the property sheet.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="538f2-143">Примечания</span><span class="sxs-lookup"><span data-stu-id="538f2-143">Remarks</span></span>

<span data-ttu-id="538f2-144">Метод **имсгсервицеадмин:: конфигуремсгсервице** позволяет настроить службу сообщений со страницей свойств конфигурации или без нее.</span><span class="sxs-lookup"><span data-stu-id="538f2-144">The **IMsgServiceAdmin::ConfigureMsgService** method enables a message service to be configured, with or without a configuration property sheet.</span></span> 
  
<span data-ttu-id="538f2-145">Чтобы разрешить конфигурацию без отображения страницы свойств, службы сообщений обычно подготовят файл заголовков, включающий константы для всех обязательных и необязательных свойств и их значений.</span><span class="sxs-lookup"><span data-stu-id="538f2-145">To allow configuration without a property sheet display, message services typically prepare a header file that includes constants for all the required and optional properties and their values.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="538f2-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="538f2-146">Notes to callers</span></span>

<span data-ttu-id="538f2-147">Чтобы получить структуру **мапиуид** для службы сообщений, которую необходимо настроить, извлеките столбец **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из строки службы сообщений в таблице служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="538f2-147">To retrieve the **MAPIUID** structure for the message service to configure, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column from the message service's row in the message service table.</span></span> <span data-ttu-id="538f2-148">Для получения дополнительных сведений обратитесь к процедуре, описанной в методе [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="538f2-148">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
<span data-ttu-id="538f2-149">Службу сообщений можно настроить без отображения страницы свойств для пользователя, только если у вас есть дополнительные сведения о значениях свойств, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="538f2-149">You can configure a message service without displaying a property sheet to a user only if you have advance information about the property values to be set.</span></span> <span data-ttu-id="538f2-150">Если вы настраиваете службу сообщений без отображения страницы свойств, передайте допустимые значения свойств в параметре _лппропс_ и не задавайте флажки МСГ_СЕРВИЦЕ_УИ_РЕАД_ОНЛИ, СЕРВИЦЕ_УИ_АЛЛОВЕД или сервице_уи_алвайс.</span><span class="sxs-lookup"><span data-stu-id="538f2-150">If you are configuring a message service without displaying a property sheet, pass valid property values in the  _lpProps_ parameter and do not set the MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED, or SERVICE_UI_ALWAYS flags.</span></span> 
  
<span data-ttu-id="538f2-151">Если вы получаете всю информацию о конфигурации пользователя с помощью страницы свойств, задайте СЕРВИЦЕ_УИ_АЛЛОВЕД в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="538f2-151">If you receive all or some of the configuration information from the user by way of a property sheet, set SERVICE_UI_ALLOWED in  _ulFlags_.</span></span> <span data-ttu-id="538f2-152">Если вы используете сведения о существующем свойстве только для установки параметров по умолчанию и пользователь может изменять параметры, установите СЕРВИЦЕ_УИ_АЛВАЙС в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="538f2-152">If you use existing property information only to establish default settings and the user is able to change the settings, set SERVICE_UI_ALWAYS in  _ulFlags_.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="538f2-153">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="538f2-153">MFCMAPI reference</span></span>

<span data-ttu-id="538f2-154">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="538f2-154">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="538f2-155">**Файл**</span><span class="sxs-lookup"><span data-stu-id="538f2-155">**File**</span></span>|<span data-ttu-id="538f2-156">**Функция**</span><span class="sxs-lookup"><span data-stu-id="538f2-156">**Function**</span></span>|<span data-ttu-id="538f2-157">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="538f2-157">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="538f2-158">Мапипрофилефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="538f2-158">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="538f2-159">Храддсервицетопрофиле</span><span class="sxs-lookup"><span data-stu-id="538f2-159">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="538f2-160">MFCMAPI использует метод **имсгсервицеадмин:: конфигуремсгсервице** для настройки службы, которая была добавлена в профиль.</span><span class="sxs-lookup"><span data-stu-id="538f2-160">MFCMAPI uses the **IMsgServiceAdmin::ConfigureMsgService** method to configure a service that has been added to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="538f2-161">См. также</span><span class="sxs-lookup"><span data-stu-id="538f2-161">See also</span></span>



[<span data-ttu-id="538f2-162">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="538f2-162">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="538f2-163">SPropValue</span><span class="sxs-lookup"><span data-stu-id="538f2-163">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="538f2-164">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="538f2-164">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="538f2-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="538f2-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

