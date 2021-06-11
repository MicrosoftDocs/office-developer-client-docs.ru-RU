---
title: Каноническое свойство PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436232"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="63f47-103">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="63f47-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="63f47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63f47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63f47-105">Содержит битмаску флагов для служб и поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="63f47-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="63f47-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="63f47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="63f47-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="63f47-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="63f47-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="63f47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="63f47-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="63f47-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="63f47-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="63f47-110">Data type:</span></span>  <br/> |<span data-ttu-id="63f47-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="63f47-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="63f47-112">Область:</span><span class="sxs-lookup"><span data-stu-id="63f47-112">Area:</span></span>  <br/> |<span data-ttu-id="63f47-113">MAPI общие</span><span class="sxs-lookup"><span data-stu-id="63f47-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63f47-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="63f47-114">Remarks</span></span>

<span data-ttu-id="63f47-115">В этом свойстве описываются характеристики службы сообщений, поставщика услуг или объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="63f47-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="63f47-116">Флаги, заданной для этого свойства, зависят от контекста.</span><span class="sxs-lookup"><span data-stu-id="63f47-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="63f47-117">Например, некоторые флаги допустимы только для объектов состояния, а другие — только для столбцов в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="63f47-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="63f47-118">Флаги имеют три класса: статический, модификабельный и динамический.</span><span class="sxs-lookup"><span data-stu-id="63f47-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="63f47-119">Статические флаги устанавливаются MAPI из данных в MAPISVC. INF и никогда не менялся.</span><span class="sxs-lookup"><span data-stu-id="63f47-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="63f47-120">Modifiable flags are set by MAPI from MAPISVC. INF, но может быть впоследствии изменен.</span><span class="sxs-lookup"><span data-stu-id="63f47-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="63f47-121">Динамические флаги можно установить и сбросить с помощью методов MAPI.</span><span class="sxs-lookup"><span data-stu-id="63f47-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="63f47-122">Для службы сообщений в этом свойстве можно установить один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="63f47-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="63f47-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="63f47-124">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="63f47-124">Reserved.</span></span> <span data-ttu-id="63f47-125">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="63f47-125">Do not use.</span></span>
    
