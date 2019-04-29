---
title: Иаддрбукресолвенаме
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
# <a name="iaddrbookresolvename"></a><span data-ttu-id="ad20b-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="ad20b-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="ad20b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad20b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad20b-105">Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="ad20b-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="ad20b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad20b-106">Parameters</span></span>

 <span data-ttu-id="ad20b-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="ad20b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ad20b-108">возврата Дескриптор родительского окна диалогового окна, который отображается, если он указан, чтобы запросить разрешение на неоднозначность.</span><span class="sxs-lookup"><span data-stu-id="ad20b-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="ad20b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad20b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ad20b-110">возврата Битовая маска флагов, которые управляют различными аспектами процесса разрешения.</span><span class="sxs-lookup"><span data-stu-id="ad20b-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="ad20b-111">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="ad20b-111">The following flags can be set:</span></span>
    
<span data-ttu-id="ad20b-112">АБ_УНИКОДЕУИ</span><span class="sxs-lookup"><span data-stu-id="ad20b-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="ad20b-113">Указывает, что _лпсзневентрититле_ является строкой Юникода.</span><span class="sxs-lookup"><span data-stu-id="ad20b-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="ad20b-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="ad20b-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="ad20b-115">Для разрешения имен используйте только автономную адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="ad20b-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="ad20b-116">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ad20b-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="ad20b-117">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="ad20b-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="ad20b-118">МАПИ_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="ad20b-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="ad20b-119">Отображает диалоговое окно, в котором пользователю предлагается ввести дополнительные сведения о разрешении имен.</span><span class="sxs-lookup"><span data-stu-id="ad20b-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="ad20b-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="ad20b-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="ad20b-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad20b-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ad20b-122">Указывает, что свойства, возвращаемые в списке адресов, должны иметь тип ПТ_УНИКОДЕ, а не PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ad20b-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="ad20b-123">_Лпсзневентрититле_</span><span class="sxs-lookup"><span data-stu-id="ad20b-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="ad20b-124">возврата Указатель на текст заголовка элемента управления в диалоговом окне, предлагающий пользователю ввести получателя.</span><span class="sxs-lookup"><span data-stu-id="ad20b-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="ad20b-125">Название зависит от типа получателя.</span><span class="sxs-lookup"><span data-stu-id="ad20b-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="ad20b-126">Параметр _лпсзневентрититле_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="ad20b-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ad20b-127">_Лпадрлист_</span><span class="sxs-lookup"><span data-stu-id="ad20b-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="ad20b-128">[по истечении] Указатель на структуру [ADRLIST](adrlist.md) , которая содержит список имен получателей, которые требуется разрешить.</span><span class="sxs-lookup"><span data-stu-id="ad20b-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="ad20b-129">Эту структуру **ADRLIST** можно создать с помощью метода [IAddrBook:: Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="ad20b-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ad20b-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad20b-130">Return value</span></span>

<span data-ttu-id="ad20b-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad20b-131">S_OK</span></span> 
  
> <span data-ttu-id="ad20b-132">Процесс разрешения имен выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ad20b-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="ad20b-133">МАПИ_Е_АМБИГУАУС_РЕЦИП</span><span class="sxs-lookup"><span data-stu-id="ad20b-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="ad20b-134">По крайней мере один получатель в параметре _лпадрлист_ сопоставлен с более чем одной записью в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="ad20b-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="ad20b-135">Обычно это значение возвращается, если установлен флаг МАПИ_ДИАЛОГ, запрещая отображение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ad20b-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="ad20b-136">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="ad20b-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ad20b-137">Не удается разрешить по крайней мере одного получателя в параметре _лпадрлист_ .</span><span class="sxs-lookup"><span data-stu-id="ad20b-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="ad20b-138">Обычно это значение возвращается, если установлен флаг МАПИ_ДИАЛОГ, запрещая отображение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ad20b-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ad20b-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad20b-139">Remarks</span></span>

