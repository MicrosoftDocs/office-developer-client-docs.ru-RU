---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408133"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="af741-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="af741-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="af741-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af741-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af741-105">Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="af741-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="af741-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af741-106">Parameters</span></span>

 <span data-ttu-id="af741-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="af741-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="af741-108">[in] Handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span><span class="sxs-lookup"><span data-stu-id="af741-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="af741-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af741-109">_ulFlags_</span></span>
  
> <span data-ttu-id="af741-110">[in] Битоваяmas флагов, которые контролируют различные аспекты процесса разрешения.</span><span class="sxs-lookup"><span data-stu-id="af741-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="af741-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="af741-111">The following flags can be set:</span></span>
    
<span data-ttu-id="af741-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="af741-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="af741-113">Указывает,  _что lpszNewEntryTitle_ является строкой ЮНИКОДА.</span><span class="sxs-lookup"><span data-stu-id="af741-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="af741-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="af741-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="af741-115">Используйте только автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="af741-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="af741-116">Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="af741-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="af741-117">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="af741-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="af741-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="af741-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="af741-119">Отображает диалоговое окно с запросом дополнительных сведений о разрешении имен.</span><span class="sxs-lookup"><span data-stu-id="af741-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="af741-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="af741-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="af741-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af741-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af741-122">Указывает, что возвращаемая в списке адресов информация о свойствах должна иметь тип PT_UNICODE, а не PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="af741-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="af741-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="af741-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="af741-124">[in] Указатель на текст для заголовка управления в диалоговом окне с запросом ввода получателя.</span><span class="sxs-lookup"><span data-stu-id="af741-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="af741-125">Заголовок зависит от типа получателя.</span><span class="sxs-lookup"><span data-stu-id="af741-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="af741-126">Параметр  _lpszNewEntryTitle_ может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="af741-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="af741-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="af741-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="af741-128">[in-out] Указатель на [структуру ADRLIST,](adrlist.md) которая содержит список имен получателей, которые необходимо разрешить.</span><span class="sxs-lookup"><span data-stu-id="af741-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="af741-129">Эту **структуру ADRLIST** можно создать с помощью метода [IAddrBook::Address.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="af741-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af741-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af741-130">Return value</span></span>

<span data-ttu-id="af741-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="af741-131">S_OK</span></span> 
  
> <span data-ttu-id="af741-132">Процесс разрешения имен был успешно успешным.</span><span class="sxs-lookup"><span data-stu-id="af741-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="af741-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="af741-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="af741-134">По крайней мере один получатель в параметре  _lpAdrList_ соответствует нескольким записям в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="af741-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="af741-135">Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="af741-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="af741-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="af741-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="af741-137">Не удается разрешить хотя бы одного получателя в параметре _lpAdrList._</span><span class="sxs-lookup"><span data-stu-id="af741-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="af741-138">Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="af741-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="af741-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="af741-139">Remarks</span></span>

<span data-ttu-id="af741-140">Клиенты и поставщики услуг **звонят методу ResolveName,** чтобы инициировать процесс разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="af741-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="af741-141">Не разрешенная запись — это запись, у нее еще нет идентификатора записи **или** PR_ENTRYID ([PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="af741-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="af741-142">**ResolveName** проходит следующий процесс для каждой не разрешенной записи в списке адресов, переданной в _параметре lpAdrList._</span><span class="sxs-lookup"><span data-stu-id="af741-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="af741-143">Если тип адреса получателя соответствует формату SMTP-адреса  @  _(displayname domain.top-level-domain),_ **ResolveName** назначает ему одноуровневый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="af741-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="af741-144">Для каждого контейнера **в свойстве PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) **ResolveName** вызывает метод [IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="af741-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="af741-145">**ResolveNames** пытается найти отображаемую имя каждого неу разрешенного получателя с отображаемым именем, которое принадлежит одной из записей.</span><span class="sxs-lookup"><span data-stu-id="af741-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="af741-146">Если контейнер не поддерживает **ResolveNames,** **ResolveName** ограничивает таблицу содержимого контейнера с помощью ограничения свойства **PR_ANR** ([PidTagAnr).](pidtaganr-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="af741-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="af741-147">Это ограничение приводит к выполнению контейнером "наилучшего угадать" типа поиска, чтобы найти нужного получателя.</span><span class="sxs-lookup"><span data-stu-id="af741-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="af741-148">Все контейнеры должны поддерживать ограничение **PR_ANR** свойств.</span><span class="sxs-lookup"><span data-stu-id="af741-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="af741-149">Когда контейнер возвращает получателя, который соответствует нескольким именам, **ResolveName** отображает диалоговое окно, если установлен флаг MAPI_DIALOG, что позволяет пользователю выбрать правильное имя.</span><span class="sxs-lookup"><span data-stu-id="af741-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="af741-150">Если все контейнеры в  свойстве PR_AB_SEARCH_PATH были вызваны и совпадение не найдено, получатель остается не разрешенным.</span><span class="sxs-lookup"><span data-stu-id="af741-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="af741-151">Если один или несколько получателей не разрешены, **ResolveName** возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="af741-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="af741-152">Если у одного или более получателей было неоднозначное разрешение, которое не удалось разрешить с помощью диалоговых окне или из-за того, что флаг MAPI_DIALOG не установлен, **ResolveName** возвращает MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="af741-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="af741-153">Если некоторые получатели неоднозначны, а некоторые не могут быть разрешены, **ResolveName** может вернуть значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="af741-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="af741-154">Если имя не может быть разрешено, клиент может создать разовый адрес, который имеет специально отформатированный адрес и идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="af741-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="af741-155">Дополнительные сведения о формате идентификаторов одноаваторной записи см. в документе [One-Off Entry Identifiers.](one-off-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="af741-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="af741-156">Дополнительные сведения о формате разных адресов см. в этой [теме.](one-off-addresses.md)</span><span class="sxs-lookup"><span data-stu-id="af741-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="af741-157">MAPI поддерживает строки символов Юникода для **ADRLIST** и новые параметры заголовка записи **для ResolveName;** Если вы установите флаг MAPI_UNICODE, следующие свойства возвращаются как тип PT_UNICODE в структурах [ADRENTRY:](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="af741-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="af741-158">**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="af741-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="af741-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="af741-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="af741-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="af741-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="af741-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="af741-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="af741-162">Однако свойство **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName)](pidtag7bitdisplayname-canonical-property.md)всегда возвращается как тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="af741-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="af741-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="af741-163">MFCMAPI reference</span></span>

<span data-ttu-id="af741-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="af741-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="af741-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="af741-165">**File**</span></span>|<span data-ttu-id="af741-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="af741-166">**Function**</span></span>|<span data-ttu-id="af741-167">**�����������**</span><span class="sxs-lookup"><span data-stu-id="af741-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af741-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="af741-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="af741-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="af741-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="af741-170">MFCMAPI использует метод **ResolveName** для разрешения одноразового адреса перед его добавлением в сообщение.</span><span class="sxs-lookup"><span data-stu-id="af741-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="af741-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="af741-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="af741-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="af741-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="af741-173">MFCMAPI использует метод **ResolveName** для получения записи адресной книги по отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="af741-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af741-174">См. также</span><span class="sxs-lookup"><span data-stu-id="af741-174">See also</span></span>



[<span data-ttu-id="af741-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="af741-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="af741-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="af741-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="af741-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="af741-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="af741-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="af741-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="af741-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="af741-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

