---
title: Имапистатусвалидатестате
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331551"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="916ad-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="916ad-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="916ad-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="916ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="916ad-105">Проверяет внешние сведения о состоянии, доступные для ресурса MAPI или поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="916ad-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="916ad-106">Этот метод поддерживается во всех объектах Status.</span><span class="sxs-lookup"><span data-stu-id="916ad-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="916ad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="916ad-107">Parameters</span></span>

<span data-ttu-id="916ad-108">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="916ad-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="916ad-109">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="916ad-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="916ad-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="916ad-110">_ulFlags_</span></span>
  
> <span data-ttu-id="916ad-111">возврата Битовая маска флагов, управляющих проверкой.</span><span class="sxs-lookup"><span data-stu-id="916ad-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="916ad-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="916ad-112">The following flags can be set:</span></span>
    
<span data-ttu-id="916ad-113">АБОРТ_КСП_ХЕАДЕР_ОПЕРАТИОН</span><span class="sxs-lookup"><span data-stu-id="916ad-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="916ad-114">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в соответствующем диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="916ad-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="916ad-115">Объект Status имеет два параметра:</span><span class="sxs-lookup"><span data-stu-id="916ad-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="916ad-116">Продолжайте работу над операцией.</span><span class="sxs-lookup"><span data-stu-id="916ad-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="916ad-117">Остановите операцию и возвратите МАПИ_Е_УСЕР_КАНЦЕЛЕД.</span><span class="sxs-lookup"><span data-stu-id="916ad-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="916ad-118">КОНФИГ_ЧАНЖЕД</span><span class="sxs-lookup"><span data-stu-id="916ad-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="916ad-119">Изменилось одно или несколько свойств конфигурации объекта Status.</span><span class="sxs-lookup"><span data-stu-id="916ad-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="916ad-120">Клиенты могут установить этот флаг, чтобы диспетчер очереди MAPI мог динамически устранять критические сбои поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="916ad-121">ФОРЦЕ_КСП_КОННЕКТ</span><span class="sxs-lookup"><span data-stu-id="916ad-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="916ad-122">Объект Status должен выполнить подключение.</span><span class="sxs-lookup"><span data-stu-id="916ad-122">The status object should perform a connection.</span></span> <span data-ttu-id="916ad-123">Если этот флаг используется с флагом РЕФРЕШ_КСП_ХЕАДЕР_КАЧЕ или ПРОЦЕСС_КСП_ХЕАДЕР_КАЧЕ, подключение выполняется без кэширования.</span><span class="sxs-lookup"><span data-stu-id="916ad-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="916ad-124">ФОРЦЕ_КСП_ДИСКОННЕКТ</span><span class="sxs-lookup"><span data-stu-id="916ad-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="916ad-125">Объект Status должен выполнить операцию отключения.</span><span class="sxs-lookup"><span data-stu-id="916ad-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="916ad-126">Если этот флаг используется с флагом РЕФРЕШ_КСП_ХЕАДЕР_КАЧЕ или ПРОЦЕСС_КСП_ХЕАДЕР_КАЧЕ, отключение происходит без кэширования.</span><span class="sxs-lookup"><span data-stu-id="916ad-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="916ad-127">ПРОЦЕСС_КСП_ХЕАДЕР_КАЧЕ</span><span class="sxs-lookup"><span data-stu-id="916ad-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="916ad-128">Записи в таблице кэша заголовков должны быть обработаны, все сообщения, отмеченные флагом МСГСТАТУС_РЕМОТЕ_ДОВНЛОАД, будут скачаны, а все сообщения, помеченные флагом МСГСТАТУС_РЕМОТЕ_ДЕЛЕТЕ, должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="916ad-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="916ad-129">Сообщения с набором МСГСТАТУС_РЕМОТЕ_ДОВНЛОАД и МСГСТАТУС_РЕМОТЕ_ДЕЛЕТЕ должны быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="916ad-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="916ad-130">РЕФРЕШ_КСП_ХЕАДЕР_КАЧЕ</span><span class="sxs-lookup"><span data-stu-id="916ad-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="916ad-131">Для удаленного поставщика транспорта необходимо скачать новый список заголовков сообщений, а все флаги, помечающие состояние сообщения, следует очистить.</span><span class="sxs-lookup"><span data-stu-id="916ad-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="916ad-132">СУППРЕСС_УИ</span><span class="sxs-lookup"><span data-stu-id="916ad-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="916ad-133">Запрещает отображение в объекте status пользовательского интерфейса в рамках операции.</span><span class="sxs-lookup"><span data-stu-id="916ad-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="916ad-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="916ad-134">Return value</span></span>

