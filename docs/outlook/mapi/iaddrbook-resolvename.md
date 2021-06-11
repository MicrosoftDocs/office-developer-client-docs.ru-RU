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
# <a name="iaddrbookresolvename"></a><span data-ttu-id="b4bd6-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="b4bd6-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="b4bd6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4bd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4bd6-105">Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="b4bd6-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="b4bd6-106">Parameters</span></span>

 <span data-ttu-id="b4bd6-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b4bd6-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b4bd6-108">[in] Ручка родительского окна диалоговое окно, которое показано, если указано, чтобы побудить пользователя к устранению двусмысленности.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="b4bd6-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b4bd6-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b4bd6-110">[in] Битмашка флагов, которые контролируют различные аспекты процесса разрешения.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="b4bd6-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b4bd6-111">The following flags can be set:</span></span>
    
<span data-ttu-id="b4bd6-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="b4bd6-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="b4bd6-113">Указывает, что  _lpszNewEntryTitle_ — это строка UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="b4bd6-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="b4bd6-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="b4bd6-115">Для выполнения разрешения имен используйте только офлайн-адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="b4bd6-116">Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="b4bd6-117">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="b4bd6-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b4bd6-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b4bd6-119">Отображает диалоговое окно, чтобы подсказыть пользователю дополнительные сведения о разрешении имен.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="b4bd6-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="b4bd6-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4bd6-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b4bd6-122">Указывает, что свойства, возвращенные в списке адресов, должны иметь тип PT_UNICODE, а не PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="b4bd6-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="b4bd6-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="b4bd6-124">[in] Указатель на текст для заголовка управления в диалоговом окне, который побуждает пользователя ввести получателя.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="b4bd6-125">Название зависит от типа получателя.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="b4bd6-126">Параметр  _lpszNewEntryTitle_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b4bd6-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="b4bd6-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="b4bd6-128">[в выходе] Указатель на [структуру ADRLIST,](adrlist.md) которая содержит список разрешенных имен получателей.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="b4bd6-129">Эта **структура ADRLIST** может быть создана методом [IAddrBook::Address.](iaddrbook-address.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b4bd6-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4bd6-130">Return value</span></span>

<span data-ttu-id="b4bd6-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4bd6-131">S_OK</span></span> 
  
> <span data-ttu-id="b4bd6-132">Процесс разрешения имен удался.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="b4bd6-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="b4bd6-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="b4bd6-134">По крайней мере один получатель  _в параметре lpAdrList_ совпадает с несколькими входами в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="b4bd6-135">Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="b4bd6-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b4bd6-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b4bd6-137">Не удается разрешить по крайней мере одного получателя в _параметре lpAdrList._</span><span class="sxs-lookup"><span data-stu-id="b4bd6-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="b4bd6-138">Обычно это значение возвращается при MAPI_DIALOG флага, запрещая отображение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b4bd6-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4bd6-139">Remarks</span></span>

<span data-ttu-id="b4bd6-140">Клиенты и поставщики услуг звонят по **методу ResolveName,** чтобы инициировать процесс разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="b4bd6-141">Неурегулированная запись — это запись, которая еще  не имеет идентификатора или PR_ENTRYID[(PidTagEntryId).](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="b4bd6-142">**ResolveName** проходит следующий процесс для каждой неурегулированной записи в списке адресов, переданных в _параметре lpAdrList._</span><span class="sxs-lookup"><span data-stu-id="b4bd6-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="b4bd6-143">Если тип адреса получателя придерживается формата SMTP-адреса _(имя_ @  _domain.top-level-domain),_ **ResolveName** назначает ему идентификатор одноуровневой записи.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="b4bd6-144">Для каждого контейнера **в свойстве PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md) **resolveName** вызывает [метод IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="b4bd6-145">**ResolveNames** пытается соответствовать отображаемого имени каждого неурегулированного получателя с отображаемым именем, которое принадлежит одной из его записей.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="b4bd6-146">Если контейнер не поддерживает **ResolveNames,** **ResolveName** ограничивает содержимое таблицы контейнера с помощью ограничения свойств **PR_ANR** [(PidTagAnr).](pidtaganr-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="b4bd6-147">Это ограничение приводит к выполнению контейнером поиска "наилучшего угадать", чтобы найти совпадающий получатель.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="b4bd6-148">Все контейнеры должны поддерживать ограничение **PR_ANR** свойств.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="b4bd6-149">Когда контейнер возвращает получателя, который соответствует нескольким именам, **ResolveName** отображает диалоговое окно, если MAPI_DIALOG флаг, который позволяет пользователю выбрать правильное имя.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="b4bd6-150">Если все контейнеры в  свойстве PR_AB_SEARCH_PATH были вызваны и не найдены совпадения, получатель остается неурегулированным.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="b4bd6-151">Если один или несколько получателей не разрешены, **ResolveName** возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="b4bd6-152">Если у одного или более получателей было неоднозначное разрешение, которое не удалось разрешить диалоговым окном, или из-за того, что флаг MAPI_DIALOG не установлен, **ResolveName** возвращается MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="b4bd6-153">Если некоторые из получателей неоднозначны, а некоторые не могут быть устранены, **ResolveName** может вернуть значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="b4bd6-154">Если имя не удается разрешить, клиент может создать разовый адрес, который имеет специально отформатированный адрес и идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="b4bd6-155">Дополнительные сведения о формате идентификаторов одноавтной записи см. в документе [One-Off Entry Identifiers.](one-off-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="b4bd6-156">Дополнительные сведения о формате разных адресов см. в [одном из них.](one-off-addresses.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="b4bd6-157">MAPI поддерживает строки символов Юникод для **ADRLIST** и новые параметры заголовка входа **в ResolveName;** Если задать флаг MAPI_UNICODE, следующие свойства возвращаются в виде PT_UNICODE в [структурах ADRENTRY:](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="b4bd6-158">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="b4bd6-159">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="b4bd6-160">**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="b4bd6-161">**PR_TRANSMITABLE_DISPLAY_NAME** [(PidTagTransmittableDisplayName)](pidtagtransmittabledisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b4bd6-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="b4bd6-162">Однако свойство **PR_7BIT_DISPLAY_NAME** [(PidTag7BitDisplayName)](pidtag7bitdisplayname-canonical-property.md)всегда возвращается как тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b4bd6-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b4bd6-163">MFCMAPI reference</span></span>

<span data-ttu-id="b4bd6-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b4bd6-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b4bd6-165">**File**</span></span>|<span data-ttu-id="b4bd6-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b4bd6-166">**Function**</span></span>|<span data-ttu-id="b4bd6-167">**�����������**</span><span class="sxs-lookup"><span data-stu-id="b4bd6-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4bd6-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b4bd6-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b4bd6-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="b4bd6-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="b4bd6-170">MFCMAPI использует метод **ResolveName** для решения разового адреса перед добавлением его в сообщение.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="b4bd6-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b4bd6-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b4bd6-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="b4bd6-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="b4bd6-173">MFCMAPI использует метод **ResolveName** для получения записи адресной книги по имени отображения.</span><span class="sxs-lookup"><span data-stu-id="b4bd6-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4bd6-174">См. также</span><span class="sxs-lookup"><span data-stu-id="b4bd6-174">See also</span></span>



[<span data-ttu-id="b4bd6-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="b4bd6-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="b4bd6-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="b4bd6-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="b4bd6-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="b4bd6-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="b4bd6-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b4bd6-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="b4bd6-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b4bd6-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

