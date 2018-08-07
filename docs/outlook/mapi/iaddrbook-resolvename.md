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
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808753"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="d7abf-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="d7abf-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="d7abf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7abf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7abf-105">Выполняет разрешение имен, назначение идентификаторов запись для получателей в список получателей.</span><span class="sxs-lookup"><span data-stu-id="d7abf-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="d7abf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7abf-106">Parameters</span></span>

 <span data-ttu-id="d7abf-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d7abf-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d7abf-108">[in] Дескриптор родительского окна диалоговое окно, которое отображается, если указано, чтобы запрашивать у пользователя разрешение неопределенность.</span><span class="sxs-lookup"><span data-stu-id="d7abf-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="d7abf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7abf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d7abf-110">[in] Битовая маска флаги, определяющие различных аспектов процесса разрешения.</span><span class="sxs-lookup"><span data-stu-id="d7abf-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="d7abf-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="d7abf-111">The following flags can be set:</span></span>
    
<span data-ttu-id="d7abf-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="d7abf-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="d7abf-113">Указывает, что этот _lpszNewEntryTitle_ — это строка Юникод.</span><span class="sxs-lookup"><span data-stu-id="d7abf-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="d7abf-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="d7abf-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="d7abf-115">Для выполнения разрешения имен используйте автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d7abf-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="d7abf-116">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="d7abf-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="d7abf-117">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d7abf-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="d7abf-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d7abf-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d7abf-119">Отображает диалоговое окно запрашивать у пользователя для сведений о разрешении дополнительных имен.</span><span class="sxs-lookup"><span data-stu-id="d7abf-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="d7abf-120">Если этот флаг не установлен, диалоговое окно не отображается.</span><span class="sxs-lookup"><span data-stu-id="d7abf-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="d7abf-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d7abf-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d7abf-122">Указывает, что возвращаемые в списке адресов свойства должны быть в формате PT_UNICODE вместо PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="d7abf-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="d7abf-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="d7abf-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="d7abf-124">[in] Указатель на текст в поле заголовок элемента управления в диалоговом окне запрос на ввод получателя.</span><span class="sxs-lookup"><span data-stu-id="d7abf-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="d7abf-125">Заголовок может отличаться в зависимости от типа получателя.</span><span class="sxs-lookup"><span data-stu-id="d7abf-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="d7abf-126">Параметр _lpszNewEntryTitle_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d7abf-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d7abf-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="d7abf-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="d7abf-128">[входной-выходной параметр] Указатель на структуру [ADRLIST](adrlist.md) , содержащего список получателей разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="d7abf-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="d7abf-129">Эта структура **ADRLIST** могут создаваться с помощью метода [IAddrBook::Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="d7abf-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7abf-130">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d7abf-130">Return value</span></span>

<span data-ttu-id="d7abf-131">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d7abf-131">S_OK</span></span> 
  
> <span data-ttu-id="d7abf-132">Процесс разрешения имен выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="d7abf-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="d7abf-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="d7abf-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="d7abf-134">По крайней мере один получатель с помощью параметра _lpAdrList_ сопоставлен более одной операции в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="d7abf-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="d7abf-135">Как правило это значение возвращается, если флаг MAPI_DIALOG установлен, Запрет отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7abf-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="d7abf-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d7abf-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d7abf-137">Не удалось разрешить по крайней мере один получатель с помощью параметра _lpAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="d7abf-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="d7abf-138">Как правило это значение возвращается, если флаг MAPI_DIALOG установлен, Запрет отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d7abf-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d7abf-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7abf-139">Remarks</span></span>