<span data-ttu-id="916ad-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="916ad-135">S_OK</span></span> 
  
> <span data-ttu-id="916ad-136">Проверка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="916ad-136">The validation was successful.</span></span>
    
<span data-ttu-id="916ad-137">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="916ad-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="916ad-138">Выполняется другая операция; ее выполнение должно быть разрешено или остановлено до инициирования этой операции.</span><span class="sxs-lookup"><span data-stu-id="916ad-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="916ad-139">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="916ad-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="916ad-140">Объект Status не поддерживает метод проверки, как указано в отсутствие флага СТАТУС_ВАЛИДАТЕ_СТАТЕ в свойстве **пр_ресаурце_месодс** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="916ad-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="916ad-141">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="916ad-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="916ad-142">Пользователь отменил операцию проверки, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="916ad-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="916ad-143">Это значение возвращается только удаленными поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="916ad-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="916ad-144">Remarks</span></span>

<span data-ttu-id="916ad-145">Метод **имапистатус:: валидатестате** проверяет состояние ресурса, связанного с объектом Status.</span><span class="sxs-lookup"><span data-stu-id="916ad-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="916ad-146">**Валидатестате** — единственный метод в интерфейсе [имапистатус](imapistatusimapiprop.md) , необходимый для всех объектов Status.</span><span class="sxs-lookup"><span data-stu-id="916ad-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="916ad-147">Точное поведение этого метода зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="916ad-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="916ad-148">В следующей таблице описывается реализация каждого из различных типов объектов Status.</span><span class="sxs-lookup"><span data-stu-id="916ad-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="916ad-149">**Объект Status**</span><span class="sxs-lookup"><span data-stu-id="916ad-149">**Status object**</span></span>|<span data-ttu-id="916ad-150">Реализация Валидатестате \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="916ad-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="916ad-151">Подсистема MAPI</span><span class="sxs-lookup"><span data-stu-id="916ad-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="916ad-152">Проверяет состояние всех ресурсов, которыми владеет текущий активный поставщик услуг и сама подсистема.</span><span class="sxs-lookup"><span data-stu-id="916ad-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="916ad-153">Диспетчер очереди MAPI</span><span class="sxs-lookup"><span data-stu-id="916ad-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="916ad-154">Выполняет вход в систему для всех поставщиков транспорта независимо от того, были ли они уже зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="916ad-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="916ad-155">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="916ad-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="916ad-156">Проверяет записи в разделе профиля.</span><span class="sxs-lookup"><span data-stu-id="916ad-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="916ad-157">Поставщик услуг</span><span class="sxs-lookup"><span data-stu-id="916ad-157">Service provider</span></span>  <br/> |<span data-ttu-id="916ad-158">Реализация зависит от типа поставщика и флагов, заданные в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="916ad-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="916ad-159">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="916ad-159">Notes to implementers</span></span>

