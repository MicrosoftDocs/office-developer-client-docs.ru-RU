---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410184"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="56b22-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="56b22-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="56b22-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56b22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56b22-105">Добавляет службу сообщений в текущий профиль и возвращает новый UID службы.</span><span class="sxs-lookup"><span data-stu-id="56b22-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="56b22-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56b22-106">Parameters</span></span>

 <span data-ttu-id="56b22-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="56b22-107">_lpszService_</span></span>
  
> <span data-ttu-id="56b22-108">[in] Указатель на имя службы сообщений, которая будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="56b22-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="56b22-109">Это имя службы сообщений должно отображаться в разделе **[Службы]** файла MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="56b22-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="56b22-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="56b22-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="56b22-111">[in] Указатель на отображаемого имени службы сообщений, которая будет добавлена.</span><span class="sxs-lookup"><span data-stu-id="56b22-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="56b22-112">Параметр  _lpszDisplayName игнорируется,_ если служба сообщений установила свойство **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)в файле MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="56b22-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="56b22-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="56b22-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="56b22-114">[in] Handle to the parent window of any dialog boxes or windows this method displays.</span><span class="sxs-lookup"><span data-stu-id="56b22-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="56b22-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56b22-115">_ulFlags_</span></span>
  
> <span data-ttu-id="56b22-116">[in] Битоваяmas флагов, которая управляет установкой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="56b22-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="56b22-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="56b22-117">The following flags can be set:</span></span>
    
<span data-ttu-id="56b22-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="56b22-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="56b22-119">Параметры lpszService и lpszDisplayName следует привести к LPWSTR и интерпретировать как строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="56b22-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="56b22-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="56b22-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="56b22-121">При добавлении новой службы сообщений в профиль подсистема MAPI, основанная на различных обстоятельствах и критериях, часто определяет, что для этого действия требуется перезапуск Outlook.</span><span class="sxs-lookup"><span data-stu-id="56b22-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="56b22-122">Если флаг SERVICE_NO_RESTART_WARNING не включен, а пользовательский интерфейс разрешен на основе флагов SERVICE_UI_ALWAYS и SERVICE_UI_ALLOWED, и хотя бы один процесс входит в текущий профиль, эта функция отображает сообщение "Чтобы изменения вступили в силу, необходимо перезапустить Outlook".</span><span class="sxs-lookup"><span data-stu-id="56b22-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="56b22-123">При включаемом SERVICE_NO_RESTART_WARNING подавляет отображение этого предупреждающих сообщений.</span><span class="sxs-lookup"><span data-stu-id="56b22-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="56b22-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="56b22-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="56b22-125">При необходимости пользовательский интерфейс конфигурации службы сообщений разрешен.</span><span class="sxs-lookup"><span data-stu-id="56b22-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="56b22-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="56b22-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="56b22-127">Служба сообщений отображает свою таблицу свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="56b22-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="56b22-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="56b22-128">_lpuidService_</span></span>
  
> <span data-ttu-id="56b22-129">[out] Указатель на UID добавленной службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="56b22-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56b22-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56b22-130">Return value</span></span>

<span data-ttu-id="56b22-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="56b22-131">S_OK</span></span>
  
> <span data-ttu-id="56b22-132">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="56b22-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="56b22-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="56b22-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="56b22-134">Имя службы сообщений не находится в разделе **[Службы]** mapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="56b22-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="56b22-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="56b22-135">Remarks</span></span>

<span data-ttu-id="56b22-136">Метод **IMsgServiceAdmin2::CreateMsgServiceEx** добавляет службу сообщений в текущий профиль.</span><span class="sxs-lookup"><span data-stu-id="56b22-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="56b22-137">**CreateMsgServiceEx** вызывает функцию точки входа службы сообщений для выполнения любых задач настройки службы.</span><span class="sxs-lookup"><span data-stu-id="56b22-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="56b22-138">Если флаг SERVICE_UI_ALLOWED в параметре  _ulFlags,_ устанавливаемая служба сообщений может отображать лист свойств, позволяющий пользователю настраивать параметры.</span><span class="sxs-lookup"><span data-stu-id="56b22-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="56b22-139">Файл MapiSvc.inf содержит список поставщиков, которые составляют службу сообщений, и свойства каждого из них.</span><span class="sxs-lookup"><span data-stu-id="56b22-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="56b22-140">**CreateMsgServiceEx** сначала создает новый раздел профиля для службы сообщений, а затем копирует все сведения для этой службы из файла MapiSvc.inf в профиль, создавая новые разделы для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="56b22-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="56b22-141">После копирования всех сведений из mapiSvc.inf функция точки входа службы сообщений **MSGSERVICEENTRY** будет вызвана со значением MSG_SERVICE_CREATE, заданным в параметре _ulContext._</span><span class="sxs-lookup"><span data-stu-id="56b22-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="56b22-142">Если флаг SERVICE_UI_ALLOWED задан в параметре _ulFlags_ метода **CreateMsgServiceEx,** значения в параметрах _ulUIParam_ и _ulFlags_ также передаются при создании функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="56b22-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="56b22-143">Поставщики услуг должны отображать свои таблицы свойств конфигурации, чтобы пользователи могли настраивать службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="56b22-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="56b22-144">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="56b22-144">Notes to callers</span></span>

<span data-ttu-id="56b22-145">Если аргумент **CreateMsgServiceEx** _lpuidService_ не имеет NULL, свойство **PR_SERVICE_UID** ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)службы сообщений, добавленной в профиль, возвращается в **GUID,** на который он указывает.</span><span class="sxs-lookup"><span data-stu-id="56b22-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="56b22-146">Передав значение **свойства PR_SERVICE_UID**  _lpuidService_ [методу IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) для настройки службы.</span><span class="sxs-lookup"><span data-stu-id="56b22-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="56b22-147">Реализация Microsoft Outlook 2010, русская версия MAPI не поддерживает MAPI_UNICODE и не будет работать, если она используется.</span><span class="sxs-lookup"><span data-stu-id="56b22-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="56b22-148">Интерфейс IMsgServiceAdmin2 доступен тем же объектом, который реализует интерфейс IMsgServiceAdmin, и был доступен с помощью реализации подсистемы MAPI в Outlook, начиная с Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="56b22-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="56b22-149">Его IID определяется следующим образом: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING может не быть определен в загружаемом файле заголовщика, в этом случае его можно добавить в код, используя следующее значение: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="56b22-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56b22-150">См. также</span><span class="sxs-lookup"><span data-stu-id="56b22-150">See also</span></span>



[<span data-ttu-id="56b22-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="56b22-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="56b22-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="56b22-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

