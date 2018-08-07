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
ms.openlocfilehash: ed87a2a6e3232cec492da6be032cf54cd66c3772
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808718"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="98ec6-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="98ec6-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="98ec6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98ec6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98ec6-105">Выполняет разрешение имен для одного или нескольких получателей записей.</span><span class="sxs-lookup"><span data-stu-id="98ec6-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="98ec6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98ec6-106">Parameters</span></span>

 <span data-ttu-id="98ec6-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="98ec6-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="98ec6-108">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, описывающий свойства, которые нужно включить в структуре [ADRLIST](adrlist.md) , возвращенных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="98ec6-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="98ec6-109">Чтобы запросить поставщика по умолчанию набор свойств, передайте в параметре _lpPropTagArray_ NULL.</span><span class="sxs-lookup"><span data-stu-id="98ec6-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="98ec6-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="98ec6-110">_ulFlags_</span></span>
  
> <span data-ttu-id="98ec6-111">[in] Битовая маска флаги, определяющее тип текста в возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="98ec6-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="98ec6-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="98ec6-112">The following flags can be set:</span></span>
    
<span data-ttu-id="98ec6-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="98ec6-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="98ec6-114">Будет найден только совпадения адрес точное прокси-сервера; Частичный совпадения, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="98ec6-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="98ec6-115">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="98ec6-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="98ec6-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="98ec6-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="98ec6-117">Автономная адресная книга будет использоваться для выполнения разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="98ec6-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="98ec6-118">Например можно использовать этот флаг для включения в клиентское приложение для открытия глобальном списке адресов (GAL) в режиме кэширования данных exchange и доступа к записи в этот список адресов из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="98ec6-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="98ec6-119">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="98ec6-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="98ec6-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98ec6-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="98ec6-121">Возвращенная строка условий в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="98ec6-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="98ec6-122">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="98ec6-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="98ec6-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="98ec6-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="98ec6-124">[in, out] На входе указатель на структуру **ADRLIST** , содержащий список получателей разрешения.</span><span class="sxs-lookup"><span data-stu-id="98ec6-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="98ec6-125">На выходе указатель на структуру **ADRLIST** , содержащий возможности разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="98ec6-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="98ec6-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="98ec6-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="98ec6-127">[in, out] Указатель на массив флаги, каждый соответствующий на структуру [ADRENTRY](adrentry.md) в параметре _lpAdrList_ флаг, который предоставляет информацию о состоянии операцию разрешения имени для получателя.</span><span class="sxs-lookup"><span data-stu-id="98ec6-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="98ec6-128">Флаги в параметре _lpFlagList_ , в том же порядке, как записи в _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="98ec6-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="98ec6-129">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="98ec6-129">The following flags can be set:</span></span>
    
<span data-ttu-id="98ec6-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="98ec6-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="98ec6-131">Была устранена, соответствующего получателю, но не уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="98ec6-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="98ec6-132">Другие контейнеры не рекомендуется для устранения этой получателя.</span><span class="sxs-lookup"><span data-stu-id="98ec6-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="98ec6-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="98ec6-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="98ec6-134">Уникальный идентификатор проблема устранена соответствующего получателя.</span><span class="sxs-lookup"><span data-stu-id="98ec6-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="98ec6-135">Другие контейнеры не рекомендуется для устранения этой получателя.</span><span class="sxs-lookup"><span data-stu-id="98ec6-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="98ec6-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="98ec6-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="98ec6-137">Запись не разрешен.</span><span class="sxs-lookup"><span data-stu-id="98ec6-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="98ec6-138">Другие контейнеры должны пытаться разрешить этому получателю.</span><span class="sxs-lookup"><span data-stu-id="98ec6-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98ec6-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="98ec6-140">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="98ec6-140">S_OK</span></span> 
  
> <span data-ttu-id="98ec6-141">Процесс разрешения имен прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="98ec6-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="98ec6-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="98ec6-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="98ec6-143">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="98ec6-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="98ec6-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="98ec6-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="98ec6-145">Поставщик адресной книги не поддерживает массовое разрешение имен с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="98ec6-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98ec6-146">Замечания</span><span class="sxs-lookup"><span data-stu-id="98ec6-146">Remarks</span></span>

