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
# <a name="iaddrbooknewentry"></a><span data-ttu-id="80c15-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="80c15-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="80c15-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80c15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80c15-105">Добавляет нового получателя в контейнер адресной книги или в список получателей исходя из сообщения.</span><span class="sxs-lookup"><span data-stu-id="80c15-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="80c15-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="80c15-106">Parameters</span></span>

 <span data-ttu-id="80c15-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="80c15-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="80c15-108">[in] Ручка родительского окна для диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="80c15-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="80c15-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80c15-109">_ulFlags_</span></span>
  
> <span data-ttu-id="80c15-110">[in] Битмашка флагов, контролируемая типом используемого текста.</span><span class="sxs-lookup"><span data-stu-id="80c15-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="80c15-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="80c15-111">The following flag can be set:</span></span>
    
<span data-ttu-id="80c15-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80c15-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="80c15-113">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="80c15-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="80c15-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="80c15-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="80c15-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="80c15-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="80c15-116">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="80c15-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="80c15-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="80c15-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="80c15-118">[in] Указатель на идентификатор входа контейнера, в котором должен быть добавлен новый получатель.</span><span class="sxs-lookup"><span data-stu-id="80c15-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="80c15-119">Если параметр _cbEIDContainer_ нулевой, метод **NewEntry** возвращает идентификатор входа получателя и список шаблонов, как если бы был вызван метод [IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md)</span><span class="sxs-lookup"><span data-stu-id="80c15-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="80c15-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="80c15-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="80c15-121">[in] Количество byte в идентификаторе входа, на который указывает параметр _lpEIDNewEntryTpl._</span><span class="sxs-lookup"><span data-stu-id="80c15-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="80c15-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="80c15-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="80c15-123">[in] Указатель на разовую шаблон, которая будет использоваться для создания нового получателя.</span><span class="sxs-lookup"><span data-stu-id="80c15-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="80c15-124">Если  _cbEIDNewEntryTpl_ ноль, а  _lpEIDNewEntryTpl_ — NULL, **NewEntry** отображает диалоговое окно, с помощью которого пользователь может выбрать из списка шаблонов для добавления новых записей.</span><span class="sxs-lookup"><span data-stu-id="80c15-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="80c15-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="80c15-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="80c15-126">[вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="80c15-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="80c15-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="80c15-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="80c15-128">[вышел] Указатель на указатель на идентификатор записи нового получателя.</span><span class="sxs-lookup"><span data-stu-id="80c15-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80c15-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80c15-129">Return value</span></span>

<span data-ttu-id="80c15-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="80c15-130">S_OK</span></span> 
  
> <span data-ttu-id="80c15-131">Новая запись адресной книги была успешно создана.</span><span class="sxs-lookup"><span data-stu-id="80c15-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80c15-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="80c15-132">Remarks</span></span>

<span data-ttu-id="80c15-133">Метод **NewEntry** создает новую запись адресной книги, которая должна быть добавлена непосредственно в контейнер или использоваться для решения исходяющих сообщений.</span><span class="sxs-lookup"><span data-stu-id="80c15-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="80c15-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="80c15-134">Notes to callers</span></span>

<span data-ttu-id="80c15-135">Если вы хотите, чтобы новая запись была добавлена в определенный контейнер, установите  _lpEIDContainer_ в идентификатор входа контейнера и  _cbEIDContainer_ к счету byte в идентификаторе записи.</span><span class="sxs-lookup"><span data-stu-id="80c15-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="80c15-136">Если вы хотите, чтобы новая запись была добавлена в список получателей исходячего сообщения, установите  _значение lpEIDContainer_ nULL и  _cbEIDContainer_ до нуля.</span><span class="sxs-lookup"><span data-stu-id="80c15-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="80c15-137">Если вы хотите разрешить пользователю клиентского приложения выбрать тип создаваемой записи, сдайте ноль в  _cbEIDNewEntryTpl_ и NULL в  _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="80c15-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="80c15-138">Метод **NewEntry** отображает разовую таблицу MAPI, список шаблонов, поддерживаемых MAPI и каждым поставщиком адресных книг в сеансе.</span><span class="sxs-lookup"><span data-stu-id="80c15-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="80c15-139">Каждый шаблон может создать запись получателя для одного или более типов адресов.</span><span class="sxs-lookup"><span data-stu-id="80c15-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="80c15-140">Если вы хотите сохранить идентификатор входа новой записи, передай допустимые указатели в параметрах _lpcbEIDNewEntry_ и _lppEIDNewEntry._</span><span class="sxs-lookup"><span data-stu-id="80c15-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="80c15-141">Вы несете ответственность за то, чтобы освободить этот идентификатор записи после его завершения, позвонив в [функцию MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="80c15-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="80c15-142">Чтобы использовать определенный шаблон для добавления новой записи в модификабельный контейнер, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="80c15-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="80c15-143">Вызов [метода IMAPISession::OpenEntry](imapisession-openentry.md) для открытия контейнера назначения и установите параметр  _lpEntryID_ в идентификатор входа контейнера.</span><span class="sxs-lookup"><span data-stu-id="80c15-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="80c15-144">Вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера назначения **и** установите параметр _ulPropTag_ PR_CREATE_TEMPLATES [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)и параметр _lpiid_ для IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="80c15-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="80c15-145">Контейнер возвращает разовую таблицу, в которую перечислены все шаблоны, которые он поддерживает для создания новых записей.</span><span class="sxs-lookup"><span data-stu-id="80c15-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="80c15-146">Извлечение строки, которая представляет шаблон для определенного типа записи, которую вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="80c15-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="80c15-147">Столбец **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)указывает тип адреса, поддерживаемый шаблоном.</span><span class="sxs-lookup"><span data-stu-id="80c15-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="80c15-148">Вызов метода **NewEntry** и установите  _lpEIDNewEntryTpl_ в идентификатор входа выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="80c15-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="80c15-149">Идентификатором записи будет **столбец PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)из строки шаблона в разовой таблице.</span><span class="sxs-lookup"><span data-stu-id="80c15-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="80c15-150">Pass zero в  _cbEIDContainer_ и NULL в  _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="80c15-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="80c15-151">Передай допустимый указатель в  _параметре lppEIDNewEntry,_ если вы хотите сохранить идентификатор записи новой записи.</span><span class="sxs-lookup"><span data-stu-id="80c15-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="80c15-152">См. также</span><span class="sxs-lookup"><span data-stu-id="80c15-152">See also</span></span>



[<span data-ttu-id="80c15-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="80c15-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="80c15-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="80c15-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="80c15-155">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="80c15-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="80c15-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="80c15-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

