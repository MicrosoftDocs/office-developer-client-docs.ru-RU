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
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="bcd15-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="bcd15-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="bcd15-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bcd15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bcd15-105">Подтверждает сведения о внешнем состоянии, доступные для ресурса MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="bcd15-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="bcd15-106">Этот метод поддерживается во всех объектах состояния.</span><span class="sxs-lookup"><span data-stu-id="bcd15-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bcd15-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="bcd15-107">Parameters</span></span>

<span data-ttu-id="bcd15-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bcd15-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="bcd15-109">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="bcd15-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="bcd15-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bcd15-110">_ulFlags_</span></span>
  
> <span data-ttu-id="bcd15-111">[in] Битмашка флагов, контролирующая проверку.</span><span class="sxs-lookup"><span data-stu-id="bcd15-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="bcd15-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="bcd15-112">The following flags can be set:</span></span>
    
<span data-ttu-id="bcd15-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="bcd15-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="bcd15-114">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в соответствующем диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="bcd15-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="bcd15-115">Объект состояния имеет два варианта:</span><span class="sxs-lookup"><span data-stu-id="bcd15-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="bcd15-116">Продолжить работу над операцией.</span><span class="sxs-lookup"><span data-stu-id="bcd15-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="bcd15-117">Остановите операцию и MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="bcd15-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="bcd15-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="bcd15-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="bcd15-119">Изменено одно или несколько свойств конфигурации объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="bcd15-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="bcd15-120">Клиенты могут установить этот флаг, чтобы разрешить пульперу MAPI динамически исправлять критически важные сбои поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="bcd15-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="bcd15-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="bcd15-122">Объект состояния должен выполнять подключение.</span><span class="sxs-lookup"><span data-stu-id="bcd15-122">The status object should perform a connection.</span></span> <span data-ttu-id="bcd15-123">Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE флагом, подключение происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="bcd15-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="bcd15-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="bcd15-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="bcd15-125">Объект состояния должен выполнять операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="bcd15-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="bcd15-126">Если этот флаг используется с REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE флагом, отключение происходит без кэшинга.</span><span class="sxs-lookup"><span data-stu-id="bcd15-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="bcd15-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bcd15-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bcd15-128">Записи в таблице кэша загона должны обрабатываться, все сообщения с флагом MSGSTATUS_REMOTE_DOWNLOAD должны быть загружены, а все сообщения, помеченные флагом MSGSTATUS_REMOTE_DELETE, должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="bcd15-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="bcd15-129">Сообщения с набором MSGSTATUS_REMOTE_DOWNLOAD и MSGSTATUS_REMOTE_DELETE должны быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="bcd15-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="bcd15-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bcd15-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bcd15-131">Для поставщика удаленного транспорта необходимо загрузить новый список заглавных сообщений и очистить все флаги, помеченные состоянием сообщения.</span><span class="sxs-lookup"><span data-stu-id="bcd15-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="bcd15-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="bcd15-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="bcd15-133">Предотвращает отображение объекта состояния пользовательского интерфейса в рамках операции.</span><span class="sxs-lookup"><span data-stu-id="bcd15-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bcd15-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcd15-134">Return value</span></span>

<span data-ttu-id="bcd15-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcd15-135">S_OK</span></span> 
  
> <span data-ttu-id="bcd15-136">Проверка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="bcd15-136">The validation was successful.</span></span>
    
<span data-ttu-id="bcd15-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="bcd15-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="bcd15-138">В настоящее время продолжается другая операция; это должно быть разрешено для завершения или его следует остановить, прежде чем эта операция будет начата.</span><span class="sxs-lookup"><span data-stu-id="bcd15-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="bcd15-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bcd15-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bcd15-140">Объект состояния не поддерживает метод проверки, как указывает отсутствие флага STATUS_VALIDATE_STATE в  свойстве[PR_RESOURCE_METHODS (PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bcd15-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="bcd15-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bcd15-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="bcd15-142">Пользователь отменил операцию проверки, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="bcd15-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="bcd15-143">Это значение возвращается только удаленными поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bcd15-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="bcd15-144">Remarks</span></span>

