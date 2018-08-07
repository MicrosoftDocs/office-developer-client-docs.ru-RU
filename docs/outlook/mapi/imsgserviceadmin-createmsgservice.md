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
ms.openlocfilehash: 6e0bdd7108bacd17134592ac05ba71510fde76d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809388"
---
# <a name="imsgserviceadmincreatemsgservice"></a><span data-ttu-id="24656-103">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="24656-103">IMsgServiceAdmin::CreateMsgService</span></span>

  
  
<span data-ttu-id="24656-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24656-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24656-105">Устаревшие: Рекомендуется использовать [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) .</span><span class="sxs-lookup"><span data-stu-id="24656-105">Deprecated: The use of [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) is recommended.</span></span> <span data-ttu-id="24656-106">Добавление службы сообщений для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="24656-106">Adds a message service to the current profile.</span></span> 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="24656-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24656-107">Parameters</span></span>

 <span data-ttu-id="24656-108">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="24656-108">_lpszService_</span></span>
  
> <span data-ttu-id="24656-109">[in] Указатель на имя службы сообщений для добавления.</span><span class="sxs-lookup"><span data-stu-id="24656-109">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="24656-110">Это имя службы сообщений, которые должны встречаться в разделе **[Services]** файла MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="24656-110">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="24656-111">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="24656-111">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="24656-112">[in] Указатель на отображаемое имя службы сообщений для добавления.</span><span class="sxs-lookup"><span data-stu-id="24656-112">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="24656-113">Параметр _lpszDisplayName_ игнорируется, если служба сообщений значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в файле MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="24656-113">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="24656-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="24656-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="24656-115">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="24656-115">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="24656-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24656-116">_ulFlags_</span></span>
  
> <span data-ttu-id="24656-117">[in] Битовая маска флаги, который определяет способ установки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="24656-117">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="24656-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="24656-118">The following flags can be set:</span></span>
    
<span data-ttu-id="24656-119">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="24656-119">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="24656-120">Параметры lpszDisplayName и lpszService должен привести к LPWSTR и как строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="24656-120">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="24656-121">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="24656-121">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="24656-122">При добавлении нового сообщения службы профиля, подсистема MAPI на основе различных ситуациях и условия, часто определяет, что это действие требуется для Outlook.</span><span class="sxs-lookup"><span data-stu-id="24656-122">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="24656-123">Если флаг SERVICE_NO_RESTART_WARNING не указан и может пользовательского интерфейса — в зависимости от флаги SERVICE_UI_ALWAYS и SERVICE_UI_ALLOWED - и по крайней мере один процесс выполнил вход в систему текущего профиля, эта функция отображает сообщение «необходимо перезапустить Outlook для Эти изменения вступили в силу.»</span><span class="sxs-lookup"><span data-stu-id="24656-123">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="24656-124">Включая флаг SERVICE_NO_RESTART_WARNING подавляет, сообщение с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="24656-124">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="24656-125">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="24656-125">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="24656-126">Конфигурация службы сообщения пользовательского интерфейса может при необходимости.</span><span class="sxs-lookup"><span data-stu-id="24656-126">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="24656-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="24656-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="24656-128">Служба сообщений отображается окно свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="24656-128">The message service displays its configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24656-129">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="24656-129">Return value</span></span>

<span data-ttu-id="24656-130">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="24656-130">S_OK</span></span> 
  
> <span data-ttu-id="24656-131">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="24656-131">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="24656-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="24656-132">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="24656-133">Имя службы сообщение не является в разделе **[Services]** MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="24656-133">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="24656-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="24656-134">Remarks</span></span>

<span data-ttu-id="24656-135">Метод **IMsgServiceAdmin::CreateMsgService** добавляет службы сообщений для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="24656-135">The **IMsgServiceAdmin::CreateMsgService** method adds a message service to the current profile.</span></span> <span data-ttu-id="24656-136">**CreateMsgService** вызывает функцию точки входа службы сообщений для выполнения каких-либо задач конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="24656-136">**CreateMsgService** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="24656-137">Если в параметре _ulFlags_ флаг SERVICE_UI_ALLOWED, устанавливаемой службы сообщений можно отобразить страницу свойств, чтобы разрешить пользователю настраивать его параметры.</span><span class="sxs-lookup"><span data-stu-id="24656-137">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet to enable the user to configure its settings.</span></span> 
  
