---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405816"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="91738-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="91738-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="91738-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91738-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91738-105">Выполняет разрешение имен для одной или более записей получателей.</span><span class="sxs-lookup"><span data-stu-id="91738-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="91738-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="91738-106">Parameters</span></span>

 <span data-ttu-id="91738-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="91738-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="91738-108">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, описывающих свойства, которые должны быть включены в структуру [ADRLIST,](adrlist.md) возвращаемую поставщиком.</span><span class="sxs-lookup"><span data-stu-id="91738-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="91738-109">Чтобы запросить набор свойств поставщика по умолчанию, передай NULL в _параметре lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="91738-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="91738-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91738-110">_ulFlags_</span></span>
  
> <span data-ttu-id="91738-111">[in] Немного флагов, которые контролируют тип текста в возвращенных строках.</span><span class="sxs-lookup"><span data-stu-id="91738-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="91738-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="91738-112">The following flags can be set:</span></span>
    
<span data-ttu-id="91738-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="91738-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="91738-114">Будут найдены только точные совпадения адресов прокси- адресов; частичные совпадения игнорируются.</span><span class="sxs-lookup"><span data-stu-id="91738-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="91738-115">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="91738-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="91738-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="91738-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="91738-117">Для выполнения разрешения имен будет использоваться только офлайн-адресная книга.</span><span class="sxs-lookup"><span data-stu-id="91738-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="91738-118">Например, этот флаг можно использовать для того, чтобы клиентская заявка открывала глобальный адресный список (GAL) в кэшировом режиме обмена и доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="91738-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="91738-119">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="91738-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="91738-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91738-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="91738-121">Возвращенные свойства строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="91738-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="91738-122">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="91738-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="91738-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="91738-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="91738-124">[in, out] На входе указатель на структуру **ADRLIST,** содержаную список получателей, которые необходимо устранить.</span><span class="sxs-lookup"><span data-stu-id="91738-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="91738-125">На выходе указатель на структуру **ADRLIST,** содержаную разрешенные имена.</span><span class="sxs-lookup"><span data-stu-id="91738-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="91738-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="91738-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="91738-127">[in, out] Указатель на массив флагов, каждый флаг, соответствующий структуре [ADRENTRY](adrentry.md) в параметре  _lpAdrList,_ который обеспечивает состояние операции разрешения имен для получателя.</span><span class="sxs-lookup"><span data-stu-id="91738-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="91738-128">Флаги в параметре _lpFlagList_ находятся в том же порядке, что и записи в _lpAdrList._</span><span class="sxs-lookup"><span data-stu-id="91738-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="91738-129">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="91738-129">The following flags can be set:</span></span>
    
<span data-ttu-id="91738-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="91738-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="91738-131">Соответствующий получатель был разрешен, но не для уникального идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="91738-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="91738-132">Другие контейнеры не должны пытаться устранить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="91738-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="91738-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="91738-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="91738-134">Соответствующий получатель был решен с уникальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="91738-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="91738-135">Другие контейнеры не должны пытаться устранить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="91738-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="91738-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="91738-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="91738-137">Соответствующая запись не разрешена.</span><span class="sxs-lookup"><span data-stu-id="91738-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="91738-138">Другие контейнеры должны попытаться разрешить этот получатель.</span><span class="sxs-lookup"><span data-stu-id="91738-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="91738-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91738-139">Return value</span></span>

<span data-ttu-id="91738-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="91738-140">S_OK</span></span> 
  
> <span data-ttu-id="91738-141">Процесс разрешения имен был успешным.</span><span class="sxs-lookup"><span data-stu-id="91738-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="91738-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="91738-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="91738-143">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="91738-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="91738-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="91738-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="91738-145">Поставщик адресных книг не поддерживает массовое разрешение имен с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="91738-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91738-146">Примечания</span><span class="sxs-lookup"><span data-stu-id="91738-146">Remarks</span></span>

