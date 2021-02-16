---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405102"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="801f4-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="801f4-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="801f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="801f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="801f4-105">Добавляет нового получателя в контейнер адресной книги или в список получателей исходяного сообщения.</span><span class="sxs-lookup"><span data-stu-id="801f4-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a><span data-ttu-id="801f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="801f4-106">Parameters</span></span>

 <span data-ttu-id="801f4-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="801f4-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="801f4-108">[in] Handle to the parent window for the dialog box.</span><span class="sxs-lookup"><span data-stu-id="801f4-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="801f4-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="801f4-109">_ulFlags_</span></span>
  
> <span data-ttu-id="801f4-110">[in] Битоваяmas флагов, которая управляет типом используемого текста.</span><span class="sxs-lookup"><span data-stu-id="801f4-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="801f4-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="801f4-111">The following flag can be set:</span></span>
    
<span data-ttu-id="801f4-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="801f4-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="801f4-113">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="801f4-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="801f4-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="801f4-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="801f4-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="801f4-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="801f4-116">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="801f4-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="801f4-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="801f4-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="801f4-118">[in] Указатель на идентификатор записи контейнера, в который будет добавлен новый получатель.</span><span class="sxs-lookup"><span data-stu-id="801f4-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="801f4-119">Если параметр _cbEIDContainer_ имеет нулевое значение, метод **NewEntry** возвращает идентификатор записи получателя и список шаблонов, как если бы был вызван метод [IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md)</span><span class="sxs-lookup"><span data-stu-id="801f4-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="801f4-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="801f4-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="801f4-121">[in] Количество byte в идентификаторе записи, на который указывает параметр _lpEIDNewEntryTpl._</span><span class="sxs-lookup"><span data-stu-id="801f4-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="801f4-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="801f4-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="801f4-123">[in] Указатель на разротной шаблон, который будет использоваться для создания нового получателя.</span><span class="sxs-lookup"><span data-stu-id="801f4-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="801f4-124">Если  _cbEIDNewEntryTpl_ имеет нулевое значение, а  _lpEIDNewEntryTpl_ — NULL, **NewEntry** отображает диалоговое окно, в котором пользователь может выбрать из списка шаблонов для добавления новых записей.</span><span class="sxs-lookup"><span data-stu-id="801f4-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="801f4-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="801f4-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="801f4-126">[out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="801f4-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="801f4-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="801f4-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="801f4-128">[out] Указатель на указатель на идентификатор записи нового получателя.</span><span class="sxs-lookup"><span data-stu-id="801f4-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="801f4-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="801f4-129">Return value</span></span>

<span data-ttu-id="801f4-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="801f4-130">S_OK</span></span> 
  
> <span data-ttu-id="801f4-131">Новая запись адресной книги успешно создана.</span><span class="sxs-lookup"><span data-stu-id="801f4-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="801f4-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="801f4-132">Remarks</span></span>

<span data-ttu-id="801f4-133">Метод **NewEntry** создает новую запись адресной книги, которая добавляется непосредственно в контейнер или используется для обращения к исходя новому сообщению.</span><span class="sxs-lookup"><span data-stu-id="801f4-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="801f4-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="801f4-134">Notes to callers</span></span>

<span data-ttu-id="801f4-135">Если вы хотите добавить новую запись в определенный контейнер, задайте  _для lpEIDContainer_ идентификатор записи контейнера, а  _для cbEIDContainer_ количество в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="801f4-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="801f4-136">Если вы хотите добавить новую запись в список получателей исходячего сообщения, установите для  _lpEIDContainer_ значение NULL, а  _для cbEIDContainer_ значение n.</span><span class="sxs-lookup"><span data-stu-id="801f4-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="801f4-137">Если вы хотите разрешить пользователю клиентского приложения выбирать тип создаемой записи, передайте ноль  _в cbEIDNewEntryTpl_ и NULL в  _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="801f4-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="801f4-138">Метод **NewEntry** отображает одностолевую таблицу MAPI, список шаблонов, поддерживаемых MAPI и каждым поставщиком адресной книги в сеансе.</span><span class="sxs-lookup"><span data-stu-id="801f4-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="801f4-139">Каждый шаблон может создать запись получателя для одного или более типов адресов.</span><span class="sxs-lookup"><span data-stu-id="801f4-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="801f4-140">Если вы хотите сохранить идентификатор записи новой записи, передав допустимые указатели в параметрах _lpcbEIDNewEntry_ и _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="801f4-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="801f4-141">Вы несете ответственность за то, чтобы освободить этот идентификатор записи после завершения работы с ним путем вызова функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="801f4-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="801f4-142">Чтобы использовать определенный шаблон для добавления новой записи в измояемый контейнер, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="801f4-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="801f4-143">Вызовите метод [IMAPISession::OpenEntry,](imapisession-openentry.md) чтобы открыть контейнер назначения, и установите для параметра  _lpEntryID_ идентификатор записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="801f4-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="801f4-144">Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера назначения и установите для параметра  _ulPropTag_ PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates),](pidtagcreatetemplates-canonical-property.md)а для параметра  _lpiid_ — IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="801f4-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="801f4-145">Контейнер возвращает одностолевую таблицу со списком всех шаблонов, которые он поддерживает для создания новых записей.</span><span class="sxs-lookup"><span data-stu-id="801f4-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="801f4-146">Извлекает строку, представляюную шаблон для определенного типа записи, которую необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="801f4-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="801f4-147">Столбец **PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)указывает тип адреса, поддерживаемый шаблоном.</span><span class="sxs-lookup"><span data-stu-id="801f4-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="801f4-148">Вызовите **метод NewEntry** и установите  _для lpEIDNewEntryTpl_ идентификатор записи выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="801f4-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="801f4-149">Идентификатором записи будет **столбец PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)из строки шаблона в одноразовой таблице.</span><span class="sxs-lookup"><span data-stu-id="801f4-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="801f4-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="801f4-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="801f4-151">Передав допустимый указатель в  _параметре lppEIDNewEntry,_ если необходимо сохранить идентификатор записи новой записи.</span><span class="sxs-lookup"><span data-stu-id="801f4-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="801f4-152">См. также</span><span class="sxs-lookup"><span data-stu-id="801f4-152">See also</span></span>



[<span data-ttu-id="801f4-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="801f4-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="801f4-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="801f4-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="801f4-155">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="801f4-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="801f4-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="801f4-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

