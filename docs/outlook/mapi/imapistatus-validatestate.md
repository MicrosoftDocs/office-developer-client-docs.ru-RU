---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438150"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="cf1a7-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cf1a7-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="cf1a7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf1a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf1a7-105">Подтверждает сведения о внешнем состоянии, доступные для ресурса MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="cf1a7-106">Этот метод поддерживается во всех объектах состояния.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cf1a7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf1a7-107">Parameters</span></span>

<span data-ttu-id="cf1a7-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="cf1a7-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="cf1a7-109">[in] Handle to the parent window of any dialog boxes or windows that this method displays.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="cf1a7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf1a7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="cf1a7-111">[in] Битоваяmas флагов, контролирующая проверку.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="cf1a7-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="cf1a7-112">The following flags can be set:</span></span>
    
<span data-ttu-id="cf1a7-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="cf1a7-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="cf1a7-114">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в соответствующем диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="cf1a7-115">У объекта status есть два варианта:</span><span class="sxs-lookup"><span data-stu-id="cf1a7-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="cf1a7-116">Продолжите работу над операцией.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="cf1a7-117">Остановите операцию и MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="cf1a7-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="cf1a7-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="cf1a7-119">Изменено одно или несколько свойств конфигурации объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="cf1a7-120">Клиенты могут установить этот флаг, чтобы позволить пулу MAPI динамически исправлять критические сбои поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="cf1a7-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="cf1a7-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="cf1a7-122">Объект состояния должен выполнить подключение.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-122">The status object should perform a connection.</span></span> <span data-ttu-id="cf1a7-123">Если этот флаг используется с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, подключение происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="cf1a7-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="cf1a7-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="cf1a7-125">Объект состояния должен выполнить операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="cf1a7-126">Если этот флаг используется с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE, отключение происходит без кэшации.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="cf1a7-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cf1a7-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cf1a7-128">Записи в таблице кэша загона должны быть обработаны, все сообщения, помеченные флагом MSGSTATUS_REMOTE_DOWNLOAD, должны быть загружены, а все сообщения с флагом MSGSTATUS_REMOTE_DELETE должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="cf1a7-129">Сообщения, для MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE, должны быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="cf1a7-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cf1a7-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cf1a7-131">Для удаленного поставщика транспорта необходимо скачать новый список заглавных сообщений и очистить все флаги, помечаемые состоянием сообщения.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="cf1a7-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="cf1a7-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="cf1a7-133">Предотвращает отображение пользовательского интерфейса в объекте состояния в рамках операции.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf1a7-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf1a7-134">Return value</span></span>

<span data-ttu-id="cf1a7-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf1a7-135">S_OK</span></span> 
  
> <span data-ttu-id="cf1a7-136">Проверка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-136">The validation was successful.</span></span>
    
<span data-ttu-id="cf1a7-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cf1a7-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cf1a7-138">В настоящее время идет другая операция; его следует разрешить завершить или остановить перед началом этой операции.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="cf1a7-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cf1a7-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cf1a7-140">Объект состояния не поддерживает метод проверки, на что указывает отсутствие флага STATUS_VALIDATE_STATE в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cf1a7-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="cf1a7-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="cf1a7-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="cf1a7-142">Пользователь отменил операцию проверки, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="cf1a7-143">Это значение возвращается только удаленными поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf1a7-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf1a7-144">Remarks</span></span>

<span data-ttu-id="cf1a7-145">Метод **IMAPIStatus::ValidateState** проверяет состояние ресурса, связанного с объектом состояния.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="cf1a7-146">**ValidateState** — единственный метод в интерфейсе [IMAPIStatus,](imapistatusimapiprop.md) необходимый для всех объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="cf1a7-147">Точное поведение этого метода зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="cf1a7-148">В следующей таблице описывается реализация каждого из различных типов объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="cf1a7-149">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="cf1a7-149">**Status object**</span></span>|<span data-ttu-id="cf1a7-150">Реализация ValidateState\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cf1a7-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf1a7-151">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="cf1a7-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="cf1a7-152">Проверяет состояние всех ресурсов, которые принадлежат текущим активным поставщикам служб и подсистеме.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="cf1a7-153">MapI spooler</span><span class="sxs-lookup"><span data-stu-id="cf1a7-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="cf1a7-154">Выполняет вход всех поставщиков транспорта независимо от того, вошли ли они в систему.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="cf1a7-155">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="cf1a7-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="cf1a7-156">Проверяет записи в разделе профиля.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="cf1a7-157">Поставщик услуг</span><span class="sxs-lookup"><span data-stu-id="cf1a7-157">Service provider</span></span>  <br/> |<span data-ttu-id="cf1a7-158">Реализация зависит от типа поставщика и флагов, установленных в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="cf1a7-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="cf1a7-159">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="cf1a7-159">Notes to implementers</span></span>