<span data-ttu-id="bcd15-145">Метод **IMAPIStatus::ValidateState** проверяет состояние ресурса, связанного с объектом состояния.</span><span class="sxs-lookup"><span data-stu-id="bcd15-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="bcd15-146">**ValidateState** — это единственный метод в [интерфейсе IMAPIStatus,](imapistatusimapiprop.md) который необходим для всех объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="bcd15-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="bcd15-147">Точное поведение этого метода зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="bcd15-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="bcd15-148">В следующей таблице описывается реализация каждого из различных типов объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="bcd15-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="bcd15-149">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="bcd15-149">**Status object**</span></span>|<span data-ttu-id="bcd15-150">Реализация ValidateState\*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="bcd15-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="bcd15-151">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="bcd15-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="bcd15-152">Проверяет состояние всех ресурсов, которые в настоящее время принадлежат действующим поставщикам услуг и самой подсистеме.</span><span class="sxs-lookup"><span data-stu-id="bcd15-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="bcd15-153">Шпалер MAPI</span><span class="sxs-lookup"><span data-stu-id="bcd15-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="bcd15-154">Выполняет логотип всех поставщиков транспорта независимо от того, вошли ли они в систему.</span><span class="sxs-lookup"><span data-stu-id="bcd15-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="bcd15-155">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="bcd15-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="bcd15-156">Проверяет записи в разделе профилей.</span><span class="sxs-lookup"><span data-stu-id="bcd15-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="bcd15-157">Поставщик услуг</span><span class="sxs-lookup"><span data-stu-id="bcd15-157">Service provider</span></span>  <br/> |<span data-ttu-id="bcd15-158">Реализация зависит от типа поставщика и флагов, заданных в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="bcd15-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="bcd15-159">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bcd15-159">Notes to implementers</span></span>

<span data-ttu-id="bcd15-160">Удаленные клиентские приложения звонят **методу ValidateState,** чтобы приступить к удаленной обработке для различных действий.</span><span class="sxs-lookup"><span data-stu-id="bcd15-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="bcd15-161">Этот метод существует в первую очередь для набора битов состояния для связи со шпалером MAPI вместо того, чтобы фактически делать какие-либо работы.</span><span class="sxs-lookup"><span data-stu-id="bcd15-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="bcd15-162">Обычно поставщик транспорта задает флажки в строке состояния, которые указывают на то, какие действия необходимо инициировать для выполнения запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="bcd15-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="bcd15-163">В этой модели взаимодействия клиента с транспортом и пулером действия, запрашиваемая клиентом, являются асинхронными, так как **ПроверкаState** возвращается до завершения запрашиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="bcd15-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="bcd15-164">Однако действия, которые не обязательно связаны с системой обмена сообщениями или связаны с транспортным интерфейсом, могут быть синхронными.</span><span class="sxs-lookup"><span data-stu-id="bcd15-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="bcd15-165">Клиентская заявка передается в битмаске следующих флагов, чтобы указать, какие действия должен принять поставщик удаленного транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="bcd15-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="bcd15-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="bcd15-167">Если это возможно, поставщик удаленного транспорта должен отменить все операции, которые связаны с загрузкой загодеров.</span><span class="sxs-lookup"><span data-stu-id="bcd15-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="bcd15-168">Для этого поставщик транспорта должен задать следующие значения свойств в строке состояния объекта logon:</span><span class="sxs-lookup"><span data-stu-id="bcd15-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="bcd15-169">Очистить STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE биты в **свойстве PR_STATUS_CODE** [(PidTagStatusCode),](pidtagstatuscode-canonical-property.md)чтобы сообщить шпалеру MAPI остановить процесс входящих флеш-данных для этого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="bcd15-170">Установите STATUS_OFFLINE в **свойстве PR_STATUS_CODE.**</span><span class="sxs-lookup"><span data-stu-id="bcd15-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bcd15-171">Установите **свойство PR_REMOTE_VALIDATE_OK** [(PidTagRemoteValidateOk)](pidtagremotevalidateok-canonical-property.md)в true.</span><span class="sxs-lookup"><span data-stu-id="bcd15-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="bcd15-172">Установите **свойство PR_STATUS_STRING** [(PidTagStatusString)](pidtagstatusstring-canonical-property.md)строке, которая указывает пользователю состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="bcd15-173">Возвращение S_OK.</span><span class="sxs-lookup"><span data-stu-id="bcd15-173">Return S_OK.</span></span> <span data-ttu-id="bcd15-174">Однако, если операция не может быть отменена, **ПроверкаState** должна вернуться MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="bcd15-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="bcd15-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="bcd15-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="bcd15-176">Поставщик удаленного транспорта никогда не должен устанавливать подключение к общему ресурсу (например, к модему или порту COM) вне контекста взаимодействия пуловер-транспорта MAPI, задействованного в методе [IXPLogon::FlushQueues.](ixplogon-flushqueues.md)</span><span class="sxs-lookup"><span data-stu-id="bcd15-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="bcd15-177">Если с этим флагом **вызвана ПроверкаState,** поставщик транспорта должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="bcd15-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="bcd15-178">Установите внутренний флаг состояния, чтобы указать, что удаленное подключение должно быть установлено при призыве метода **IXPLogon::FlushQueues.**</span><span class="sxs-lookup"><span data-stu-id="bcd15-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="bcd15-179">Установите правильные значения в таблице состояния, чтобы вызвать spooler MAPI, чтобы инициировать процесс очистки очереди.</span><span class="sxs-lookup"><span data-stu-id="bcd15-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="bcd15-180">После завершения очистки очередей отпустите общий ресурс.</span><span class="sxs-lookup"><span data-stu-id="bcd15-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="bcd15-181">Очистить STATUS_OFFLINE в **свойстве PR_STATUS_CODE.**</span><span class="sxs-lookup"><span data-stu-id="bcd15-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bcd15-182">Возвращение S_OK.</span><span class="sxs-lookup"><span data-stu-id="bcd15-182">Return S_OK.</span></span>
    