<span data-ttu-id="63f47-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="63f47-127">Динамический.</span><span class="sxs-lookup"><span data-stu-id="63f47-127">Dynamic.</span></span> <span data-ttu-id="63f47-128">Служба сообщений содержит хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63f47-128">The message service contains the default store.</span></span> <span data-ttu-id="63f47-129">Перед удалением или удалением этой службы из профиля должен отображаться пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="63f47-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="63f47-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="63f47-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="63f47-131">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-131">Static.</span></span> <span data-ttu-id="63f47-132">Флаг уровня службы, который должен указывать, что ни один из поставщиков в службе сообщений не может использоваться для обеспечения удостоверения.</span><span class="sxs-lookup"><span data-stu-id="63f47-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="63f47-133">Этот флаг или SERVICE_PRIMARY_IDENTITY должен быть заданной, но не оба.</span><span class="sxs-lookup"><span data-stu-id="63f47-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="63f47-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="63f47-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="63f47-135">Модификабель.</span><span class="sxs-lookup"><span data-stu-id="63f47-135">Modifiable.</span></span> <span data-ttu-id="63f47-136">Соответствующая служба сообщений содержит поставщика, используемого для основного удостоверения для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="63f47-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="63f47-137">Для этого флага используйте [объект IMsgServiceAdmin::SetPrimaryIdentity.](imsgserviceadmin-setprimaryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="63f47-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="63f47-138">Этот флаг или SERVICE_NO_PRIMARY_IDENTITY должен быть установлен, но не оба.</span><span class="sxs-lookup"><span data-stu-id="63f47-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="63f47-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="63f47-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="63f47-140">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-140">Static.</span></span> <span data-ttu-id="63f47-141">Любая попытка создать или скопировать эту службу сообщений в профиль, в котором уже существует служба, будет неудачной.</span><span class="sxs-lookup"><span data-stu-id="63f47-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="63f47-142">Чтобы создать единую службу копирования, **добавьте свойство PR_RESOURCE_FLAGS** в раздел службы в MAPISVC. INF и установите этот флаг.</span><span class="sxs-lookup"><span data-stu-id="63f47-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="63f47-143">Для поставщика услуг один или несколько из следующих флагов можно установить в **PR_RESOURCE_FLAGS:**</span><span class="sxs-lookup"><span data-stu-id="63f47-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="63f47-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="63f47-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="63f47-145">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-145">Static.</span></span> <span data-ttu-id="63f47-146">Крюк шпалер должен обрабатывать входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="63f47-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="63f47-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="63f47-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="63f47-148">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-148">Static.</span></span> <span data-ttu-id="63f47-149">Крюк шпалер должен обрабатывать исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="63f47-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="63f47-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="63f47-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="63f47-151">Модификабель.</span><span class="sxs-lookup"><span data-stu-id="63f47-151">Modifiable.</span></span> <span data-ttu-id="63f47-152">Это удостоверение следует применять к исходящие сообщения, если профиль содержит несколько экземпляров этого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="63f47-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="63f47-153">Это может произойти, если в профиле появится несколько экземпляров одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="63f47-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="63f47-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="63f47-155">Модификабель.</span><span class="sxs-lookup"><span data-stu-id="63f47-155">Modifiable.</span></span> <span data-ttu-id="63f47-156">Этот магазин сообщений — хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="63f47-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="63f47-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="63f47-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="63f47-158">Динамический.</span><span class="sxs-lookup"><span data-stu-id="63f47-158">Dynamic.</span></span> <span data-ttu-id="63f47-159">Стандартные папки в этом хранилище сообщений, включая корневую папку межличностного сообщения (IPM), еще не проверены.</span><span class="sxs-lookup"><span data-stu-id="63f47-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="63f47-160">MAPI устанавливает и очищает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="63f47-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="63f47-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="63f47-162">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-162">Static.</span></span> <span data-ttu-id="63f47-163">Этот магазин сообщений не может стать хранилищем сообщений по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="63f47-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="63f47-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="63f47-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="63f47-165">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-165">Static.</span></span> <span data-ttu-id="63f47-166">Этот поставщик не дает удостоверение в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="63f47-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="63f47-167">Этот флаг или STATUS_PRIMARY_IDENTITY должен быть заданной.</span><span class="sxs-lookup"><span data-stu-id="63f47-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="63f47-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="63f47-169">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-169">Static.</span></span> <span data-ttu-id="63f47-170">Этот поставщик транспорта тесно соединен с хранилищем сообщений и обставирует свойство[PR_OWN_STORE_ENTRYID (PidTagOwnStoreEntryId)](pidtagownstoreentryid-canonical-property.md)в строке состояния. </span><span class="sxs-lookup"><span data-stu-id="63f47-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="63f47-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="63f47-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="63f47-172">Модификабель.</span><span class="sxs-lookup"><span data-stu-id="63f47-172">Modifiable.</span></span> <span data-ttu-id="63f47-173">Этот поставщик дает основное удостоверение сеанса; идентификатор входа для объекта, обставленного удостоверением, возвращается из [IMAPISession::QueryIdentity.](imapisession-queryidentity.md)</span><span class="sxs-lookup"><span data-stu-id="63f47-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="63f47-174">Этот флаг или **STATUS_NO_PRIMARY_IDENTITY** должен быть заданной.</span><span class="sxs-lookup"><span data-stu-id="63f47-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="63f47-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="63f47-176">Модификабель.</span><span class="sxs-lookup"><span data-stu-id="63f47-176">Modifiable.</span></span> <span data-ttu-id="63f47-177">Этот магазин сообщений должен использоваться при входе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="63f47-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="63f47-178">После открытия этот магазин должен быть заданной как хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="63f47-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="63f47-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="63f47-180">Модификабель.</span><span class="sxs-lookup"><span data-stu-id="63f47-180">Modifiable.</span></span> <span data-ttu-id="63f47-181">Этот магазин сообщений будет использоваться, если основной магазин не доступен при входе в систему клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="63f47-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="63f47-182">После открытия этот магазин должен быть заданной как хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="63f47-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="63f47-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="63f47-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="63f47-184">Динамический.</span><span class="sxs-lookup"><span data-stu-id="63f47-184">Dynamic.</span></span> <span data-ttu-id="63f47-185">Этот хранилище сообщений будет использоваться simple MAPI в качестве магазина сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="63f47-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="63f47-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="63f47-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="63f47-187">Динамический.</span><span class="sxs-lookup"><span data-stu-id="63f47-187">Dynamic.</span></span> <span data-ttu-id="63f47-188">Этот магазин сообщений не должен публиковаться в таблице хранения сообщений и будет удален из профиля после входа.</span><span class="sxs-lookup"><span data-stu-id="63f47-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="63f47-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="63f47-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="63f47-190">Статическое.</span><span class="sxs-lookup"><span data-stu-id="63f47-190">Static.</span></span> <span data-ttu-id="63f47-191">Этот транспорт будет последним транспортом, выбранным для отправки сообщения, когда несколько поставщиков транспорта могут передать сообщение.</span><span class="sxs-lookup"><span data-stu-id="63f47-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="63f47-192">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="63f47-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="63f47-193">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="63f47-193">Header files</span></span>

<span data-ttu-id="63f47-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="63f47-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="63f47-195">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="63f47-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="63f47-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="63f47-196">Mapitags.h</span></span>
  
> <span data-ttu-id="63f47-197">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="63f47-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="63f47-198">См. также</span><span class="sxs-lookup"><span data-stu-id="63f47-198">See also</span></span>



[<span data-ttu-id="63f47-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="63f47-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="63f47-200">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="63f47-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="63f47-201">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63f47-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="63f47-202">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="63f47-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="63f47-203">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="63f47-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="63f47-204">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="63f47-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