<span data-ttu-id="98ec6-147">Метод **ResolveNames** пытается сопоставить нерешенные получателей из массива записей с помощью параметра _lpAdrList_ список получателей в этот контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="98ec6-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="98ec6-148">Неизвестный получатель обычно имеет только свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и возможно несколько других свойств.</span><span class="sxs-lookup"><span data-stu-id="98ec6-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="98ec6-149">Неизвестный получатель не имеет свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) и его соответствующий флаг в параметре _lpFlagList_ задано значение MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="98ec6-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="98ec6-150">С другой стороны разрешенных получателя всегда имеет по крайней мере **PR_ENTRYID** свойства, а также некоторые другие свойства, такие как **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**и **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98ec6-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="98ec6-151">Разрешение имен обычно запускается, когда клиент вызывает метод [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="98ec6-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="98ec6-152">Outlook MAPI отвечает путем вызова метода **ResolveNames** каждого контейнер адресной книги, включенных в путь поиска книги адрес, указанный в свойстве **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98ec6-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="98ec6-153">Операции с помощью параметра _lpAdrList_ включают получателей, уже разрешить, так как они находятся в контейнеров, для которых MAPI уже вызван **ResolveNames**, так как записи ранее в путь поиска.</span><span class="sxs-lookup"><span data-stu-id="98ec6-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="98ec6-154">Каждый контейнер предпринимается попытка разрешить нерешенные записи соответствующей отображаемое имя получателя, с отображаемым именем одного из его записи.</span><span class="sxs-lookup"><span data-stu-id="98ec6-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="98ec6-155">При обнаружении уникальное соответствие **ResolveNames** добавляет свойство **PR_ENTRYID** и других свойств, содержащихся в параметре _lpPropTagArray_ соответствующей записи в структуре исходящей **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="98ec6-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="98ec6-156">Затем **ResolveNames** задает запись в параметре _lpFlagList_ MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="98ec6-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="98ec6-157">Идентификатор записи, хранящиеся в свойстве **PR_ENTRYID** может быть Краткосрочные или продолжительные.</span><span class="sxs-lookup"><span data-stu-id="98ec6-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="98ec6-158">В конце концов контейнеров в поиск путь предпринята процесса разрешения имен, MAPI открывает диалоговое окно, если это возможно, чтобы запрашивать у пользователя за помощью в устранении любые оставшиеся.</span><span class="sxs-lookup"><span data-stu-id="98ec6-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="98ec6-159">Клиенты могут также использовать возвращенный структура **ADRLIST** вызовы метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="98ec6-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="98ec6-160">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="98ec6-160">Notes to implementers</span></span>

<span data-ttu-id="98ec6-161">Вам не требуется для поддержки разрешение имен с помощью метода **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="98ec6-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="98ec6-162">Вместо этого, и Кроме того он может поддерживать с ограничением свойство **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98ec6-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="98ec6-163">Если вы решили зависеть от **PR_ANR** ограничения для разрешения имен, можно вернуть MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="98ec6-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="98ec6-164">For more information, see [���������� ���������� ����](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="98ec6-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="98ec6-165">Установите флаг запись получателя в параметре _lpFlagList_ MAPI_UNRESOLVED, если получатель не соответствует контейнер получателей.</span><span class="sxs-lookup"><span data-stu-id="98ec6-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="98ec6-166">Если получателя соответствует нескольким получателям, установить его флаг MAPI_AMBIGUOUS и не изменяйте его структуры **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="98ec6-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="98ec6-167">MAPI требуется определенных свойств для получателей, которые включены в список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="98ec6-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="98ec6-168">Можно включить их в структуре **ADRENTRY** как часть процесса разрешения имен или дождитесь MAPI запросить их с помощью вызовов методов [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) и [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="98ec6-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="98ec6-169">Можно исключить эти дополнительные вызовы и повысить производительность, включая следующие свойства в структуре **ADRENTRY** все возможности разрешения получателей:</span><span class="sxs-lookup"><span data-stu-id="98ec6-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="98ec6-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="98ec6-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="98ec6-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="98ec6-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="98ec6-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="98ec6-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="98ec6-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="98ec6-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="98ec6-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="98ec6-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="98ec6-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="98ec6-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="98ec6-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="98ec6-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="98ec6-177">Некоторые свойства с помощью параметра _lpPropTagArray_ недоступны — обычно поддерживает запись контейнер свойств и они не включаются в член **ADRENTRY** получателя в структуре **ADRLIST** — Задайте тип свойства каждого свойства недоступен для PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="98ec6-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="98ec6-178">Не удаляйте все свойства из структуры **ADRENTRY** Разрешить получателя.</span><span class="sxs-lookup"><span data-stu-id="98ec6-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="98ec6-179">Если вам необходимо заменить, а не изменять структуру **ADRENTRY** , сведениям исходной структуры **ADRENTRY** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) , а затем распределите замены структура **ADRENTRY** с [ MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="98ec6-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="98ec6-180">См. также</span><span class="sxs-lookup"><span data-stu-id="98ec6-180">See also</span></span>



[<span data-ttu-id="98ec6-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="98ec6-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="98ec6-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="98ec6-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="98ec6-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="98ec6-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="98ec6-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="98ec6-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="98ec6-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="98ec6-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="98ec6-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="98ec6-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="98ec6-187">Каноническое свойство PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="98ec6-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="98ec6-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="98ec6-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="98ec6-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="98ec6-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