<span data-ttu-id="bcd15-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="bcd15-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="bcd15-184">Поставщик удаленного транспорта должен освободить подключение к ресурсам системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bcd15-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="bcd15-185">После этого следует установить STATUS_OFFLINE в свойстве  PR_STATUS_CODE и S_OK.</span><span class="sxs-lookup"><span data-stu-id="bcd15-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="bcd15-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bcd15-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bcd15-187">Поставщик удаленного транспорта должен обрабатывать удаленные сообщения и отправлять отложенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="bcd15-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="bcd15-188">Для этого поставщик транспорта должен задать следующие значения свойств в строке состояния объекта logon:</span><span class="sxs-lookup"><span data-stu-id="bcd15-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="bcd15-189">Установите **свойство PR_STATUS_STRING** строку, которая указывает пользователю состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="bcd15-190">Установите STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="bcd15-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bcd15-191">Установите **свойство PR_REMOTE_VALIDATE_OK** в строке состояния поставщика транспорта false.</span><span class="sxs-lookup"><span data-stu-id="bcd15-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="bcd15-192">Если еще одна операция (например, загрузка заготавлителей) при назважении **ValidateState, ПроверкаState** должна MAPI_E_BUSY. </span><span class="sxs-lookup"><span data-stu-id="bcd15-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="bcd15-193">Выполните код для обработки REFRESH_XP_HEADER_CACHE флага, а также для удовлетворения требований клиента Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="bcd15-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="bcd15-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="bcd15-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="bcd15-195">Поставщик удаленного транспорта должен получать новые заглавные сообщения из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bcd15-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="bcd15-196">Для этого поставщик транспорта должен сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="bcd15-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="bcd15-197">Установите **свойство PR_STATUS_STRING** строку, которая указывает пользователю состояние поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="bcd15-198">Установите STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE в **свойстве** PR_STATUS_CODE.</span><span class="sxs-lookup"><span data-stu-id="bcd15-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bcd15-199">Очистить STATUS_OFFLINE в **свойстве PR_STATUS_CODE.**</span><span class="sxs-lookup"><span data-stu-id="bcd15-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bcd15-200">Установите STATUS_ONLINE в **свойстве PR_STATUS_CODE.**</span><span class="sxs-lookup"><span data-stu-id="bcd15-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="bcd15-201">Установите **свойство PR_REMOTE_VALIDATE_OK** в строке состояния поставщика транспорта false.</span><span class="sxs-lookup"><span data-stu-id="bcd15-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="bcd15-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="bcd15-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="bcd15-203">Если у поставщика транспорта есть какие-либо части пользовательского интерфейса для обработки загонщиков сообщений (например, диалоговое окно, которое подтверждает загрузку сообщений), диалоговое окно должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="bcd15-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="bcd15-204">В противном **случае ValidateState** может MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="bcd15-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="bcd15-205">Если какие-либо флаги, кроме этих, передаются, **ПроверкаState** должна MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="bcd15-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="bcd15-206">Часто клиент звонит поставщику транспорта по методу **IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="bcd15-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="bcd15-207">Во время обработки **ValidateState** поставщик транспорта не должен выполнять действия, выделяющие ограниченные системные ресурсы, такие как модем или порт COM.</span><span class="sxs-lookup"><span data-stu-id="bcd15-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="bcd15-208">Это происходит из-за того, что для пульпера MAPI иногда требуется смыть очереди на несколько поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="bcd15-209">Однако клиент может вызвать метод **ValidateState** любого поставщика транспорта в любое время.</span><span class="sxs-lookup"><span data-stu-id="bcd15-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="bcd15-210">Если поставщик транспорта пытается выделить ограниченный ресурс во время обработки **ValidateState,** ошибка может привести к конфликту с другим поставщиком транспорта, который шпалер MAPI поручил смыть очереди.</span><span class="sxs-lookup"><span data-stu-id="bcd15-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="bcd15-211">Если вы разрешаете все ограниченные выделения ресурсов происходить под руководством пулера MAPI, можно избежать таких конфликтов.</span><span class="sxs-lookup"><span data-stu-id="bcd15-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="bcd15-212">Поставщик транспорта должен поддерживать свойство **PR_REMOTE_VALIDATE_OK,** чтобы клиентские приложения могли обнаруживать, когда поставщик транспорта занят или ждет, когда пуллер MAPI начнет действие.</span><span class="sxs-lookup"><span data-stu-id="bcd15-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bcd15-213">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bcd15-213">Notes to callers</span></span>