<span data-ttu-id="916ad-160">Удаленные клиентские приложения вызывают метод **валидатестате** , чтобы запустить удаленную обработку для различных действий.</span><span class="sxs-lookup"><span data-stu-id="916ad-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="916ad-161">Этот метод в основном существует для установки битов состояния для общения с диспетчером очереди MAPI, а не для фактического выполнения какой – либо работы.</span><span class="sxs-lookup"><span data-stu-id="916ad-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="916ad-162">Как правило, поставщик транспорта устанавливает флаги в строке состояния, указывающие на очередь MAPI, какие действия необходимо инициировать для выполнения запроса клиента.</span><span class="sxs-lookup"><span data-stu-id="916ad-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="916ad-163">В этой модели взаимодействия клиента с транспортным сервером действия, запрашиваемые клиентом, выполняются асинхронно, в то же **валидатестате** возвращаются до выполнения запрошенных действий.</span><span class="sxs-lookup"><span data-stu-id="916ad-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="916ad-164">Однако действия, которые не включают в себя базовую систему обмена сообщениями или которые используют интерфейс, связанный с транспортом, могут быть синхронными.</span><span class="sxs-lookup"><span data-stu-id="916ad-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="916ad-165">Клиентское приложение передает битовую маску следующих флагов, чтобы указать, какие действия должен выполнять удаленный поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="916ad-166">АБОРТ_КСП_ХЕАДЕР_ОПЕРАТИОН</span><span class="sxs-lookup"><span data-stu-id="916ad-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="916ad-167">Если это возможно, удаленный поставщик транспорта должен отменить все операции, которые включают загрузку заголовков.</span><span class="sxs-lookup"><span data-stu-id="916ad-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="916ad-168">Для этого поставщик транспорта должен задать следующие значения свойств в строке состояния объекта входа:</span><span class="sxs-lookup"><span data-stu-id="916ad-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="916ad-169">Очистите биты СТАТУС_ИНБАУНД_ЕНАБЛЕД и СТАТУС_ИНБАУНД_АКТИВЕ в свойстве **пр_статус_коде** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)), чтобы сообщить диспетчеру почтовых остановить входящий процесс очистки для этого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="916ad-170">Установите бит СТАТУС_ОФФЛИНЕ в свойстве \*\*пр_статус_коде\*\* .</span><span class="sxs-lookup"><span data-stu-id="916ad-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="916ad-171">ПриСвойте свойству **пр_ремоте_валидате_ок** ([PIDTAGREMOTEVALIDATEOK](pidtagremotevalidateok-canonical-property.md)) значение true.</span><span class="sxs-lookup"><span data-stu-id="916ad-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="916ad-172">Задайте в качестве значения свойства **пр_статус_стринг** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) строку, которая указывает состояние поставщика транспорта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="916ad-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="916ad-173">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="916ad-173">Return S_OK.</span></span> <span data-ttu-id="916ad-174">Однако если не удается отменить выполняемую операцию, **валидатестате** должен вернуть мапи_е_буси.</span><span class="sxs-lookup"><span data-stu-id="916ad-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="916ad-175">ФОРЦЕ_КСП_КОННЕКТ</span><span class="sxs-lookup"><span data-stu-id="916ad-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="916ad-176">Удаленный поставщик транспорта не должен устанавливать подключение к общему ресурсу (например, модем или COM-порт) за пределами контекста диалога MAPI-Transport, используемого в методе [иксплогон:: FlushQueues](ixplogon-flushqueues.md) .</span><span class="sxs-lookup"><span data-stu-id="916ad-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="916ad-177">Если **валидатестате** вызывается с этим флагом, ваш поставщик транспорта должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="916ad-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="916ad-178">Установите флаг внутреннего состояния, чтобы указать, что удаленное подключение должно быть установлено при вызове метода **иксплогон:: FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="916ad-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="916ad-179">Задайте правильные значения в таблице состояние, чтобы диспетчер очереди MAPI инициировал процесс очистки очереди.</span><span class="sxs-lookup"><span data-stu-id="916ad-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="916ad-180">После завершения очистки очередей Освободите общий ресурс.</span><span class="sxs-lookup"><span data-stu-id="916ad-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="916ad-181">Очистите бит СТАТУС_ОФФЛИНЕ в свойстве \*\*пр_статус_коде\*\* .</span><span class="sxs-lookup"><span data-stu-id="916ad-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="916ad-182">Возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="916ad-182">Return S_OK.</span></span>
    
