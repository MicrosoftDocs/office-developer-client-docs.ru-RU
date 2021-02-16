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
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="30a0c-103">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="30a0c-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="30a0c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30a0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30a0c-105">Содержит битовуюmass флагов для служб и поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="30a0c-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30a0c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="30a0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30a0c-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="30a0c-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="30a0c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="30a0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30a0c-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="30a0c-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="30a0c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="30a0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="30a0c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="30a0c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="30a0c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="30a0c-112">Area:</span></span>  <br/> |<span data-ttu-id="30a0c-113">Общие MAPI</span><span class="sxs-lookup"><span data-stu-id="30a0c-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30a0c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="30a0c-114">Remarks</span></span>

<span data-ttu-id="30a0c-115">Это свойство описывает характеристики службы сообщений, поставщика службы или объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="30a0c-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="30a0c-116">Флаги, установленные для этого свойства, зависят от его контекста.</span><span class="sxs-lookup"><span data-stu-id="30a0c-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="30a0c-117">Например, некоторые флаги допустимы только для объектов состояния, а другие флаги только для столбцов в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="30a0c-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="30a0c-118">Флаги имеют три класса: статические, изможимые и динамические.</span><span class="sxs-lookup"><span data-stu-id="30a0c-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="30a0c-119">Статические флаги устанавливаются MAPI из данных в MAPISVC. InF и никогда не изменяется.</span><span class="sxs-lookup"><span data-stu-id="30a0c-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="30a0c-120">Modifiable flags are set by MAPI from MAPISVC. INF, но впоследствии его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="30a0c-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="30a0c-121">Динамические флаги можно устанавливать и сбрасывать с помощью методов MAPI.</span><span class="sxs-lookup"><span data-stu-id="30a0c-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="30a0c-122">Для службы сообщений в этом свойстве можно установить один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="30a0c-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="30a0c-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="30a0c-124">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="30a0c-124">Reserved.</span></span> <span data-ttu-id="30a0c-125">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="30a0c-125">Do not use.</span></span>
    
