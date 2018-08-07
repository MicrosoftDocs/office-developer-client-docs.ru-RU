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
ms.openlocfilehash: 3aae61f7b21c507da7955dbb4393d13bfb5fa24c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809358"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a><span data-ttu-id="e807d-103">IMsgServiceAdmin2::CreateMsgServiceEx</span><span class="sxs-lookup"><span data-stu-id="e807d-103">IMsgServiceAdmin2::CreateMsgServiceEx</span></span>

  
  
<span data-ttu-id="e807d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e807d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e807d-105">Добавление службы сообщений для текущего профиля и возвращает, недавно добавленных службы ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="e807d-105">Adds a message service to the current profile and returns that newly added service UID.</span></span>
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a><span data-ttu-id="e807d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e807d-106">Parameters</span></span>

 <span data-ttu-id="e807d-107">_lpszService_</span><span class="sxs-lookup"><span data-stu-id="e807d-107">_lpszService_</span></span>
  
> <span data-ttu-id="e807d-108">[in] Указатель на имя службы сообщений для добавления.</span><span class="sxs-lookup"><span data-stu-id="e807d-108">[in] A pointer to the name of the message service to add.</span></span> <span data-ttu-id="e807d-109">Это имя службы сообщений, которые должны встречаться в разделе **[Services]** файла MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="e807d-109">This message service name must appear in the **[Services]** section of the MapiSvc.inf file.</span></span> 
    
 <span data-ttu-id="e807d-110">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="e807d-110">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="e807d-111">[in] Указатель на отображаемое имя службы сообщений для добавления.</span><span class="sxs-lookup"><span data-stu-id="e807d-111">[in] A pointer to the display name of the message service to add.</span></span> <span data-ttu-id="e807d-112">Параметр _lpszDisplayName_ игнорируется, если служба сообщений значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в файле MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="e807d-112">The  _lpszDisplayName_ parameter is ignored if the message service has set the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MapiSvc.inf file.</span></span>
    
 <span data-ttu-id="e807d-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e807d-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="e807d-114">[in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.</span><span class="sxs-lookup"><span data-stu-id="e807d-114">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="e807d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e807d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="e807d-116">[in] Битовая маска флаги, который определяет способ установки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e807d-116">[in] A bitmask of flags that controls how the message service is installed.</span></span> <span data-ttu-id="e807d-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="e807d-117">The following flags can be set:</span></span>
    
<span data-ttu-id="e807d-118">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e807d-118">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="e807d-119">Параметры lpszDisplayName и lpszService должен привести к LPWSTR и как строк в кодировке Юникод.</span><span class="sxs-lookup"><span data-stu-id="e807d-119">The lpszService and the lpszDisplayName parameters should be cast to LPWSTR and interpreted as Unicode strings.</span></span>
    
<span data-ttu-id="e807d-120">SERVICE_NO_RESTART_WARNING</span><span class="sxs-lookup"><span data-stu-id="e807d-120">SERVICE_NO_RESTART_WARNING</span></span>
  
> <span data-ttu-id="e807d-121">При добавлении нового сообщения службы профиля, подсистема MAPI на основе различных ситуациях и условия, часто определяет, что это действие требуется для Outlook.</span><span class="sxs-lookup"><span data-stu-id="e807d-121">When adding a new message service to the profile, the MAPI subsystem, based on various circumstances and criteria, often determines that this action requires a restart of Outlook.</span></span> <span data-ttu-id="e807d-122">Если флаг SERVICE_NO_RESTART_WARNING не указан и может пользовательского интерфейса — в зависимости от флаги SERVICE_UI_ALWAYS и SERVICE_UI_ALLOWED - и по крайней мере один процесс выполнил вход в систему текущего профиля, эта функция отображает сообщение «необходимо перезапустить Outlook для Эти изменения вступили в силу.»</span><span class="sxs-lookup"><span data-stu-id="e807d-122">If the SERVICE_NO_RESTART_WARNING flag is not included and UI is allowed - based on the SERVICE_UI_ALWAYS and SERVICE_UI_ALLOWED flags - and at least one process is logged onto the current profile, this function displays the message "You must restart Outlook for these changes to take effect."</span></span> <span data-ttu-id="e807d-123">Включая флаг SERVICE_NO_RESTART_WARNING подавляет, сообщение с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="e807d-123">Including the SERVICE_NO_RESTART_WARNING flag suppresses the display of that warning message.</span></span>
    
<span data-ttu-id="e807d-124">SERVICE_UI_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="e807d-124">SERVICE_UI_ALLOWED</span></span>
  
> <span data-ttu-id="e807d-125">Конфигурация службы сообщения пользовательского интерфейса может при необходимости.</span><span class="sxs-lookup"><span data-stu-id="e807d-125">The message service configuration UI is allowed if needed.</span></span>
    
<span data-ttu-id="e807d-126">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="e807d-126">SERVICE_UI_ALWAYS</span></span>
  
> <span data-ttu-id="e807d-127">Служба сообщений отображается окно свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e807d-127">The message service displays its configuration property sheet.</span></span>
    
 <span data-ttu-id="e807d-128">_lpuidService_</span><span class="sxs-lookup"><span data-stu-id="e807d-128">_lpuidService_</span></span>
  
> <span data-ttu-id="e807d-129">[out] Указатель на UID добавлена служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="e807d-129">[out] The pointer to the UID of the message service added.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e807d-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="e807d-131">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e807d-131">S_OK</span></span>
  
