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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330186"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="b251b-103">Каноническое свойство PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="b251b-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="b251b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b251b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b251b-105">Содержит битовую маску флагов для служб сообщений и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b251b-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b251b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b251b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b251b-107">ПР_РЕСАУРЦЕ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="b251b-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="b251b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b251b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b251b-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="b251b-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="b251b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b251b-110">Data type:</span></span>  <br/> |<span data-ttu-id="b251b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b251b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b251b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b251b-112">Area:</span></span>  <br/> |<span data-ttu-id="b251b-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="b251b-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b251b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b251b-114">Remarks</span></span>

<span data-ttu-id="b251b-115">Это свойство описывает характеристики службы сообщений, поставщика услуг или объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="b251b-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="b251b-116">Флаги, заданные для этого свойства, зависят от контекста.</span><span class="sxs-lookup"><span data-stu-id="b251b-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="b251b-117">Например, некоторые флаги действительны только для объектов status и других флагов только для столбцов в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b251b-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="b251b-118">Флаги относятся к трем классам: статические, изменяемые и динамические.</span><span class="sxs-lookup"><span data-stu-id="b251b-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="b251b-119">Статические флаги устанавливаются MAPI из данных в MAPISVC. INF и никогда не изменялся.</span><span class="sxs-lookup"><span data-stu-id="b251b-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="b251b-120">Изменяемые флаги устанавливаются MAPI из MAPISVC. INF, но его можно изменить позже.</span><span class="sxs-lookup"><span data-stu-id="b251b-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="b251b-121">Динамические флаги можно устанавливать и сбрасывать с помощью методов MAPI.</span><span class="sxs-lookup"><span data-stu-id="b251b-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="b251b-122">Для службы сообщений можно задать один или несколько из следующих флагов в этом свойстве:</span><span class="sxs-lookup"><span data-stu-id="b251b-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="b251b-123">СЕРВИЦЕ_КРЕАТЕ_ВИС_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="b251b-124">Резервирования.</span><span class="sxs-lookup"><span data-stu-id="b251b-124">Reserved.</span></span> <span data-ttu-id="b251b-125">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="b251b-125">Do not use.</span></span>
    