<span data-ttu-id="bcd15-214">Поскольку этот метод может вызвать другие потенциально длительные вызовы, **ValidateState** может вернуться MAPI_E_BUSY, чтобы сообщить вам, что этот метод ожидает завершения другой операции.</span><span class="sxs-lookup"><span data-stu-id="bcd15-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="bcd15-215">Прежде чем пытаться выполнить другую задачу, необходимо дождаться завершения ожидаемой операции.</span><span class="sxs-lookup"><span data-stu-id="bcd15-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="bcd15-216">Вы имеете самый полный контроль над вызовами объектов состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="bcd15-217">Вы можете передать один или несколько флагов **в ValidateState,** которые влияют на работу поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="bcd15-218">Например, флаг ABORT_XP_HEADER_OPERATION указывает, что пользователь отменил проверку.</span><span class="sxs-lookup"><span data-stu-id="bcd15-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="bcd15-219">Поставщики транспорта могут решить прервать, MAPI_E_USER_CANCELED или продолжить.</span><span class="sxs-lookup"><span data-stu-id="bcd15-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="bcd15-220">Вы можете CONFIG_CHANGED флаг на вызов либо к объекту состояния поставщика услуг, либо к шпалеру MAPI, чтобы указать, что параметр конфигурации изменен.</span><span class="sxs-lookup"><span data-stu-id="bcd15-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="bcd15-221">Вы можете использовать CONFIG_CHANGED для динамической перенастройки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="bcd15-222">При CONFIG_CHANGED вызове объекта состояния поставщика услуг поставщик отвечает вызовом [на IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) чтобы предупредить шпалер MAPI об изменении.</span><span class="sxs-lookup"><span data-stu-id="bcd15-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="bcd15-223">Когда вы CONFIG_CHANGED на вызов объекта состояния пульпера MAPI, шпалер вызывает [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для каждого активного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="bcd15-224">**AddressTypes** информирует шпалер MAPI о поддерживаемых типах адресов транспорта.</span><span class="sxs-lookup"><span data-stu-id="bcd15-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="bcd15-225">Некоторые поставщики услуг также отображают индикатор прогресса, если проверка, как ожидается, займет много времени.</span><span class="sxs-lookup"><span data-stu-id="bcd15-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="bcd15-226">Отображение индикатора прогресса полезно, но не обязательно.</span><span class="sxs-lookup"><span data-stu-id="bcd15-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="bcd15-227">Когда заданная SUPPRESS_UI, ни один из листов свойств конфигурации или диалоговых окне хода не может отображаться.</span><span class="sxs-lookup"><span data-stu-id="bcd15-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bcd15-228">См. также</span><span class="sxs-lookup"><span data-stu-id="bcd15-228">See also</span></span>

- [<span data-ttu-id="bcd15-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="bcd15-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="bcd15-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="bcd15-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="bcd15-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="bcd15-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="bcd15-232">Каноническое свойство PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="bcd15-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="bcd15-233">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="bcd15-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="bcd15-234">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="bcd15-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="bcd15-235">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="bcd15-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="bcd15-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bcd15-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