> <span data-ttu-id="e807d-132">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="e807d-132">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e807d-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e807d-133">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="e807d-134">Имя службы сообщение не является в разделе **[Services]** MapiSvc.inf.</span><span class="sxs-lookup"><span data-stu-id="e807d-134">The message service name is not in the **[Services]** section of MapiSvc.inf.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e807d-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="e807d-135">Remarks</span></span>

<span data-ttu-id="e807d-136">Метод **IMsgServiceAdmin2::CreateMsgServiceEx** добавляет службы сообщений для текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="e807d-136">The **IMsgServiceAdmin2::CreateMsgServiceEx** method adds a message service to the current profile.</span></span> <span data-ttu-id="e807d-137">**CreateMsgServiceEx** вызывает функцию точки входа службы сообщений для выполнения каких-либо задач конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="e807d-137">**CreateMsgServiceEx** calls the message service's entry point function to perform any service-specific configuration tasks.</span></span> <span data-ttu-id="e807d-138">Если в параметре _ulFlags_ флаг SERVICE_UI_ALLOWED, устанавливаемой службы сообщений можно отобразить страницу свойств, позволяя пользователям для настройки ее параметров.</span><span class="sxs-lookup"><span data-stu-id="e807d-138">If the SERVICE_UI_ALLOWED flag is set in the  _ulFlags_ parameter, the message service being installed can display a property sheet enabling the user to configure its settings.</span></span> 
  
<span data-ttu-id="e807d-139">Файла MapiSvc.inf содержит список поставщиков, которые составляют службы сообщений и свойства для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e807d-139">The MapiSvc.inf file contains the list of providers that make up a message service and the properties for each.</span></span> <span data-ttu-id="e807d-140">**CreateMsgServiceEx** сначала создается новый раздел профиля для службы сообщений и затем копирует все данные для этой службы из файла MapiSvc.inf в профиль, создание новых раздела для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="e807d-140">**CreateMsgServiceEx** first creates a new profile section for the message service and then copies all of the information for that service from the MapiSvc.inf file into the profile, creating new sections for each provider.</span></span> 
  
<span data-ttu-id="e807d-141">После копирования всей информации из MapiSvc.inf функцию точки входа для службы сообщений, **MSGSERVICEENTRY**вызывается с MSG_SERVICE_CREATE значение, установленное в параметре _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="e807d-141">After all the information has been copied from MapiSvc.inf, the message service's entry point function, **MSGSERVICEENTRY**, is called with the MSG_SERVICE_CREATE value set in the  _ulContext_ parameter.</span></span> <span data-ttu-id="e807d-142">Если флаг SERVICE_UI_ALLOWED установлен в параметре _ulFlags_ метод **CreateMsgServiceEx** , в параметрах _ulUIParam_ и _ulFlags_ также передаются значения при вызове функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e807d-142">If the SERVICE_UI_ALLOWED flag is set in the **CreateMsgServiceEx** method's  _ulFlags_ parameter, the values in the  _ulUIParam_ and  _ulFlags_ parameters are also passed when the message service's entry point function is called.</span></span> <span data-ttu-id="e807d-143">Поставщиков услуг должны отображать свойств их конфигурации, поэтому пользователи могут настраивать службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e807d-143">Service providers should display their configuration property sheets so users can configure the message service.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e807d-144">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e807d-144">Notes to callers</span></span>

<span data-ttu-id="e807d-145">Если аргумент _lpuidService_ **CreateMsgServiceEx** не может быть NULL, свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений, который был добавлен к профилю возвращается **идентификатор GUID** , на который указывает.</span><span class="sxs-lookup"><span data-stu-id="e807d-145">If the **CreateMsgServiceEx** _lpuidService_ argument is not NULL, the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property of the message service that was added to the profile is returned in the **GUID** to which it points.</span></span> 
  
<span data-ttu-id="e807d-146">Передайте значение свойства **PR_SERVICE_UID** с помощью параметра _lpuidService_ методу [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , чтобы настроить службу.</span><span class="sxs-lookup"><span data-stu-id="e807d-146">Pass the value of the **PR_SERVICE_UID** property in the  _lpuidService_ parameter to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method to configure the service.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="e807d-147">Реализация Microsoft Outlook 2010 подсистемы MAPI не поддерживает MAPI_UNICODE и завершится ошибкой, если она используется.</span><span class="sxs-lookup"><span data-stu-id="e807d-147">The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e807d-148">Интерфейс IMsgServiceAdmin2 предоставляется тот же объект, который реализует интерфейс IMsgServiceAdmin и уже была доступна с помощью Outlook реализации подсистемы MAPI, начиная с Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="e807d-148">The IMsgServiceAdmin2 interface is exposed by the same object that implements the IMsgServiceAdmin interface, and has been available using Outlook's implementation of the MAPI subsystem since Outlook 2003.</span></span> <span data-ttu-id="e807d-149">ИД его интерфейса определяется следующим образом: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING не могут быть определены в файле загружаемых заголовка в настоящий момент, в этом случае можно добавить его в код с помощью следующее значение: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`</span><span class="sxs-lookup"><span data-stu-id="e807d-149">Its IID is defined as follows: >  `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)`>  `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> The  _ulFlags_ SERVICE_NO_RESTART_WARNING might not be defined in the downloadable header file you currently have, in which case you can add it to your code using the following value: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e807d-150">См. также</span><span class="sxs-lookup"><span data-stu-id="e807d-150">See also</span></span>



[<span data-ttu-id="e807d-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span><span class="sxs-lookup"><span data-stu-id="e807d-151">IMsgServiceAdmin2 : IMsgServiceAdmin</span></span>](imsgserviceadmin2imsgserviceadmin.md)


[<span data-ttu-id="e807d-152">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e807d-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