<span data-ttu-id="916ad-183">ФОРЦЕ_КСП_ДИСКОННЕКТ</span><span class="sxs-lookup"><span data-stu-id="916ad-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="916ad-184">Удаленный поставщик транспорта должен освободить свое подключение к системным ресурсам системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="916ad-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="916ad-185">После этого необходимо установить бит СТАТУС_ОФФЛИНЕ в свойстве \*\*пр_статус_коде\*\* и возвращать значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="916ad-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="916ad-186">ПРОЦЕСС_КСП_ХЕАДЕР_КАЧЕ</span><span class="sxs-lookup"><span data-stu-id="916ad-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="916ad-187">Удаленный поставщик транспорта должен обрабатывать удаленные сообщения и отправлять сообщения, которые были отложены.</span><span class="sxs-lookup"><span data-stu-id="916ad-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="916ad-188">Для этого поставщик транспорта должен задать следующие значения свойств в строке состояния объекта входа:</span><span class="sxs-lookup"><span data-stu-id="916ad-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="916ad-189">ПриСвойте свойству **пр_статус_стринг** строку, которая указывает состояние поставщика транспорта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="916ad-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="916ad-190">Задайте биты СТАТУС_АУТБАУНД_ЕНАБЛЕД и СТАТУС_АУТБАУНД_АКТИВЕ в свойстве **пр_статус_коде** .</span><span class="sxs-lookup"><span data-stu-id="916ad-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="916ad-191">Задайте для свойства **пр_ремоте_валидате_ок** в строке состояния поставщика транспорта значение false.</span><span class="sxs-lookup"><span data-stu-id="916ad-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="916ad-192">Если выполняется другая операция (например, Загрузка заголовков) при вызове **валидатестате** , **валидатестате** должен возвратить мапи_е_буси.</span><span class="sxs-lookup"><span data-stu-id="916ad-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="916ad-193">Выполните код для обработки флага РЕФРЕШ_КСП_ХЕАДЕР_КАЧЕ, а также для удовлетворения требований клиента Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="916ad-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="916ad-194">РЕФРЕШ_КСП_ХЕАДЕР_КАЧЕ</span><span class="sxs-lookup"><span data-stu-id="916ad-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="916ad-195">Удаленный поставщик транспорта должен получить все новые заголовки сообщений из системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="916ad-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="916ad-196">Для этого поставщик транспорта должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="916ad-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="916ad-197">ПриСвойте свойству **пр_статус_стринг** строку, которая указывает состояние поставщика транспорта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="916ad-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="916ad-198">Задайте биты СТАТУС_ИНБАУНД_ЕНАБЛЕД и СТАТУС_ИНБАУНД_АКТИВЕ в свойстве **пр_статус_коде** .</span><span class="sxs-lookup"><span data-stu-id="916ad-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="916ad-199">Очистите бит СТАТУС_ОФФЛИНЕ в свойстве \*\*пр_статус_коде\*\* .</span><span class="sxs-lookup"><span data-stu-id="916ad-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="916ad-200">Установите бит СТАТУС_ОНЛИНЕ в свойстве \*\*пр_статус_коде\*\* .</span><span class="sxs-lookup"><span data-stu-id="916ad-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="916ad-201">Задайте для свойства **пр_ремоте_валидате_ок** в строке состояния поставщика транспорта значение false.</span><span class="sxs-lookup"><span data-stu-id="916ad-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="916ad-202">ШОВ_КСП_СЕССИОН_УИ</span><span class="sxs-lookup"><span data-stu-id="916ad-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="916ad-203">Если у поставщика транспорта есть какие-либо фрагменты пользовательского интерфейса для обработки заголовков сообщений (например, диалоговое окно, которое подтверждает загрузку сообщений), откроется диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="916ad-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="916ad-204">В противном случае **валидатестате** может вернуть мапи_е_но_суппорт.</span><span class="sxs-lookup"><span data-stu-id="916ad-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="916ad-205">Если передаются любые другие флаги, **валидатестате** должен вернуть мапи_е_ункновн_флагс.</span><span class="sxs-lookup"><span data-stu-id="916ad-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="916ad-206">Клиентский вызов поставщика транспорта часто будет поддерживать метод **имапистатус:: валидатестате** .</span><span class="sxs-lookup"><span data-stu-id="916ad-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="916ad-207">При обработке **валидатестате**поставщик транспорта не должен выполнять никакие действия, которые выделяют недостаточные системные ресурсы, например модем или COM-порт.</span><span class="sxs-lookup"><span data-stu-id="916ad-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="916ad-208">Это связано с тем, что диспетчеру MAPI иногда потребуется сбрасывать очереди на нескольких поставщиках транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="916ad-209">Тем не менее, клиент может в любой момент вызвать любой метод **валидатестате** поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="916ad-210">Если поставщик транспорта пытается выделить неограниченный ресурс во время обработки **валидатестате**, ошибка может возникать из-за конфликта с другим поставщиком транспорта, в котором диспетчер очереди MAPI предписывает очистить очереди.</span><span class="sxs-lookup"><span data-stu-id="916ad-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="916ad-211">Если вы разрешите все неограниченные выделения ресурсов при использовании очереди печати MAPI, можно избежать подобных конфликтов.</span><span class="sxs-lookup"><span data-stu-id="916ad-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="916ad-212">Поставщик транспорта должен поддерживать свойство **пр_ремоте_валидате_ок** , чтобы клиентские приложения могли определять, когда поставщик транспорта занят или ожидает, что диспетчер очереди MAPI начинает действие.</span><span class="sxs-lookup"><span data-stu-id="916ad-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="916ad-213">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="916ad-213">Notes to callers</span></span>