<span data-ttu-id="cf1a7-160">Удаленные клиентские приложения звонят **методу ValidateState,** чтобы запустить удаленную обработку для различных действий.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="cf1a7-161">Этот метод в основном используется для того, чтобы устанавливать биты состояния для связи с пулером MAPI вместо того, чтобы фактически делать какие-либо работы.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="cf1a7-162">Как правило, поставщик транспорта устанавливает флаги в строке состояния, которые указывают пуле MAPI, какие действия необходимо инициировать для выполнения запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="cf1a7-163">В этой модели взаимодействия между клиентом и пулом транспорта действия, запрашиваемая клиентом, являются асинхронными, так как **ValidateState** возвращается до завершения запрашиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="cf1a7-164">Однако действия, которые необязательно связаны с системой обмена сообщениями или связаны с интерфейсом транспорта, могут быть синхронными.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="cf1a7-165">Клиентские приложения передает битовуюmass из следующих флагов, чтобы указать, какие действия должен принять удаленный поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="cf1a7-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="cf1a7-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="cf1a7-167">По возможности поставщик удаленного транспорта должен отменить все операции, которые связаны с загрузкой headers.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="cf1a7-168">Для этого поставщик транспорта должен установить следующие значения свойств в строке состояния объекта для логотипа:</span><span class="sxs-lookup"><span data-stu-id="cf1a7-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="cf1a7-169">Очищайте биты STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE в свойстве **PR_STATUS_CODE** ([PidTagStatusCode),](pidtagstatuscode-canonical-property.md)чтобы сообщить пуле MAPI, что необходимо остановить процесс очистки входящих данных для этого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="cf1a7-170">За установите STATUS_OFFLINE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cf1a7-171">**Задайте PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk) в](pidtagremotevalidateok-canonical-property.md)true.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="cf1a7-172">Установите **для PR_STATUS_STRING** [(PidTagStatusString)](pidtagstatusstring-canonical-property.md)строку, которая указывает пользователю состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="cf1a7-173">Возврат S_OK.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-173">Return S_OK.</span></span> <span data-ttu-id="cf1a7-174">Однако если не удается отменить операцию, **ValidateState** должен вернуть MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="cf1a7-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="cf1a7-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="cf1a7-176">Поставщик удаленного транспорта никогда не должен устанавливать подключение к общему ресурсу (например, модему или COM-порту) вне контекста взаимодействия mapI spooler-transport, задействованного в методе [IXPLogon::FlushQueues.](ixplogon-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="cf1a7-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="cf1a7-177">Если **проверка ValidateState** вызвана с этим флагом, ваш поставщик транспорта должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="cf1a7-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="cf1a7-178">Установите внутренний флаг состояния, чтобы указать, что удаленное подключение необходимо установить при методе **IXPLogon::FlushQueues.**</span><span class="sxs-lookup"><span data-stu-id="cf1a7-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="cf1a7-179">Установите правильные значения в таблице состояния, чтобы пул mapI инициирует процесс очистки очереди.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="cf1a7-180">После очистки очередей отпустите общий ресурс.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="cf1a7-181">Очистка STATUS_OFFLINE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cf1a7-182">Возврат S_OK.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-182">Return S_OK.</span></span>
    
