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
ms.openlocfilehash: dae917b3e536aee5f24879edc3ccf0736e7c9f34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811730"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="1b801-103">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="1b801-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1b801-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b801-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b801-105">Содержит битовую маску флагов для поставщиков и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b801-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b801-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1b801-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b801-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1b801-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1b801-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1b801-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b801-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="1b801-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="1b801-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1b801-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b801-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1b801-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1b801-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1b801-112">Area:</span></span>  <br/> |<span data-ttu-id="1b801-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="1b801-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b801-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b801-114">Remarks</span></span>

<span data-ttu-id="1b801-115">Это свойство описывает характеристики службы сообщений, поставщик службы или состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1b801-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="1b801-116">Флаги, заданные для этого свойства зависит от его контекста.</span><span class="sxs-lookup"><span data-stu-id="1b801-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="1b801-117">К примеру некоторые флаги являются допустимыми только для объектов состояния и другие флаги только для столбцов в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b801-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="1b801-118">Флаги используются три классов: static, изменяемые и динамические.</span><span class="sxs-lookup"><span data-stu-id="1b801-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="1b801-119">Статические флаги задаются MAPI на основе данных в файл Mapisvc.inf. INF и никогда не изменяется.</span><span class="sxs-lookup"><span data-stu-id="1b801-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="1b801-120">Можно изменить флаги задаются MAPI в файл Mapisvc.inf. INF, но может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="1b801-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="1b801-121">Динамические флаги можно задать и сброс методами MAPI.</span><span class="sxs-lookup"><span data-stu-id="1b801-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="1b801-122">Для службы сообщений одной или нескольких из следующих флагов можно задать в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="1b801-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="1b801-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="1b801-124">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="1b801-124">Reserved.</span></span> <span data-ttu-id="1b801-125">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="1b801-125">Do not use.</span></span>
    