<span data-ttu-id="916ad-214">Так как этот метод может привести к выполнению других потенциально длительных вызовов, **валидатестате** может вернуть мапи_е_буси, чтобы сообщить о том, что этот метод ожидает завершения другой операции.</span><span class="sxs-lookup"><span data-stu-id="916ad-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="916ad-215">Перед попыткой выполнения другой задачи необходимо дождаться завершения ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="916ad-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="916ad-216">Вы можете управлять вызовами объектов состояния поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="916ad-217">В **валидатестате** можно передать один или несколько флагов, которые влияют на операции поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="916ad-218">Например, флаг АБОРТ_КСП_ХЕАДЕР_ОПЕРАТИОН указывает, что пользователь отменил проверку.</span><span class="sxs-lookup"><span data-stu-id="916ad-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="916ad-219">Поставщики транспорта могут отменить операцию, возвращая МАПИ_Е_УСЕР_КАНЦЕЛЕД, или продолжить.</span><span class="sxs-lookup"><span data-stu-id="916ad-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="916ad-220">Можно установить флаг КОНФИГ_ЧАНЖЕД для вызова в объект Status поставщика услуг или в диспетчере очереди MAPI, чтобы указать, что параметр конфигурации был изменен.</span><span class="sxs-lookup"><span data-stu-id="916ad-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="916ad-221">Вы можете использовать КОНФИГ_ЧАНЖЕД для динамической перенастройки поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="916ad-222">Когда вы настраиваете КОНФИГ_ЧАНЖЕД при вызове к объекту Status поставщика услуг, поставщик реагирует на вызов [имаписуппорт:: спулернотифи](imapisupport-spoolernotify.md) , чтобы предупредить Диспетчер очереди MAPI об изменении.</span><span class="sxs-lookup"><span data-stu-id="916ad-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="916ad-223">Когда вы задаете КОНФИГ_ЧАНЖЕД при вызове объекта Status диспетчера MAPI, диспетчер очереди вызовов вызывает [иксплогон:: аддресстипес](ixplogon-addresstypes.md) для каждого активного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="916ad-224">**Аддресстипес** информирует диспетчер очереди MAPI о поддерживаемых типах адресов транспорта.</span><span class="sxs-lookup"><span data-stu-id="916ad-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="916ad-225">Некоторые поставщики услуг также отображают индикатор хода выполнения, если предполагается выполнение проверки в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="916ad-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="916ad-226">Отображение индикатора хода выполнения полезно, но не обязательно.</span><span class="sxs-lookup"><span data-stu-id="916ad-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="916ad-227">Если установлен флаг СУППРЕСС_УИ, не отображаются ни вкладки свойств конфигурации, ни диалоговые окна хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="916ad-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="916ad-228">См. также</span><span class="sxs-lookup"><span data-stu-id="916ad-228">See also</span></span>

- [<span data-ttu-id="916ad-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="916ad-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="916ad-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="916ad-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="916ad-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="916ad-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="916ad-232">Каноническое свойство PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="916ad-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="916ad-233">Каноническое свойство PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="916ad-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="916ad-234">Каноническое свойство PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="916ad-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="916ad-235">Каноническое свойство PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="916ad-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="916ad-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="916ad-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