<span data-ttu-id="91738-147">Метод **ResolveNames** пытается связать неурегулированных получателей из массива записей в параметре  _lpAdrList_ с получателями в этом контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="91738-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="91738-148">Неурегулированный получатель обычно имеет только **свойство PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)и, возможно, несколько других свойств.</span><span class="sxs-lookup"><span data-stu-id="91738-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="91738-149">Неурегулированный получатель не имеет **свойства PR_ENTRYID** [(PidTagEntryId),](pidtagentryid-canonical-property.md)а соответствующий флаг в параметре  _lpFlagList_ задан для MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="91738-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="91738-150">И наоборот, у разрешенного получателя всегда есть по крайней мере **свойство PR_ENTRYID** плюс несколько других свойств, таких как **PR_EMAIL_ADDRESS** [(PidTagEmailAddress),](pidtagemailaddress-canonical-property.md) **PR_DISPLAY_NAME** и **PR_ADDRTYPE** [(PidTagAddressType).](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="91738-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="91738-151">Разрешение имен обычно начинается, когда клиент вызывает [метод IAddrBook::ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="91738-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="91738-152">Outlook MAPI отвечает вызовом метода **ResolveNames** каждого контейнера адресной книги, включенного в путь поиска адресной книги, указанного в свойстве **PR_AB_SEARCH_PATH** [(PidTagAbSearchPath).](pidtagabsearchpath-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="91738-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="91738-153">Записи в  _параметре lpAdrList_ включают получателей, уже решенных, поскольку они находятся в контейнерах, для которых MAPI уже называется **ResolveNames,** так как записи отображаются ранее в пути поиска.</span><span class="sxs-lookup"><span data-stu-id="91738-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="91738-154">Каждый контейнер пытается устранить неурегулированные записи, сообразуя имя отображения получателя с отображаемой именем одной из его записей.</span><span class="sxs-lookup"><span data-stu-id="91738-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="91738-155">При обнаружении уникального совпадения  **ResolveNames** добавляет свойство PR_ENTRYID и другие свойства, включенные в параметр _lpPropTagArray,_ к соответствующей записи в исходячей структуре **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="91738-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="91738-156">**Затем ResolveNames** задает запись в параметре  _lpFlagList_ для MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="91738-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="91738-157">Идентификатор записи, хранимый в **свойстве PR_ENTRYID,** может быть краткосрочным или долгосрочным.</span><span class="sxs-lookup"><span data-stu-id="91738-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="91738-158">После того как все контейнеры в пути поиска попытались разрешить имя, MAPI открывает диалоговое окно, по возможности, чтобы подсказать пользователю помощь в разрешении оставшихся конфликтов.</span><span class="sxs-lookup"><span data-stu-id="91738-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="91738-159">Клиенты также могут использовать возвращенную **структуру ADRLIST** в вызовах к методу [IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="91738-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="91738-160">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="91738-160">Notes to implementers</span></span>

<span data-ttu-id="91738-161">Не требуется поддерживать разрешение имен методом **ResolveNames.**</span><span class="sxs-lookup"><span data-stu-id="91738-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="91738-162">Вместо этого или дополнительно вы можете поддерживать его с помощью **ограничения** PR_ANR [(PidTagAnr).](pidtaganr-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="91738-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="91738-163">Если вы решите полагаться на **ограничение** PR_ANR для разрешения имен, вы можете MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="91738-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="91738-164">For more information, see [���������� ���������� ����](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="91738-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="91738-165">Установите запись флага получателя в параметре  _lpFlagList_ MAPI_UNRESOLVED, если получатель не совпадает ни с одним из получателей контейнера.</span><span class="sxs-lookup"><span data-stu-id="91738-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="91738-166">Если получатель соответствует нескольким получателям, установите его флаг MAPI_AMBIGUOUS и не измените структуру **ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="91738-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="91738-167">MAPI требует определенных свойств для получателей, включенных в список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="91738-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="91738-168">Их можно включить в структуру **ADRENTRY** в процессе разрешения имен или дождаться, когда MAPI запросит их с вызовами в [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) и [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md)</span><span class="sxs-lookup"><span data-stu-id="91738-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="91738-169">Эти дополнительные вызовы можно устранить и повысить производительность, включив следующие свойства в **структуры ADRENTRY** всех разрешенных получателей:</span><span class="sxs-lookup"><span data-stu-id="91738-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="91738-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="91738-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="91738-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="91738-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="91738-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="91738-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="91738-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="91738-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="91738-174">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="91738-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="91738-175">**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="91738-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="91738-176">**PR_TRANSMITABLE_DISPLAY_NAME** [(PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="91738-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="91738-177">Если некоторые свойства в параметре  _lpPropTagArray_ недоступны, как правило, из-за того, что запись контейнера не поддерживает свойства и они не включены в член **ADRENTRY** получателя в структуре **ADRLIST,** установите тип свойства каждого недоступного свойства PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="91738-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="91738-178">Не удалять свойства из структуры **ADRENTRY** решенного получателя.</span><span class="sxs-lookup"><span data-stu-id="91738-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="91738-179">Если необходимо заменить, а не изменять структуру **ADRENTRY,** сначала освободите оригинальную структуру **ADRENTRY,** назвав функцию [MAPIFreeBuffer,](mapifreebuffer.md) а затем распределите структуру **ADRENTRY** на [MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="91738-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="91738-180">См. также</span><span class="sxs-lookup"><span data-stu-id="91738-180">See also</span></span>



[<span data-ttu-id="91738-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="91738-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="91738-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="91738-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="91738-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="91738-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="91738-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="91738-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="91738-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="91738-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="91738-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="91738-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="91738-187">Каноническое свойство PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="91738-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="91738-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="91738-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="91738-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="91738-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