<span data-ttu-id="1b801-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="1b801-127">Динамические.</span><span class="sxs-lookup"><span data-stu-id="1b801-127">Dynamic.</span></span> <span data-ttu-id="1b801-128">Служба сообщений содержит хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b801-128">The message service contains the default store.</span></span> <span data-ttu-id="1b801-129">Пользовательский интерфейс должен отображаться запросом на подтверждение перед удалением или перемещением этой службы из профиля.</span><span class="sxs-lookup"><span data-stu-id="1b801-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="1b801-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="1b801-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="1b801-131">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-131">Static.</span></span> <span data-ttu-id="1b801-132">Флаг уровня службы, который должен содержать значение, указывающее, что ни один из поставщиков службы сообщений можно использовать для предоставления идентификатора.</span><span class="sxs-lookup"><span data-stu-id="1b801-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="1b801-133">Этот флаг или SERVICE_PRIMARY_IDENTITY должен быть набор, но не оба.</span><span class="sxs-lookup"><span data-stu-id="1b801-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="1b801-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="1b801-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="1b801-135">Можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b801-135">Modifiable.</span></span> <span data-ttu-id="1b801-136">Соответствующая служба сообщение содержит поставщика, используемый для основного удостоверения для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="1b801-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="1b801-137">Используйте [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) , чтобы установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="1b801-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="1b801-138">Этот флаг или SERVICE_NO_PRIMARY_IDENTITY должен быть набор, но не оба.</span><span class="sxs-lookup"><span data-stu-id="1b801-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="1b801-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="1b801-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="1b801-140">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-140">Static.</span></span> <span data-ttu-id="1b801-141">Любая попытка создания или скопируйте этой службы сообщений в профиль, где уже существует служба завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1b801-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="1b801-142">Для создания одной копии сообщения службы добавьте свойство **PR_RESOURCE_FLAGS** в раздел службы в файл Mapisvc.inf. INF и назначьте этот флаг.</span><span class="sxs-lookup"><span data-stu-id="1b801-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="1b801-143">Для поставщика услуг одной или нескольких из следующих флагов можно задать в **PR_RESOURCE_FLAGS**:</span><span class="sxs-lookup"><span data-stu-id="1b801-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="1b801-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="1b801-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="1b801-145">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-145">Static.</span></span> <span data-ttu-id="1b801-146">Обработчик очереди необходим для обработки входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b801-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="1b801-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="1b801-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="1b801-148">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-148">Static.</span></span> <span data-ttu-id="1b801-149">Обработчик очереди должен обработки исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="1b801-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="1b801-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="1b801-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="1b801-151">Можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b801-151">Modifiable.</span></span> <span data-ttu-id="1b801-152">Это удостоверение должен применяться для исходящих сообщений, если профиль содержит несколько экземпляров данного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="1b801-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="1b801-153">Это может произойти, если несколько экземпляров одной транспорт отображаются в профиле.</span><span class="sxs-lookup"><span data-stu-id="1b801-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="1b801-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="1b801-155">Можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b801-155">Modifiable.</span></span> <span data-ttu-id="1b801-156">В этом хранилище сообщений — это хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="1b801-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="1b801-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="1b801-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="1b801-158">Динамические.</span><span class="sxs-lookup"><span data-stu-id="1b801-158">Dynamic.</span></span> <span data-ttu-id="1b801-159">Стандартные папки хранилища, включая корневую папку электронной почты — это сообщение (IPM), не было проверено.</span><span class="sxs-lookup"><span data-stu-id="1b801-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="1b801-160">MAPI задает и удаляет этот флаг.</span><span class="sxs-lookup"><span data-stu-id="1b801-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="1b801-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="1b801-162">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-162">Static.</span></span> <span data-ttu-id="1b801-163">В этом хранилище сообщений не способен стать хранилище сообщений по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="1b801-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="1b801-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="1b801-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="1b801-165">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-165">Static.</span></span> <span data-ttu-id="1b801-166">Этот поставщик не предоставил удостоверения в его строке состояния.</span><span class="sxs-lookup"><span data-stu-id="1b801-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="1b801-167">Этот флаг или STATUS_PRIMARY_IDENTITY должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="1b801-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="1b801-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="1b801-169">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-169">Static.</span></span> <span data-ttu-id="1b801-170">Данный транспортный протокол тесно связаны с хранилищем сообщений и предоставляющей свойство **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) в строке его состояния.</span><span class="sxs-lookup"><span data-stu-id="1b801-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="1b801-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="1b801-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="1b801-172">Можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b801-172">Modifiable.</span></span> <span data-ttu-id="1b801-173">Этот поставщик передает основной идентификатор для сеанса; Идентификатор записи для передачи идентификатора объекта возвращается из [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="1b801-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="1b801-174">Это флаг или **STATUS_NO_PRIMARY_IDENTITY** должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="1b801-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="1b801-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="1b801-176">Можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b801-176">Modifiable.</span></span> <span data-ttu-id="1b801-177">В этом хранилище сообщений будет использоваться при входе в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="1b801-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="1b801-178">После запуска этого хранилища следует задать в качестве хранилища по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="1b801-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="1b801-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="1b801-180">Можно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b801-180">Modifiable.</span></span> <span data-ttu-id="1b801-181">Хранилища будет использоваться, если основного хранилища недоступен при входе в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="1b801-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="1b801-182">После запуска этого хранилища следует задать в качестве хранилища по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="1b801-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="1b801-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="1b801-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="1b801-184">Динамические.</span><span class="sxs-lookup"><span data-stu-id="1b801-184">Dynamic.</span></span> <span data-ttu-id="1b801-185">В этом хранилище сообщений используется Simple MAPI как его хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b801-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="1b801-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="1b801-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="1b801-187">Динамические.</span><span class="sxs-lookup"><span data-stu-id="1b801-187">Dynamic.</span></span> <span data-ttu-id="1b801-188">Хранилища не должны быть опубликованы в таблице хранилища сообщений и будет удален из профиля после выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="1b801-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="1b801-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="1b801-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="1b801-190">Static.</span><span class="sxs-lookup"><span data-stu-id="1b801-190">Static.</span></span> <span data-ttu-id="1b801-191">В этом транспорта ожидает последнего транспорта, установите флажок, чтобы отправить сообщение, когда несколько поставщиков транспорта существует возможность передачи сообщения.</span><span class="sxs-lookup"><span data-stu-id="1b801-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1b801-192">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1b801-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b801-193">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1b801-193">Header files</span></span>

<span data-ttu-id="1b801-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b801-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b801-195">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1b801-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b801-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b801-196">Mapitags.h</span></span>
  
> <span data-ttu-id="1b801-197">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1b801-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b801-198">См. также</span><span class="sxs-lookup"><span data-stu-id="1b801-198">See also</span></span>



[<span data-ttu-id="1b801-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="1b801-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="1b801-200">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="1b801-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="1b801-201">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b801-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b801-202">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b801-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b801-203">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1b801-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b801-204">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1b801-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