<span data-ttu-id="cf1a7-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="cf1a7-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="cf1a7-184">Поставщик удаленного транспорта должен освободить подключение к ресурсам системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="cf1a7-185">После этого он должен установить STATUS_OFFLINE в  свойстве PR_STATUS_CODE и вернуть S_OK.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="cf1a7-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cf1a7-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cf1a7-187">Поставщик удаленного транспорта должен обрабатывать удаленные сообщения и отправлять все отложенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="cf1a7-188">Для этого поставщик транспорта должен установить следующие значения свойств в строке состояния объекта для логотипа:</span><span class="sxs-lookup"><span data-stu-id="cf1a7-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="cf1a7-189">Установите **для PR_STATUS_STRING** строку, которая указывает пользователю состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="cf1a7-190">Установите STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cf1a7-191">Установите **для PR_REMOTE_VALIDATE_OK** свойства в строке состояния поставщика транспорта false.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="cf1a7-192">Если при вызвании **ValidateState** происходит другая операция (например,  загрузка MAPI_E_BUSY).</span><span class="sxs-lookup"><span data-stu-id="cf1a7-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="cf1a7-193">Выполните код для обработки REFRESH_XP_HEADER_CACHE флага, чтобы удовлетворить требования клиента Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="cf1a7-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cf1a7-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cf1a7-195">Поставщик удаленного транспорта должен получить все новые заглавные сообщения из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="cf1a7-196">Для этого поставщик транспорта должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="cf1a7-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="cf1a7-197">Установите **для PR_STATUS_STRING** строку, которая указывает пользователю состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="cf1a7-198">Установите STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cf1a7-199">Очистка STATUS_OFFLINE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cf1a7-200">За установите STATUS_ONLINE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="cf1a7-201">Установите **для PR_REMOTE_VALIDATE_OK** свойства в строке состояния поставщика транспорта false.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="cf1a7-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="cf1a7-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="cf1a7-203">Если у вашего поставщика транспорта есть какие-либо элементы пользовательского интерфейса для обработки заглавных сообщений (например, диалоговое окно с подтверждением загрузки сообщений), это диалоговое окно должно отобразиться.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="cf1a7-204">В **противном случае ValidateState** может вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="cf1a7-205">Если передаются какие-либо флаги, кроме этих, **ValidateState** должен возвращать MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="cf1a7-206">Вызовом клиента к поставщику транспорта часто является метод **IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="cf1a7-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="cf1a7-207">Во время обработки **ValidateState** поставщик транспорта не должен выполнять никаких действий, выделяющих системные ресурсы, например модем или COM-порт.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="cf1a7-208">Это происходит потому, что пулу MAPI иногда требуется очистить очереди для более чем одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="cf1a7-209">Однако клиент может в любое время вызвать метод **ValidateState** любого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="cf1a7-210">Если поставщик транспорта пытается выделить ресурс- источающий ресурс во время обработки **ValidateState,** ошибка может привести к конфликту с другим поставщиком транспорта, который пулер MAPI проинструктировали о очистке очередей.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="cf1a7-211">Если вы разрешаете выделение всех ресурсоемких ресурсов под руководством пула MAPI, можно избежать таких конфликтов.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="cf1a7-212">Ваш поставщик транспорта должен поддерживать **PR_REMOTE_VALIDATE_OK,** чтобы клиентские приложения могли определить, когда ваш поставщик транспорта занят или ожидает, пока пулер MAPI инициирует действие.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cf1a7-213">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cf1a7-213">Notes to callers</span></span>

<span data-ttu-id="cf1a7-214">Поскольку этот метод может привести к другим потенциально длительным вызовам, **ValidateState** может возвращать MAPI_E_BUSY, чтобы сообщить, что этот метод ожидает завершения другой операции.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="cf1a7-215">Необходимо дождаться завершения ожидающих операций, прежде чем пытаться выполнить другую задачу.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="cf1a7-216">Вы имеете самый полный контроль над вызовами объектов состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="cf1a7-217">В **ValidateState** можно передать один или несколько флагов, влияющих на работу поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="cf1a7-218">Например, флаг ABORT_XP_HEADER_OPERATION указывает, что пользователь отменил проверку.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="cf1a7-219">Поставщики транспорта могут отменить, вернуть MAPI_E_USER_CANCELED или продолжить.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="cf1a7-220">Вы можете установить флаг CONFIG_CHANGED в вызове для объекта состояния поставщика услуг или пула MAPI, чтобы указать, что параметр конфигурации был изменен.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="cf1a7-221">Вы можете использовать CONFIG_CHANGED для динамической перенастройки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="cf1a7-222">При CONFIG_CHANGED вызове объекта состояния поставщика услуг поставщик отвечает вызовом [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) чтобы оповещать пула MAPI об изменении.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="cf1a7-223">Когда вы CONFIG_CHANGED в вызове объекта состояния пула MAPI, пулер вызывает [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для каждого активного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="cf1a7-224">**AddressTypes** сообщает пулу MAPI о поддерживаемых типах адресов транспорта.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="cf1a7-225">Некоторые поставщики услуг также отображают индикатор хода выполнения, если ожидается, что проверка займет много времени.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="cf1a7-226">Отображение индикатора хода выполнения полезно, но не обязательно.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="cf1a7-227">Если установлен SUPPRESS_UI, никакие листы свойств конфигурации или диалоговые окна хода выполнения не отображаются.</span><span class="sxs-lookup"><span data-stu-id="cf1a7-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf1a7-228">См. также</span><span class="sxs-lookup"><span data-stu-id="cf1a7-228">See also</span></span>

- [<span data-ttu-id="cf1a7-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="cf1a7-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="cf1a7-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="cf1a7-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="cf1a7-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="cf1a7-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="cf1a7-232">Каноническое свойство PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="cf1a7-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="cf1a7-233">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="cf1a7-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="cf1a7-234">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="cf1a7-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="cf1a7-235">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="cf1a7-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="cf1a7-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cf1a7-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