<span data-ttu-id="d7abf-140">Клиенты и поставщики услуг вызовите метод **ResolveName** начать процесс разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="d7abf-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="d7abf-141">Нерешенные запись является записью, которая не имеет идентификатор записи или свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7abf-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="d7abf-142">**ResolveName** проходит через процесс для каждой нерешенные записи в списке адресов, переданной в параметре _lpAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="d7abf-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="d7abf-143">Если тип адреса получателя, соответствующий формат SMTP-адреса ( _displayname_@ _domain.top уровень домена_), **ResolveName** назначается идентификатор единичных записей.</span><span class="sxs-lookup"><span data-stu-id="d7abf-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="d7abf-144">Для каждого контейнера в свойстве **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) **ResolveName** вызывается метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="d7abf-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="d7abf-145">**ResolveNames** пытается сопоставить отображаемое имя каждого получателя, нерешенные с отображаемым именем, к которому относится к одному из его записи.</span><span class="sxs-lookup"><span data-stu-id="d7abf-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="d7abf-146">Если контейнер не поддерживает **ResolveNames**, **ResolveName** ограничивает контейнера содержимого таблицы с помощью ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7abf-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="d7abf-147">Это ограничение вызывает контейнер для выполнения типа «лучше всего подбора» поиск, чтобы найти получатель.</span><span class="sxs-lookup"><span data-stu-id="d7abf-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="d7abf-148">Все контейнеры должны поддерживать ограничение свойства **PR_ANR** .</span><span class="sxs-lookup"><span data-stu-id="d7abf-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="d7abf-149">При возвращении получателя, который соответствует несколько имен контейнером **ResolveName** отображает диалоговое окно, если установлен флаг MAPI_DIALOG, позволяющее пользователю выбрать правильное имя.</span><span class="sxs-lookup"><span data-stu-id="d7abf-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="d7abf-150">Если все контейнеров в свойстве **PR_AB_SEARCH_PATH** вызван и не найдено, получатель не устранена.</span><span class="sxs-lookup"><span data-stu-id="d7abf-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="d7abf-151">Если один или несколько получателей разрешены, **ResolveName** возвращает MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="d7abf-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="d7abf-152">Если неоднозначные решение, которое не удалось разрешить диалоговое окно с одного или нескольких получателей, или не был установлен флажок MAPI_DIALOG, **ResolveName** возвращает MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="d7abf-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="d7abf-153">Когда некоторых получателей неоднозначным и некоторые не может быть разрешен, **ResolveName** может вернуть либо значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="d7abf-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="d7abf-154">Если не удается разрешить имя, клиента можно создать указывает адрес, который имеет специально созданный адрес и идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d7abf-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="d7abf-155">Дополнительные сведения о формате идентификаторов единичных записей можно [Одноразовых идентификаторы записей](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="d7abf-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="d7abf-156">Дополнительные сведения о формате одноразовых адресов можно [Одноразовых адреса](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="d7abf-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="d7abf-157">MAPI поддерживает знаков Юникод для **ADRLIST** и новых параметров заголовка входа **ResolveName**; Если значение флага MAPI_UNICODE, в качестве типа PT_UNICODE структур [ADRENTRY](adrentry.md) возвращаются следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="d7abf-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="d7abf-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7abf-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7abf-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7abf-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7abf-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7abf-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="d7abf-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d7abf-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="d7abf-162">Свойство **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) всегда возвращается как тип PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="d7abf-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d7abf-163">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="d7abf-163">MFCMAPI reference</span></span>

<span data-ttu-id="d7abf-164">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="d7abf-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d7abf-165">**����**</span><span class="sxs-lookup"><span data-stu-id="d7abf-165">**File**</span></span>|<span data-ttu-id="d7abf-166">**�������**</span><span class="sxs-lookup"><span data-stu-id="d7abf-166">**Function**</span></span>|<span data-ttu-id="d7abf-167">**�����������**</span><span class="sxs-lookup"><span data-stu-id="d7abf-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7abf-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d7abf-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d7abf-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="d7abf-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="d7abf-170">Mfcmapi (en) использует метод **ResolveName** обрабатывать указывает адрес до его добавления к сообщению.</span><span class="sxs-lookup"><span data-stu-id="d7abf-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="d7abf-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d7abf-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d7abf-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="d7abf-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="d7abf-173">Mfcmapi (en) использует метод **ResolveName** для поиска запись книги по отображаемому имени.</span><span class="sxs-lookup"><span data-stu-id="d7abf-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7abf-174">См. также</span><span class="sxs-lookup"><span data-stu-id="d7abf-174">See also</span></span>



[<span data-ttu-id="d7abf-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d7abf-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="d7abf-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="d7abf-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="d7abf-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="d7abf-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="d7abf-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d7abf-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="d7abf-179">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d7abf-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

