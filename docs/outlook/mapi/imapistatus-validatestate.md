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
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809118"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="14c89-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="14c89-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="14c89-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14c89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14c89-105">Проверяет состояние внешних информация, доступная для ресурсов MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="14c89-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="14c89-106">Этот метод поддерживается во всех объектах состояние.</span><span class="sxs-lookup"><span data-stu-id="14c89-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="14c89-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="14c89-107">Parameters</span></span>

<span data-ttu-id="14c89-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="14c89-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="14c89-109">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="14c89-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="14c89-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14c89-110">_ulFlags_</span></span>
  
> <span data-ttu-id="14c89-111">[in] Битовая маска флаги, который управляет проверки.</span><span class="sxs-lookup"><span data-stu-id="14c89-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="14c89-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="14c89-112">The following flags can be set:</span></span>
    
<span data-ttu-id="14c89-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="14c89-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="14c89-114">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне соответствующего.</span><span class="sxs-lookup"><span data-stu-id="14c89-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="14c89-115">Объект состояния имеет два варианта:</span><span class="sxs-lookup"><span data-stu-id="14c89-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="14c89-116">Продолжить работу на операции.</span><span class="sxs-lookup"><span data-stu-id="14c89-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="14c89-117">Отменить эту операцию и вернуться MAPI_E_USER_CANCELED.</span><span class="sxs-lookup"><span data-stu-id="14c89-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="14c89-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="14c89-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="14c89-119">Один или несколько свойств конфигурации объекта состояния изменен.</span><span class="sxs-lookup"><span data-stu-id="14c89-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="14c89-120">Клиенты можно задать этот флаг, чтобы разрешить диспетчер очереди MAPI для динамического исправления ошибок поставщика критические транспортировки.</span><span class="sxs-lookup"><span data-stu-id="14c89-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="14c89-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="14c89-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="14c89-122">Объект состояния следует выполнить подключение.</span><span class="sxs-lookup"><span data-stu-id="14c89-122">The status object should perform a connection.</span></span> <span data-ttu-id="14c89-123">При использовании с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE этот флаг подключения происходит без кэширования.</span><span class="sxs-lookup"><span data-stu-id="14c89-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="14c89-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="14c89-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="14c89-125">Состояние объекта следует выполнить операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="14c89-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="14c89-126">При использовании с флагом REFRESH_XP_HEADER_CACHE или PROCESS_XP_HEADER_CACHE этот флаг отключения происходит без кэширования.</span><span class="sxs-lookup"><span data-stu-id="14c89-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="14c89-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="14c89-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="14c89-128">Будут обрабатываться записей в таблице кэша заголовок, необходимо загрузить все сообщения, помеченные с флагом MSGSTATUS_REMOTE_DOWNLOAD и все сообщения, помеченные с флагом MSGSTATUS_REMOTE_DELETE подлежащий удалению.</span><span class="sxs-lookup"><span data-stu-id="14c89-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="14c89-129">Необходимо переместить сообщения, для которых MSGSTATUS_REMOTE_DOWNLOAD и задать MSGSTATUS_REMOTE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="14c89-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="14c89-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="14c89-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="14c89-131">Для поставщика транспорта удаленного необходимо загрузить новый список заголовков сообщений и все флаги, пометить состояние сообщения должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="14c89-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="14c89-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="14c89-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="14c89-133">Запрещает отображение пользовательского интерфейса в рамках операции объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="14c89-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14c89-134">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="14c89-134">Return value</span></span>

<span data-ttu-id="14c89-135">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="14c89-135">S_OK</span></span> 
  
> <span data-ttu-id="14c89-136">Проверка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="14c89-136">The validation was successful.</span></span>
    
<span data-ttu-id="14c89-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="14c89-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="14c89-138">Другой операции находится в стадии разработки; должны для выполнения или она должна быть остановлена, до инициализации этой операции.</span><span class="sxs-lookup"><span data-stu-id="14c89-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="14c89-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="14c89-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="14c89-140">Состояние объекта не поддерживает метод проверки, что указывает на отсутствие флага STATUS_VALIDATE_STATE в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="14c89-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="14c89-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="14c89-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="14c89-142">Пользователь отменил операции проверки, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="14c89-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="14c89-143">Это значение возвращается только поставщиков удаленных транспорта.</span><span class="sxs-lookup"><span data-stu-id="14c89-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="14c89-144">Замечания</span><span class="sxs-lookup"><span data-stu-id="14c89-144">Remarks</span></span>

