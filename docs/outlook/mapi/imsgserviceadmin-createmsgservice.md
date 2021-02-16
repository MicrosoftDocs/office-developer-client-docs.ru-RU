---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434979"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="9c4c4-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="9c4c4-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="9c4c4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c4c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c4c4-105">Не рекомендуется: рекомендуется использовать [IMsgServiceAdmin2::CreateMsgServiceEx.](imsgserviceadmin2-createmsgserviceex.md)</span><span class="sxs-lookup"><span data-stu-id="9c4c4-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="9c4c4-106">Добавляет службу сообщений в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="9c4c4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c4c4-107">Parameters</span></span>

 <span data-ttu-id="9c4c4-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="9c4c4-108">_lpszService_</span></span>
  
> <span data-ttu-id="9c4c4-109">[in] Указатель на имя добавляемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="9c4c4-110">Это имя службы сообщений должно отображаться в разделе **[Службы]** файла MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="9c4c4-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="9c4c4-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="9c4c4-112">[in] Указатель на отображаемого имени службы сообщений, которая будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="9c4c4-113">Параметр  _lpszDisplayName игнорируется,_ если служба сообщений установила свойство **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)в файле MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="9c4c4-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9c4c4-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="9c4c4-115">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="9c4c4-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9c4c4-116">_ulFlags_</span></span>
  
> <span data-ttu-id="9c4c4-117">[in] Битоваяmas флагов, которая управляет установкой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="9c4c4-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9c4c4-118">The following flags can be set:</span></span>
    
<span data-ttu-id="9c4c4-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9c4c4-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="9c4c4-120">Параметры lpszService и lpszDisplayName следует привести к LPWSTR и интерпретировать как строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="9c4c4-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="9c4c4-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="9c4c4-122">При добавлении новой службы сообщений в профиль подсистема MAPI, основанная на различных обстоятельствах и критериях, часто определяет, что для этого действия требуется перезапуск Outlook.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="9c4c4-123">Если флаг SERVICE_NO_RESTART_WARNING не включен, а пользовательский интерфейс разрешен на основе флагов SERVICE_UI_ALWAYS и SERVICE_UI_ALLOWED, и хотя бы один процесс входит в текущий профиль, эта функция отображает сообщение "Чтобы изменения вступили в силу, необходимо перезапустить Outlook".</span><span class="sxs-lookup"><span data-stu-id="9c4c4-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="9c4c4-124">При включаемом SERVICE_NO_RESTART_WARNING подавляет отображение этого предупреждающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="9c4c4-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="9c4c4-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="9c4c4-126">При необходимости пользовательский интерфейс конфигурации службы сообщений разрешен.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="9c4c4-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="9c4c4-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="9c4c4-128">Служба сообщений отображает свою таблицу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c4c4-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c4c4-129">Return value</span></span>

<span data-ttu-id="9c4c4-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c4c4-130">S_OK</span></span> 
  
> <span data-ttu-id="9c4c4-131">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9c4c4-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9c4c4-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9c4c4-133">Имя службы сообщений не находится в разделе **[Службы]** mapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9c4c4-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c4c4-134">Remarks</span></span>

<span data-ttu-id="9c4c4-135">Метод **IMsgServiceAdmin::CreateMsgService** добавляет службу сообщений в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="9c4c4-136">**CreateMsgService** вызывает функцию точки входа службы сообщений для выполнения любых задач настройки службы.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="9c4c4-137">Если флаг SERVICE_UI_ALLOWED в параметре  _ulFlags,_ устанавливаемая служба сообщений может отображать лист свойств, позволяющий пользователю настраивать свои параметры.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="9c4c4-138">Файл MapiSvc.inf содержит список поставщиков, которые составляют службу сообщений, и свойства каждого из них.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="9c4c4-139">**CreateMsgService** сначала создает новый раздел профиля для службы сообщений, а затем копирует все сведения для этой службы из файла MapiSvc.inf в профиль, создавая новые разделы для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="9c4c4-140">После копирования всех данных из mapiSvc.inf функция точки входа службы сообщений будет вызвана с MSG_SERVICE_CREATE значением, заданным в параметре _ulContext._</span><span class="sxs-lookup"><span data-stu-id="9c4c4-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="9c4c4-141">Если флаг SERVICE_UI_ALLOWED задан в параметре _ulFlags_ метода **CreateMsgService,** значения в параметрах _ulUIParam_ и _ulFlags_ также передаются при создании функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="9c4c4-142">Поставщики услуг должны отображать свои таблицы свойств конфигурации, чтобы пользователи могли настраивать службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9c4c4-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9c4c4-143">Notes to callers</span></span>

 <span data-ttu-id="9c4c4-144">**CreateMsgService** не возвращает структуру [MAPIUID](mapiuid.md) для службы сообщений, добавленной в профиль.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="9c4c4-145">Чтобы получить **MAPIUID** для созданной службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="9c4c4-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="9c4c4-146">Вызовите [метод IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить таблицу администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="9c4c4-147">Найдите строку, которая представляет службу сообщений, написав ограничение **на таблицу, которая** соответствует свойству PR_SERVICE_NAME ([PidTagServiceName)](pidtagservicename-canonical-property.md)с именем службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="9c4c4-148">Извлечение свойства **PR_SERVICE_UID** [(PidTagServiceUid).](pidtagserviceuid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="9c4c4-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="9c4c4-149">Передав значение **свойства PR_SERVICE_UID**  _параметра lpUid_ [методу IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) для настройки службы.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="9c4c4-150">Реализация Microsoft Outlook 2010, русская версия MAPI не поддерживает MAPI_UNICODE и не будет работать, если она используется.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9c4c4-151">Файл  _ulFlags_ SERVICE_NO_RESTART_WARNING может не быть определен в загружаемом файле заголовок, который у вас есть в данный момент. В этом случае вы можете добавить его в код, используя следующее значение: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="9c4c4-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9c4c4-152">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9c4c4-152">MFCMAPI reference</span></span>

<span data-ttu-id="9c4c4-153">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9c4c4-154">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9c4c4-154">**File**</span></span>|<span data-ttu-id="9c4c4-155">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9c4c4-155">**Function**</span></span>|<span data-ttu-id="9c4c4-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9c4c4-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9c4c4-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="9c4c4-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9c4c4-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="9c4c4-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="9c4c4-159">MFCMAPI использует метод **IMsgServiceAdmin::CreateMsgService** для добавления службы в профиль.</span><span class="sxs-lookup"><span data-stu-id="9c4c4-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c4c4-160">См. также</span><span class="sxs-lookup"><span data-stu-id="9c4c4-160">See also</span></span>



[<span data-ttu-id="9c4c4-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c4c4-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="9c4c4-162">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9c4c4-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