<span data-ttu-id="ad20b-140">Клиенты и поставщики услуг вызывают метод **ресолвенаме** для запуска процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="ad20b-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="ad20b-141">Неразрешенная запись — это запись, у которой еще нет идентификатора записи или свойства **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ad20b-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="ad20b-142">**Ресолвенаме** проходит следующий процесс для каждой неразрешенной записи в списке адресов, переданном параметром _лпадрлист_ .</span><span class="sxs-lookup"><span data-stu-id="ad20b-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="ad20b-143">Если тип адреса получателя соответствует формату SMTP-адреса (домен _DisplayName_@ _. верхний уровень — домен_), **ресолвенаме** назначает ему идентификатор одноразовой записи.</span><span class="sxs-lookup"><span data-stu-id="ad20b-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="ad20b-144">Для каждого контейнера в свойстве **пр_аб_сеарч_пас** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) **ресолвенаме** вызывает метод [иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="ad20b-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="ad20b-145">**ResolveNames** пытается найти отображаемое имя каждого неизвестного получателя с отображаемым именем, принадлежащим одной из записей.</span><span class="sxs-lookup"><span data-stu-id="ad20b-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="ad20b-146">Если контейнер не поддерживает **ResolveNames**, **ресолвенаме** ограничит таблицу содержимого контейнера с помощью ограничения свойства **пр_анр** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ad20b-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="ad20b-147">Это ограничение приводит к тому, что контейнер выполнит "лучший тип поиска", чтобы найти совпадающего получателя.</span><span class="sxs-lookup"><span data-stu-id="ad20b-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="ad20b-148">Все контейнеры должны поддерживать ограничение свойства **пр_анр** .</span><span class="sxs-lookup"><span data-stu-id="ad20b-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="ad20b-149">Если контейнер возвращает получателя, который соответствует нескольким именам, **ресолвенаме** отображает диалоговое окно, если установлен флаг мапи_диалог, который позволяет пользователю выбрать правильное имя.</span><span class="sxs-lookup"><span data-stu-id="ad20b-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="ad20b-150">Если были вызваны все контейнеры в свойстве **пр_аб_сеарч_пас** , а совпадения не найдены, получатель остается неразрешимым.</span><span class="sxs-lookup"><span data-stu-id="ad20b-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="ad20b-151">Если один или несколько получателей не разрешены, **ресолвенаме** возвращает мапи_е_нот_фаунд.</span><span class="sxs-lookup"><span data-stu-id="ad20b-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="ad20b-152">Если одному или нескольким получателям присвоено неоднозначное разрешение, которое не удалось разрешить с помощью диалогового окна, или не задано значение флага МАПИ_ДИАЛОГ, **ресолвенаме** возвращает мапи_е_амбигуаус_реЦип.</span><span class="sxs-lookup"><span data-stu-id="ad20b-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="ad20b-153">Если некоторые из получателей являются неоднозначными и не удается разрешить некоторые из них, **ресолвенаме** может возвращать значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad20b-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="ad20b-154">Если не удается разрешить имя, клиент может создать один адрес с особым отформатированным адресом и идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="ad20b-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="ad20b-155">Дополнительные сведения о формате одноразовых идентификаторов записей можно узнать в статье одноразовые [идентификаторы записей](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="ad20b-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="ad20b-156">Более подробную информацию о формате одноразовых адресов можно узнать в разделе [одноразовЫе адреса](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="ad20b-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="ad20b-157">MAPI поддерживает строки символов Юникода для **ADRLIST** и новые параметры заголовка записи в **ресолвенаме**; При установке флага МАПИ_УНИКОДЕ следующие свойства возвращаются в виде типа ПТ_УНИКОДЕ в структурах [адрентри](adrentry.md) :</span><span class="sxs-lookup"><span data-stu-id="ad20b-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="ad20b-158">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad20b-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad20b-159">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad20b-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad20b-160">**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad20b-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad20b-161">**Пр_трансмитабле_дисплай_наме** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad20b-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="ad20b-162">Однако свойство **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) всегда возвращается как тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ad20b-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad20b-163">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ad20b-163">MFCMAPI reference</span></span>

<span data-ttu-id="ad20b-164">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ad20b-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad20b-165">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ad20b-165">**File**</span></span>|<span data-ttu-id="ad20b-166">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ad20b-166">**Function**</span></span>|<span data-ttu-id="ad20b-167">**�����������**</span><span class="sxs-lookup"><span data-stu-id="ad20b-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad20b-168">Мапиабфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="ad20b-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ad20b-169">Аддонеоффаддресс</span><span class="sxs-lookup"><span data-stu-id="ad20b-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="ad20b-170">MFCMAPI использует метод **ресолвенаме** , чтобы разрешить один адрес перед добавлением его в сообщение.</span><span class="sxs-lookup"><span data-stu-id="ad20b-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="ad20b-171">Мапиабфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="ad20b-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ad20b-172">АддреЦипиент</span><span class="sxs-lookup"><span data-stu-id="ad20b-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="ad20b-173">MFCMAPI использует метод **ресолвенаме** для поиска записи в адресной книге по отображаемому имени.</span><span class="sxs-lookup"><span data-stu-id="ad20b-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad20b-174">См. также</span><span class="sxs-lookup"><span data-stu-id="ad20b-174">See also</span></span>



[<span data-ttu-id="ad20b-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ad20b-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ad20b-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="ad20b-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="ad20b-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ad20b-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="ad20b-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ad20b-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ad20b-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ad20b-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

