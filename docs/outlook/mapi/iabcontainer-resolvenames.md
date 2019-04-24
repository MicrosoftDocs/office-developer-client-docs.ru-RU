---
title: Иабконтаинерресолвенамес
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279572"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="c388a-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c388a-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="c388a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c388a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c388a-105">Выполняет разрешение имен для одной или нескольких записей получателей.</span><span class="sxs-lookup"><span data-stu-id="c388a-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="c388a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c388a-106">Parameters</span></span>

 <span data-ttu-id="c388a-107">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="c388a-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c388a-108">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, описывающих свойства, которые необходимо включить в структуру [ADRLIST](adrlist.md) , возвращаемую поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c388a-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="c388a-109">Чтобы запросить набор свойств поставщика по умолчанию, передайте значение NULL в параметр _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="c388a-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="c388a-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c388a-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c388a-111">возврата Битовая маска флагов, определяющая тип текста в возвращаемых строках.</span><span class="sxs-lookup"><span data-stu-id="c388a-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="c388a-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c388a-112">The following flags can be set:</span></span>
    
<span data-ttu-id="c388a-113">ЕМС_АБ_АДДРЕСС_ЛУКУП</span><span class="sxs-lookup"><span data-stu-id="c388a-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="c388a-114">Будут найдены только точные соответствия адресов прокси-серверов; частичное совпадение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c388a-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="c388a-115">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="c388a-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="c388a-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c388a-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="c388a-117">Для разрешения имен будет использоваться только автономная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="c388a-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="c388a-118">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="c388a-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c388a-119">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="c388a-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="c388a-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c388a-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c388a-121">Возвращаемые строковые свойства представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="c388a-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="c388a-122">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="c388a-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c388a-123">_Лпадрлист_</span><span class="sxs-lookup"><span data-stu-id="c388a-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="c388a-124">[вход, выход] В поле input — указатель на структуру **ADRLIST** , которая содержит список получателей, которые требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="c388a-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="c388a-125">В выходных данных — указатель на структуру **ADRLIST** , которая содержит разрешенные имена.</span><span class="sxs-lookup"><span data-stu-id="c388a-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="c388a-126">_Лпфлаглист_</span><span class="sxs-lookup"><span data-stu-id="c388a-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="c388a-127">[вход, выход] Указатель на массив флагов, каждый флаг которого соответствует структуре [адрентри](adrentry.md) в параметре _лпадрлист_ , который предоставляет состояние операции разрешения имен для получателя.</span><span class="sxs-lookup"><span data-stu-id="c388a-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="c388a-128">Флаги в параметре _лпфлаглист_ расположены в том же порядке, что и записи в _лпадрлист_.</span><span class="sxs-lookup"><span data-stu-id="c388a-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="c388a-129">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c388a-129">The following flags can be set:</span></span>
    
<span data-ttu-id="c388a-130">МАПИ_АМБИГУАУС</span><span class="sxs-lookup"><span data-stu-id="c388a-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="c388a-131">Соответствующий получатель разрешен, но не является уникальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="c388a-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="c388a-132">Другие контейнеры не должны пытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="c388a-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="c388a-133">МАПИ_РЕСОЛВЕД</span><span class="sxs-lookup"><span data-stu-id="c388a-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="c388a-134">Соответствующий получатель был сопоставлен с уникальным идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="c388a-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="c388a-135">Другие контейнеры не должны пытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="c388a-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="c388a-136">МАПИ_УНРЕСОЛВЕД</span><span class="sxs-lookup"><span data-stu-id="c388a-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="c388a-137">Соответствующая запись не была устранена.</span><span class="sxs-lookup"><span data-stu-id="c388a-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="c388a-138">Другие контейнеры должны попытаться разрешить этого получателя.</span><span class="sxs-lookup"><span data-stu-id="c388a-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c388a-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c388a-139">Return value</span></span>

<span data-ttu-id="c388a-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="c388a-140">S_OK</span></span> 
  
> <span data-ttu-id="c388a-141">Процесс разрешения имен выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c388a-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="c388a-142">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="c388a-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c388a-143">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="c388a-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="c388a-144">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="c388a-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="c388a-145">Поставщик адресных книг не поддерживает массовое разрешение имен с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="c388a-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c388a-146">Замечания</span><span class="sxs-lookup"><span data-stu-id="c388a-146">Remarks</span></span>