<span data-ttu-id="b251b-126">СЕРВИЦЕ_ДЕФАУЛТ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="b251b-127">Платформа.</span><span class="sxs-lookup"><span data-stu-id="b251b-127">Dynamic.</span></span> <span data-ttu-id="b251b-128">Служба сообщений содержит хранилище по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b251b-128">The message service contains the default store.</span></span> <span data-ttu-id="b251b-129">Пользовательский интерфейс должен отображаться С запросом подтверждения перед удалением или перемещением этой службы из профиля.</span><span class="sxs-lookup"><span data-stu-id="b251b-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="b251b-130">СЕРВИЦЕ_НО_ПРИМАРИ_ИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="b251b-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="b251b-131">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-131">Static.</span></span> <span data-ttu-id="b251b-132">Флаг уровня обслуживания, указывающий, что ни один из поставщиков в службе сообщений не может быть использован для предоставления удостоверения.</span><span class="sxs-lookup"><span data-stu-id="b251b-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="b251b-133">Этот флаг или СЕРВИЦЕ_ПРИМАРИ_ИДЕНТИТИ должен быть задан, но не оба.</span><span class="sxs-lookup"><span data-stu-id="b251b-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="b251b-134">СЕРВИЦЕ_ПРИМАРИ_ИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="b251b-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="b251b-135">Допуска.</span><span class="sxs-lookup"><span data-stu-id="b251b-135">Modifiable.</span></span> <span data-ttu-id="b251b-136">Соответствующая служба сообщений содержит поставщика, используемого для основного удостоверения для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="b251b-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="b251b-137">Используйте [имсгсервицеадмин:: сетпримаридентити](imsgserviceadmin-setprimaryidentity.md) , чтобы установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b251b-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="b251b-138">Этот флаг или СЕРВИЦЕ_НО_ПРИМАРИ_ИДЕНТИТИ должен быть задан, но не оба.</span><span class="sxs-lookup"><span data-stu-id="b251b-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="b251b-139">СЕРВИЦЕ_СИНГЛЕ_КОПИ</span><span class="sxs-lookup"><span data-stu-id="b251b-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="b251b-140">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-140">Static.</span></span> <span data-ttu-id="b251b-141">Любая попытка создать или скопировать эту службу сообщений в профиль, в котором служба уже существует, завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="b251b-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="b251b-142">Чтобы создать одну службу сообщений копии, добавьте свойство **пр_ресаурце_флагс** в раздел службы в Mapisvc. INF и установите этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b251b-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="b251b-143">Для поставщика услуг можно задать один или несколько из следующих флагов в **пр_ресаурце_флагс**:</span><span class="sxs-lookup"><span data-stu-id="b251b-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="b251b-144">ХУК_ИНБАУНД</span><span class="sxs-lookup"><span data-stu-id="b251b-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="b251b-145">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-145">Static.</span></span> <span data-ttu-id="b251b-146">Ловушке диспетчера очереди должны обрабатывать входящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="b251b-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="b251b-147">ХУК_АУТБАУНД</span><span class="sxs-lookup"><span data-stu-id="b251b-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="b251b-148">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-148">Static.</span></span> <span data-ttu-id="b251b-149">Ловушке диспетчера очереди должны обрабатывать исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="b251b-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="b251b-150">СТАТУС_ДЕФАУЛТ_АУТБАУНД</span><span class="sxs-lookup"><span data-stu-id="b251b-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="b251b-151">Допуска.</span><span class="sxs-lookup"><span data-stu-id="b251b-151">Modifiable.</span></span> <span data-ttu-id="b251b-152">Это удостоверение следует применять к исходящим сообщениям, если профиль содержит несколько экземпляров этого поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="b251b-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="b251b-153">Это может произойти, если в профиле отображается несколько экземпляров одного поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="b251b-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="b251b-154">СТАТУС_ДЕФАУЛТ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="b251b-155">Допуска.</span><span class="sxs-lookup"><span data-stu-id="b251b-155">Modifiable.</span></span> <span data-ttu-id="b251b-156">Это хранилище сообщений является хранилищем по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="b251b-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="b251b-157">СТАТУС_НИД_ИПМ_ТРИ</span><span class="sxs-lookup"><span data-stu-id="b251b-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="b251b-158">Платформа.</span><span class="sxs-lookup"><span data-stu-id="b251b-158">Dynamic.</span></span> <span data-ttu-id="b251b-159">Стандартные папки в этом хранилище сообщений, включая корневую папку сообщений (IPM), еще не прошли проверку.</span><span class="sxs-lookup"><span data-stu-id="b251b-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="b251b-160">MAPI задает и очищает этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b251b-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="b251b-161">СТАТУС_НО_ДЕФАУЛТ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="b251b-162">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-162">Static.</span></span> <span data-ttu-id="b251b-163">Этот банк сообщений не может стать хранилищем сообщений по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="b251b-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="b251b-164">СТАТУС_НО_ПРИМАРИ_ИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="b251b-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="b251b-165">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-165">Static.</span></span> <span data-ttu-id="b251b-166">Этот поставщик не предоставляет удостоверение в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="b251b-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="b251b-167">Необходимо задать этот флаг или СТАТУС_ПРИМАРИ_ИДЕНТИТИ.</span><span class="sxs-lookup"><span data-stu-id="b251b-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="b251b-168">СТАТУС_ОВН_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="b251b-169">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-169">Static.</span></span> <span data-ttu-id="b251b-170">Этот поставщик транспорта тесно связан с хранилищем сообщений и представляет свойство **пр_овн_сторе_ентрид** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="b251b-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="b251b-171">СТАТУС_ПРИМАРИ_ИДЕНТИТИ</span><span class="sxs-lookup"><span data-stu-id="b251b-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="b251b-172">Допуска.</span><span class="sxs-lookup"><span data-stu-id="b251b-172">Modifiable.</span></span> <span data-ttu-id="b251b-173">Этот поставщик имеет основной идентификатор для сеанса; Идентификатор записи для объекта, удостоверяющего идентификатор, возвращается из [IMAPISession:: куеридентити](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="b251b-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="b251b-174">Необходимо задать этот флаг или **статус_но_примари_идентити** .</span><span class="sxs-lookup"><span data-stu-id="b251b-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="b251b-175">СТАТУС_ПРИМАРИ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="b251b-176">Допуска.</span><span class="sxs-lookup"><span data-stu-id="b251b-176">Modifiable.</span></span> <span data-ttu-id="b251b-177">Это хранилище сообщений используется, когда клиентское приложение выполняет вход.</span><span class="sxs-lookup"><span data-stu-id="b251b-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="b251b-178">После открытия это хранилище должно быть настроено как хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="b251b-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="b251b-179">СТАТУС_СЕКОНДАРИ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="b251b-180">Допуска.</span><span class="sxs-lookup"><span data-stu-id="b251b-180">Modifiable.</span></span> <span data-ttu-id="b251b-181">Этот банк сообщений используется, если первичное хранилище недоступно, когда клиентское приложение выполняет вход.</span><span class="sxs-lookup"><span data-stu-id="b251b-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="b251b-182">После открытия это хранилище должно быть настроено как хранилище по умолчанию для профиля.</span><span class="sxs-lookup"><span data-stu-id="b251b-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="b251b-183">СТАТУС_СИМПЛЕ_СТОРЕ</span><span class="sxs-lookup"><span data-stu-id="b251b-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="b251b-184">Платформа.</span><span class="sxs-lookup"><span data-stu-id="b251b-184">Dynamic.</span></span> <span data-ttu-id="b251b-185">Этот банк сообщений будет использоваться простым MAPI в качестве хранилища сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b251b-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="b251b-186">СТАТУС_ТЕМП_СЕКТИОН</span><span class="sxs-lookup"><span data-stu-id="b251b-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="b251b-187">Платформа.</span><span class="sxs-lookup"><span data-stu-id="b251b-187">Dynamic.</span></span> <span data-ttu-id="b251b-188">Этот банк сообщений не должен быть опубликован в таблице хранилища сообщений и будет удален из профиля после выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="b251b-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="b251b-189">СТАТУС_КСП_ПРЕФЕР_ЛАСТ</span><span class="sxs-lookup"><span data-stu-id="b251b-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="b251b-190">Статический.</span><span class="sxs-lookup"><span data-stu-id="b251b-190">Static.</span></span> <span data-ttu-id="b251b-191">Предполагается, что этот транспорт является последним выбранным для отправки сообщениям, когда несколько поставщиков транспорта могут передать сообщение.</span><span class="sxs-lookup"><span data-stu-id="b251b-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b251b-192">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b251b-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b251b-193">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="b251b-193">Header files</span></span>

<span data-ttu-id="b251b-194">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b251b-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="b251b-195">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b251b-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="b251b-196">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="b251b-196">Mapitags.h</span></span>
  
> <span data-ttu-id="b251b-197">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="b251b-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b251b-198">См. также</span><span class="sxs-lookup"><span data-stu-id="b251b-198">See also</span></span>



[<span data-ttu-id="b251b-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="b251b-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="b251b-200">Каноническое свойство PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="b251b-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="b251b-201">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b251b-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b251b-202">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="b251b-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b251b-203">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b251b-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b251b-204">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b251b-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