<span data-ttu-id="14c89-145">Метод **IMAPIStatus::ValidateState** проверяет состояние ресурса, связанного с объектом состояния.</span><span class="sxs-lookup"><span data-stu-id="14c89-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="14c89-146">**ValidateState** — это единственный метод в интерфейсе [IMAPIStatus](imapistatusimapiprop.md) , необходимое для всех объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="14c89-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="14c89-147">Точное поведение этого метода зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="14c89-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="14c89-148">В следующей таблице описаны реализации каждого из различных типов объектов состояния.</span><span class="sxs-lookup"><span data-stu-id="14c89-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="14c89-149">**Состояние объекта**</span><span class="sxs-lookup"><span data-stu-id="14c89-149">**Status object**</span></span>|<span data-ttu-id="14c89-150">ValidateState ** реализации **</span><span class="sxs-lookup"><span data-stu-id="14c89-150">****ValidateState** implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14c89-151">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="14c89-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="14c89-152">Проверяет состояние все ресурсы, которые поставщиков услуг текущего активного и сама подсистема владельцем.</span><span class="sxs-lookup"><span data-stu-id="14c89-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="14c89-153">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="14c89-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="14c89-154">Входит в систему всех поставщиков транспорта, независимо от того, является ли уже входе в систему.</span><span class="sxs-lookup"><span data-stu-id="14c89-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="14c89-155">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="14c89-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="14c89-156">Проверяет, находятся в записях его раздела профиля.</span><span class="sxs-lookup"><span data-stu-id="14c89-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="14c89-157">Поставщик услуг</span><span class="sxs-lookup"><span data-stu-id="14c89-157">Service provider</span></span>  <br/> |<span data-ttu-id="14c89-158">Реализация зависит от типа поставщика и флаги, задавать в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="14c89-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="14c89-159">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="14c89-159">Notes to implementers</span></span>