<span data-ttu-id="c388a-147">Метод **ResolveNames** пытается сопоставлять неразрешенных получателей из массива записей параметра _лпадрлист_ с получателями в этом контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c388a-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="c388a-148">У неизвестного получателя обычно есть только свойство **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) и, возможно, несколько других свойств.</span><span class="sxs-lookup"><span data-stu-id="c388a-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="c388a-149">Нераспознанный получатель не имеет свойства **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)), а соответствующий флаг в параметре _лпфлаглист_ имеет значение мапи_унресолвед.</span><span class="sxs-lookup"><span data-stu-id="c388a-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="c388a-150">И наоборот, у разрешенного получателя всегда есть по крайней мере свойство **пр_ентрид** , а также некоторые другие свойства, такие как **пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **пр_дисплай_наме**и **пр_аддртипе** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c388a-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="c388a-151">Разрешение имен обычно начинается, когда клиент вызывает метод [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="c388a-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="c388a-152">Outlook MAPI отвечает, вызывая метод **ResolveNames** каждого контейнера адресных книг, включенных в путь для поиска в адресной книге, заданный свойством **пр_аб_сеарч_пас** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c388a-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="c388a-153">Записи в параметре _лпадрлист_ включают получателей, которые уже разрешены, так как они находятся в контейнерах, для которых MAPI уже вызывал **ResolveNames**, так как записи отображаются ранее в пути поиска.</span><span class="sxs-lookup"><span data-stu-id="c388a-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="c388a-154">Каждый контейнер пытается разрешить неразрешенные записи, выполнив сопоставление отображаемого имени получателя с отображаемым именем одной из записей.</span><span class="sxs-lookup"><span data-stu-id="c388a-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="c388a-155">Если найдено уникальное соответствие, **ResolveNames** добавляет свойство **пр_ентрид** и другие свойства, включенные в параметр _лппроптагаррай_ , в соответствующую запись в структуре исходящих **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="c388a-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="c388a-156">Затем **ResolveNames** задает для записи в параметре _лпфлаглист_ значение мапи_ресолвед.</span><span class="sxs-lookup"><span data-stu-id="c388a-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="c388a-157">Идентификатор записи, хранящийся в свойстве **пр_ентрид** , может быть краткосрочным или долгосрочным.</span><span class="sxs-lookup"><span data-stu-id="c388a-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="c388a-158">После того как все контейнеры, указанные в пути поиска, попытались выполнить разрешение имен, MAPI открывает диалоговое окно, если это возможно, чтобы запросить у пользователя помощь по устранению оставшихся конфликтов.</span><span class="sxs-lookup"><span data-stu-id="c388a-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="c388a-159">Клиенты также могут использовать возвращенную структуру **ADRLIST** в вызовах метода [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="c388a-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c388a-160">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c388a-160">Notes to implementers</span></span>

<span data-ttu-id="c388a-161">Не требуется поддержка разрешения имен с помощью метода **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="c388a-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="c388a-162">Вместо этого или Кроме того, вы можете поддерживать его с помощью ограничения свойства **пр_анр** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c388a-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="c388a-163">Если вы решили использовать ограничение **пр_анр** для разрешения имен, вы можете вернуть мапи_е_но_суппорт.</span><span class="sxs-lookup"><span data-stu-id="c388a-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="c388a-164">For more information, see [���������� ���������� ����](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="c388a-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="c388a-165">Установите для записи флага получателя в параметре _лпфлаглист_ значение мапи_унресолвед, если получатель не отвечает ни одному из получателей контейнера.</span><span class="sxs-lookup"><span data-stu-id="c388a-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="c388a-166">Если получатель соответствует нескольким получателям, установите для него флаг МАПИ_АМБИГУАУС и не изменяйте его структуру **адрентри** .</span><span class="sxs-lookup"><span data-stu-id="c388a-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="c388a-167">Для MAPI требуются определенные свойства получателей, включенных в список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="c388a-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="c388a-168">Вы можете включить их в структуру **адрентри** как часть процесса разрешения имен или подождать, пока MAPI запросит их, выполнив вызовы [IAddrBook::P репаререЦипс](iaddrbook-preparerecips.md) и [имаписуппорт:: експандреЦипс](imapisupport-expandrecips.md) методы.</span><span class="sxs-lookup"><span data-stu-id="c388a-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="c388a-169">Вы можете устранить эти дополнительные вызовы и увеличить производительность, включив следующие свойства в структуры **адрентри** всех разрешенных получателей:</span><span class="sxs-lookup"><span data-stu-id="c388a-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="c388a-170">**ПР_АДДРТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="c388a-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="c388a-171">**ПР_ДИСПЛАЙ_НАМЕ**</span><span class="sxs-lookup"><span data-stu-id="c388a-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="c388a-172">**ПР_ЕМАИЛ_АДДРЕСС**</span><span class="sxs-lookup"><span data-stu-id="c388a-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="c388a-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="c388a-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="c388a-174">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c388a-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c388a-175">**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c388a-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="c388a-176">**Пр_трансмитабле_дисплай_наме** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c388a-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="c388a-177">Если некоторые свойства в параметре _лппроптагаррай_ недоступны (обычно это вызвано тем, что запись контейнера не поддерживает свойства и не включается в элемент **адрентри** получателя в структуре **ADRLIST** ), Задайте для каждого недоступного свойства тип свойства ПТ_ЕРРОР.</span><span class="sxs-lookup"><span data-stu-id="c388a-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="c388a-178">Не удаляйте свойства из разрешенной структуры **адрентри** получателя.</span><span class="sxs-lookup"><span data-stu-id="c388a-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="c388a-179">Если вместо изменения структуры **адрентри** необходимо заменить, сначала удалите исходную структуру **адрентри** , вызвав функцию [мапифрибуффер](mapifreebuffer.md) , а затем выделяйте структуру replacement **адрентри** с [ Мапиаллокатебуффер](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c388a-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c388a-180">См. также</span><span class="sxs-lookup"><span data-stu-id="c388a-180">See also</span></span>



[<span data-ttu-id="c388a-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="c388a-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="c388a-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c388a-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="c388a-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="c388a-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="c388a-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="c388a-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="c388a-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="c388a-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="c388a-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="c388a-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="c388a-187">Каноническое свойство PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="c388a-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="c388a-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="c388a-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="c388a-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c388a-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