<span data-ttu-id="24656-138">Файла MapiSvc.inf содержит список поставщиков, которые составляют службы сообщений и свойства для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="24656-138">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="24656-139">**CreateMsgService** сначала создается новый раздел профиля для службы сообщений и затем копирует все данные для этой службы из файла MapiSvc.inf в профиль, создание новых раздела для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="24656-139">**CreateMsgService** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="24656-140">После копирования всей информации из MapiSvc.inf функции точки входа службы сообщений вызывается с MSG_SERVICE_CREATE значение, установленное в параметре _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="24656-140">After all the information has been copied from MapiSvc.inf, the message service's entry point function is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="24656-141">Если флаг SERVICE_UI_ALLOWED установлен в параметре _ulFlags_ метод **CreateMsgService** , в параметрах _ulUIParam_ и _ulFlags_ также передаются значения при вызове функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="24656-141">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgService** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="24656-142">Поставщиков услуг должны отображать свойств их конфигурации, поэтому пользователи могут настраивать службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="24656-142">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="24656-143">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="24656-143">Notes to callers</span></span>

 <span data-ttu-id="24656-144">**CreateMsgService** не возвращает структуру [MAPIUID](mapiuid.md) для службы сообщений, который был добавлен к профилю.</span><span class="sxs-lookup"><span data-stu-id="24656-144">**CreateMsgService** does not return the [MAPIUID](mapiuid.md) structure for the message service that was added to the profile.</span></span> 
  
<span data-ttu-id="24656-145">Чтобы получить **MAPIUID** сообщение о создании службы, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="24656-145">To retrieve the **MAPIUID** for the created message service, use the following procedure:</span></span> 
  
1. <span data-ttu-id="24656-146">Вызовите метод [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для получения таблицы администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="24656-146">Call the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method to get the message service administration table.</span></span> 
    
2. <span data-ttu-id="24656-147">Найдите строку, которая представляет службы сообщений, установив ограничение в таблице, которая соответствует свойству **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) с именем службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="24656-147">Locate the row that represents the message service by placing a restriction on the table that matches the **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) property with the name of the message service.</span></span> 
    
3. <span data-ttu-id="24656-148">Получение свойств службы **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="24656-148">Retrieve the service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span> 
    
4. <span data-ttu-id="24656-149">Передайте значение свойства **PR_SERVICE_UID** с помощью параметра _lpUid_ методу [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , чтобы настроить службу.</span><span class="sxs-lookup"><span data-stu-id="24656-149">Pass the value of the **PR_SERVICE_UID** property in the  _lpUid_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
    
> [!CAUTION]
> <span data-ttu-id="24656-150">Реализация Microsoft Outlook 2010 подсистемы MAPI не поддерживает MAPI_UNICODE и завершится ошибкой, если она используется.</span><span class="sxs-lookup"><span data-stu-id="24656-150">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="24656-151">_UlFlags_ SERVICE_NO_RESTART_WARNING не могут быть определены в файле загружаемых заголовка в настоящий момент, в этом случае можно добавить его в код с помощью следующее значение: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="24656-151">The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24656-152">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="24656-152">MFCMAPI reference</span></span>

<span data-ttu-id="24656-153">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="24656-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24656-154">**����**</span><span class="sxs-lookup"><span data-stu-id="24656-154">**File**</span></span>|<span data-ttu-id="24656-155">**�������**</span><span class="sxs-lookup"><span data-stu-id="24656-155">**Function**</span></span>|<span data-ttu-id="24656-156">**�����������**</span><span class="sxs-lookup"><span data-stu-id="24656-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24656-157">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="24656-157">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="24656-158">HrAddServiceToProfile</span><span class="sxs-lookup"><span data-stu-id="24656-158">HrAddServiceToProfile</span></span>  <br/> |<span data-ttu-id="24656-159">Mfcmapi (en) использует метод **IMsgServiceAdmin::CreateMsgService** для добавления в профиль службы.</span><span class="sxs-lookup"><span data-stu-id="24656-159">MFCMAPI uses the **IMsgServiceAdmin::CreateMsgService** method to add a service to a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24656-160">См. также</span><span class="sxs-lookup"><span data-stu-id="24656-160">See also</span></span>



[<span data-ttu-id="24656-161">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24656-161">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="24656-162">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="24656-162">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