<span data-ttu-id="14c89-160">Удаленные клиентские приложения вызовите метод **ValidateState** для запуска удаленного обработки для различных действий.</span><span class="sxs-lookup"><span data-stu-id="14c89-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="14c89-161">Этот метод используется в основном для установки состояния битов для взаимодействия с диспетчер очереди MAPI, а не фактически операцию.</span><span class="sxs-lookup"><span data-stu-id="14c89-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="14c89-162">Как правило поставщика транспорта устанавливает флаги в строке ее состояния, которые указывают диспетчер очереди MAPI, что действия необходимо быть инициирован для выполнения запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="14c89-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="14c89-163">В этой модели взаимодействия клиентов транспорта очереди действия, требуемой клиентом является асинхронным, в **ValidateState** возвращает до завершения запрошенного действия.</span><span class="sxs-lookup"><span data-stu-id="14c89-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="14c89-164">Тем не менее может быть синхронного действия, не используя обязательно системы обмена сообщениями или которые включают транспорта интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14c89-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="14c89-165">Клиентское приложение передает Битовая маска следующие флажки, чтобы определить, какие действия, поставщика транспорта удаленного должен выполнять.</span><span class="sxs-lookup"><span data-stu-id="14c89-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="14c89-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="14c89-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="14c89-167">Если это возможно поставщика транспорта удаленного должен отменить любые операций на загрузку заголовков.</span><span class="sxs-lookup"><span data-stu-id="14c89-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="14c89-168">Для этого поставщика транспорта необходимо присвоить следующие значения свойств в строке состояния объект вход в систему:</span><span class="sxs-lookup"><span data-stu-id="14c89-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="14c89-169">Снимите флажок STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE бит в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)), чтобы сообщить диспетчер очереди MAPI для остановки входящих процесс очистки для данного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="14c89-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="14c89-170">Задайте STATUS_OFFLINE бит в свойстве **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="14c89-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="14c89-171">Присвойте свойству **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="14c89-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="14c89-172">Присвойте свойству **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) к типу string, указывающее состояние поставщика транспорта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="14c89-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="14c89-173">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="14c89-173">Return S_OK.</span></span> <span data-ttu-id="14c89-174">Тем не менее если не удается отменить эту операцию в процессе выполнения, **ValidateState** должен возвращать MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="14c89-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="14c89-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="14c89-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="14c89-176">Поставщик удаленного транспорта никогда не следует установить подключение к общему ресурсу (например, модем или COM-порт) вне контекста взаимодействия очереди транспорта MAPI, участвующих в метод [IXPLogon::FlushQueues](ixplogon-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="14c89-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="14c89-177">Если **ValidateState** вызван с этот флаг, поставщика транспорта должен выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="14c89-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="14c89-178">Задайте флаг внутреннего состояния, чтобы указать, что при вызове метода **IXPLogon::FlushQueues** должно быть установлено подключение к удаленному.</span><span class="sxs-lookup"><span data-stu-id="14c89-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="14c89-179">Задайте правильные значения в таблице состояния, чтобы вызвать диспетчер очереди MAPI начать процесс очистки очереди.</span><span class="sxs-lookup"><span data-stu-id="14c89-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="14c89-180">После завершения очистки очередей release общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="14c89-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="14c89-181">Снимите флажок STATUS_OFFLINE бит в свойстве **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="14c89-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="14c89-182">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="14c89-182">Return S_OK.</span></span>
    
<span data-ttu-id="14c89-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="14c89-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="14c89-184">Поставщик удаленного транспорта освобождать его подключения к ресурсов системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="14c89-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="14c89-185">После этого, его следует установить бит STATUS_OFFLINE в свойстве **PR_STATUS_CODE** и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="14c89-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="14c89-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="14c89-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="14c89-187">Поставщик удаленного транспорта следует обработки удаленных сообщений и отправить все сообщения, которые были отложены.</span><span class="sxs-lookup"><span data-stu-id="14c89-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="14c89-188">Для этого поставщика транспорта необходимо присвоить следующие значения свойств в строке состояния объект вход в систему:</span><span class="sxs-lookup"><span data-stu-id="14c89-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="14c89-189">Присвойте свойству **PR_STATUS_STRING** к типу string, указывающее состояние поставщика транспорта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="14c89-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="14c89-190">Установка двоичных файлов STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE в свойстве **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="14c89-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="14c89-191">Присвойте свойству **PR_REMOTE_VALIDATE_OK** в строке состояния поставщика транспорта значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="14c89-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="14c89-192">Если другой операции находится в стадии разработки (например, загрузку заголовков) при вызове **ValidateState** **ValidateState** должна вернуть MAPI_E_BUSY.</span><span class="sxs-lookup"><span data-stu-id="14c89-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="14c89-193">Выполнение кода для обработки флаг REFRESH_XP_HEADER_CACHE, а также соблюдения требований клиента Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="14c89-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="14c89-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="14c89-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="14c89-195">Поставщик удаленного транспорта должны получить любые новые заголовки сообщений из систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="14c89-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="14c89-196">Для этого поставщика транспорта необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="14c89-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="14c89-197">Присвойте свойству **PR_STATUS_STRING** к типу string, указывающее состояние поставщика транспорта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="14c89-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="14c89-198">Установка двоичных файлов STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE в свойстве **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="14c89-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="14c89-199">Снимите флажок STATUS_OFFLINE бит в свойстве **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="14c89-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="14c89-200">Задайте STATUS_ONLINE бит в свойстве **PR_STATUS_CODE** .</span><span class="sxs-lookup"><span data-stu-id="14c89-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="14c89-201">Присвойте свойству **PR_REMOTE_VALIDATE_OK** в строке состояния поставщика транспорта значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="14c89-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="14c89-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="14c89-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="14c89-203">Если ваш поставщик транспорта любой части пользовательского интерфейса для обработки заголовков сообщений (например, диалоговое окно, которое подтверждает загрузку сообщений), окно должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="14c89-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="14c89-204">В противном случае **ValidateState** может вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="14c89-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="14c89-205">Если переданную флаги других **ValidateState** должен возвращать MAPI_E_UNKNOWN_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="14c89-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="14c89-206">Вызов клиента для поставщика транспорта часто будут в метод **IMAPIStatus::ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="14c89-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="14c89-207">Во время обработки **ValidateState**, поставщика транспорта не следует выполнять любые действия, которые выделение нехватки системных ресурсов, таких как модем или COM-порт.</span><span class="sxs-lookup"><span data-stu-id="14c89-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="14c89-208">Это так, как диспетчер очереди MAPI в некоторых случаях требуется очистить очередей на более одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="14c89-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="14c89-209">Тем не менее клиент может вызывать метод **ValidateState** любого поставщика транспорта в любое время.</span><span class="sxs-lookup"><span data-stu-id="14c89-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="14c89-210">Если ваш поставщик транспорта попытается выделить нехватки ресурсов во время обработки **ValidateState**, ошибка может привести к из-за конфликта с другого поставщика транспорта, предписывает диспетчер очереди MAPI для очистки очереди.</span><span class="sxs-lookup"><span data-stu-id="14c89-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="14c89-211">Если вы включили все выделений нехватки ресурсов будет выполнена под руководством диспетчер очереди MAPI, можно избежать подобных конфликтов.</span><span class="sxs-lookup"><span data-stu-id="14c89-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="14c89-212">Поставщика транспорта должны поддерживать свойство **PR_REMOTE_VALIDATE_OK** , поэтому клиентских приложений можно определить, когда поставщика транспорта «занят» или ожидая очереди MAPI для инициации действия.</span><span class="sxs-lookup"><span data-stu-id="14c89-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="14c89-213">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="14c89-213">Notes to callers</span></span>

<span data-ttu-id="14c89-214">Так как этот метод можно вызывать другие потенциально длительных вызовов, **ValidateState** может вернуть MAPI_E_BUSY, информирующее о том, что этот метод ожидает другой операции.</span><span class="sxs-lookup"><span data-stu-id="14c89-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="14c89-215">Должен ожидать до завершения операции ожидающие прежде чем другой задачи.</span><span class="sxs-lookup"><span data-stu-id="14c89-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="14c89-216">У вас есть полный контроль над звонков для передачи объектов состояние поставщика.</span><span class="sxs-lookup"><span data-stu-id="14c89-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="14c89-217">Один или несколько флагов можно передать **ValidateState** , которые влияют на операции поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="14c89-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="14c89-218">Например флаг ABORT_XP_HEADER_OPERATION указывает, что пользователь отменил проверки.</span><span class="sxs-lookup"><span data-stu-id="14c89-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="14c89-219">Поставщики транспорта можно указать, кто прервать, возвращая MAPI_E_USER_CANCELED, или по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="14c89-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="14c89-220">Флаг CONFIG_CHANGED можно задать на вызов объекта состояние поставщика службы или диспетчер очереди MAPI для указания изменения параметров конфигурации.</span><span class="sxs-lookup"><span data-stu-id="14c89-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="14c89-221">CONFIG_CHANGED можно использовать для динамического назначения поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="14c89-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="14c89-222">При установке CONFIG_CHANGED на вызов объекта состояние поставщика услуг поставщика отвечает вызов [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) для оповещения диспетчер очереди MAPI изменения.</span><span class="sxs-lookup"><span data-stu-id="14c89-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="14c89-223">При установке CONFIG_CHANGED на объект состояния очереди MAPI очереди вызывает [IXPLogon::AddressTypes](ixplogon-addresstypes.md) для каждого поставщика транспорта активный.</span><span class="sxs-lookup"><span data-stu-id="14c89-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="14c89-224">**AddressTypes** информирует диспетчер очереди MAPI типов поддерживаемых адресов транспорта.</span><span class="sxs-lookup"><span data-stu-id="14c89-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="14c89-225">Некоторых поставщиков услуг также отобразить индикатор выполнения, если проверка уйти много времени.</span><span class="sxs-lookup"><span data-stu-id="14c89-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="14c89-226">Отображение индикатор выполнения полезным, но не требуется.</span><span class="sxs-lookup"><span data-stu-id="14c89-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="14c89-227">Если для флага SUPPRESS_UI, ни одно из свойств конфигурации или диалоговые окна хода выполнения могут быть отображены.</span><span class="sxs-lookup"><span data-stu-id="14c89-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14c89-228">См. также</span><span class="sxs-lookup"><span data-stu-id="14c89-228">See also</span></span>

- [<span data-ttu-id="14c89-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="14c89-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="14c89-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="14c89-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="14c89-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="14c89-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="14c89-232">Каноническое свойство PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="14c89-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="14c89-233">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="14c89-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="14c89-234">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="14c89-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="14c89-235">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="14c89-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="14c89-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="14c89-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