<span data-ttu-id="30a0c-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="30a0c-127">Динамический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-127">Dynamic.</span></span> <span data-ttu-id="30a0c-128">Служба сообщений содержит хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30a0c-128">The message service contains the default store.</span></span> <span data-ttu-id="30a0c-129">Перед удалением или перемещением этой службы из профиля должен отображаться пользовательский интерфейс с запросом подтверждения.</span><span class="sxs-lookup"><span data-stu-id="30a0c-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="30a0c-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="30a0c-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="30a0c-131">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-131">Static.</span></span> <span data-ttu-id="30a0c-132">Флаг уровня службы, который должен указывать, что ни один из поставщиков в службе сообщений не может использоваться для идентификации.</span><span class="sxs-lookup"><span data-stu-id="30a0c-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="30a0c-133">Этот флаг или SERVICE_PRIMARY_IDENTITY должен быть установлен, но не оба.</span><span class="sxs-lookup"><span data-stu-id="30a0c-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="30a0c-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="30a0c-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="30a0c-135">Можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="30a0c-135">Modifiable.</span></span> <span data-ttu-id="30a0c-136">Соответствующая служба сообщений содержит поставщика, используемого для основного удостоверения для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="30a0c-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="30a0c-137">Используйте [IMsgServiceAdmin::SetPrimaryIdentity,](imsgserviceadmin-setprimaryidentity.md) чтобы установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="30a0c-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="30a0c-138">Этот флаг или SERVICE_NO_PRIMARY_IDENTITY должен быть установлен, но не оба.</span><span class="sxs-lookup"><span data-stu-id="30a0c-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="30a0c-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="30a0c-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="30a0c-140">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-140">Static.</span></span> <span data-ttu-id="30a0c-141">Любая попытка создать или скопировать эту службу сообщений в профиль, в котором она уже существует, не удастся.</span><span class="sxs-lookup"><span data-stu-id="30a0c-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="30a0c-142">Чтобы создать службу сообщений с **одной копией, добавьте PR_RESOURCE_FLAGS** в раздел службы в MAPISVC. InF и установите этот флаг.</span><span class="sxs-lookup"><span data-stu-id="30a0c-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="30a0c-143">Для поставщика услуг можно установить один или несколько из следующих флагов в **PR_RESOURCE_FLAGS:**</span><span class="sxs-lookup"><span data-stu-id="30a0c-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="30a0c-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="30a0c-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="30a0c-145">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-145">Static.</span></span> <span data-ttu-id="30a0c-146">Обжевщик пула должен обрабатывать входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="30a0c-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="30a0c-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="30a0c-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="30a0c-148">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-148">Static.</span></span> <span data-ttu-id="30a0c-149">Обжевщик пула должен обрабатывать исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="30a0c-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="30a0c-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="30a0c-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="30a0c-151">Можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="30a0c-151">Modifiable.</span></span> <span data-ttu-id="30a0c-152">Это удостоверение должно применяться к исходящие сообщения, если профиль содержит несколько экземпляров этого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="30a0c-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="30a0c-153">Это может произойти, если в профиле появляется несколько экземпляров одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="30a0c-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="30a0c-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="30a0c-155">Можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="30a0c-155">Modifiable.</span></span> <span data-ttu-id="30a0c-156">Это хранилище сообщений является хранилищем по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="30a0c-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="30a0c-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="30a0c-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="30a0c-158">Динамический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-158">Dynamic.</span></span> <span data-ttu-id="30a0c-159">Стандартные папки в этом хранилище сообщений, включая корневую папку IPM, еще не проверены.</span><span class="sxs-lookup"><span data-stu-id="30a0c-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="30a0c-160">MAPI устанавливает и очищает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="30a0c-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="30a0c-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="30a0c-162">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-162">Static.</span></span> <span data-ttu-id="30a0c-163">Это хранилище сообщений не может стать хранилищем сообщений по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="30a0c-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="30a0c-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="30a0c-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="30a0c-165">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-165">Static.</span></span> <span data-ttu-id="30a0c-166">Этот поставщик не дает удостоверение в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="30a0c-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="30a0c-167">Этот флаг или STATUS_PRIMARY_IDENTITY должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="30a0c-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="30a0c-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="30a0c-169">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-169">Static.</span></span> <span data-ttu-id="30a0c-170">Этот поставщик транспорта тесно совмещается с хранилищем сообщений и хранит свойство **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId)](pidtagownstoreentryid-canonical-property.md)в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="30a0c-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="30a0c-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="30a0c-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="30a0c-172">Можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="30a0c-172">Modifiable.</span></span> <span data-ttu-id="30a0c-173">Этот поставщик предоставил основное удостоверение для сеанса; Идентификатор записи для объекта, в котором предоставлено удостоверение, возвращается из [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="30a0c-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="30a0c-174">Этот флаг или **STATUS_NO_PRIMARY_IDENTITY** должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="30a0c-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="30a0c-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="30a0c-176">Можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="30a0c-176">Modifiable.</span></span> <span data-ttu-id="30a0c-177">Это хранилище сообщений используется при входе в систему клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="30a0c-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="30a0c-178">После открытия это хранилище должно быть установлено как хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="30a0c-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="30a0c-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="30a0c-180">Можно модификабельно.</span><span class="sxs-lookup"><span data-stu-id="30a0c-180">Modifiable.</span></span> <span data-ttu-id="30a0c-181">Это хранилище сообщений будет использоваться, если основное хранилище не доступно при входе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="30a0c-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="30a0c-182">После открытия это хранилище должно быть установлено как хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="30a0c-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="30a0c-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="30a0c-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="30a0c-184">Динамический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-184">Dynamic.</span></span> <span data-ttu-id="30a0c-185">Это хранилище сообщений будет использоваться Simple MAPI как хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="30a0c-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="30a0c-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="30a0c-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="30a0c-187">Динамический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-187">Dynamic.</span></span> <span data-ttu-id="30a0c-188">Это хранилище сообщений не должно быть опубликовано в таблице хранения сообщений и будет удалено из профиля после удаления.</span><span class="sxs-lookup"><span data-stu-id="30a0c-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="30a0c-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="30a0c-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="30a0c-190">Статический.</span><span class="sxs-lookup"><span data-stu-id="30a0c-190">Static.</span></span> <span data-ttu-id="30a0c-191">Этот транспорт должен быть последним транспортом, выбранным для отправки сообщения, когда несколько поставщиков транспорта могут передать сообщение.</span><span class="sxs-lookup"><span data-stu-id="30a0c-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="30a0c-192">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="30a0c-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="30a0c-193">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="30a0c-193">Header files</span></span>

<span data-ttu-id="30a0c-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30a0c-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="30a0c-195">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="30a0c-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="30a0c-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="30a0c-196">Mapitags.h</span></span>
  
> <span data-ttu-id="30a0c-197">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="30a0c-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30a0c-198">См. также</span><span class="sxs-lookup"><span data-stu-id="30a0c-198">See also</span></span>



[<span data-ttu-id="30a0c-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="30a0c-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="30a0c-200">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="30a0c-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="30a0c-201">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="30a0c-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30a0c-202">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="30a0c-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30a0c-203">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="30a0c-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30a0c-204">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="30a0c-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

