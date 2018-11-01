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
ms.openlocfilehash: eaf472a380acd62cddb2c20c35335ccb1e2ce07f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585859"
---
# <a name="iaddrbooknewentry"></a><span data-ttu-id="78fae-103">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="78fae-103">IAddrBook::NewEntry</span></span>

  
  
<span data-ttu-id="78fae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78fae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78fae-105">Добавляет нового получателя контейнер адресной книги или списка получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="78fae-105">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="78fae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78fae-106">Parameters</span></span>

 <span data-ttu-id="78fae-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="78fae-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="78fae-108">[in] Дескриптор родительского окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="78fae-108">[in] A handle to the parent window for the dialog box.</span></span>
    
 <span data-ttu-id="78fae-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78fae-109">_ulFlags_</span></span>
  
> <span data-ttu-id="78fae-110">[in] Битовая маска флаги, определяющее тип текст, который используется.</span><span class="sxs-lookup"><span data-stu-id="78fae-110">[in] A bitmask of flags that controls the type of the text that is used.</span></span> <span data-ttu-id="78fae-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="78fae-111">The following flag can be set:</span></span>
    
<span data-ttu-id="78fae-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78fae-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="78fae-113">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="78fae-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="78fae-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="78fae-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="78fae-115">_cbEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="78fae-115">_cbEIDContainer_</span></span>
  
> <span data-ttu-id="78fae-116">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="78fae-116">[in] The byte count in the entry identifier pointed to by the  _lpEIDContainer_ parameter.</span></span> 
    
 <span data-ttu-id="78fae-117">_lpEIDContainer_</span><span class="sxs-lookup"><span data-stu-id="78fae-117">_lpEIDContainer_</span></span>
  
> <span data-ttu-id="78fae-118">[in] Указатель на идентификатор записи контейнер, в котором для добавления нового получателя.</span><span class="sxs-lookup"><span data-stu-id="78fae-118">[in] A pointer to the entry identifier of the container where the new recipient is to be added.</span></span> <span data-ttu-id="78fae-119">Если параметр _cbEIDContainer_ равно нулю, метод **NewEntry** возвращает идентификатор получателя записи и список шаблонов, как если бы метод [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) вызван.</span><span class="sxs-lookup"><span data-stu-id="78fae-119">If the  _cbEIDContainer_ parameter is zero, the **NewEntry** method returns a recipient entry identifier and a list of templates as if the [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) method was called.</span></span> 
    
 <span data-ttu-id="78fae-120">_cbEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="78fae-120">_cbEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="78fae-121">[in] Число байтов в идентификатор записи, на который указывает параметр _lpEIDNewEntryTpl_ .</span><span class="sxs-lookup"><span data-stu-id="78fae-121">[in] The byte count in the entry identifier pointed to by the  _lpEIDNewEntryTpl_ parameter.</span></span> 
    
 <span data-ttu-id="78fae-122">_lpEIDNewEntryTpl_</span><span class="sxs-lookup"><span data-stu-id="78fae-122">_lpEIDNewEntryTpl_</span></span>
  
> <span data-ttu-id="78fae-123">[in] Указатель на одноразовых шаблон, который будет использоваться для создания нового получателя.</span><span class="sxs-lookup"><span data-stu-id="78fae-123">[in] A pointer to a one-off template that will be used to create the new recipient.</span></span> <span data-ttu-id="78fae-124">Если _cbEIDNewEntryTpl_ равно нулю, а _lpEIDNewEntryTpl_ имеет значение NULL, **NewEntry** отображает диалоговое окно, с помощью которой пользователь может выбрать из списка шаблонов для добавления новых записей.</span><span class="sxs-lookup"><span data-stu-id="78fae-124">If  _cbEIDNewEntryTpl_ is zero and  _lpEIDNewEntryTpl_ is NULL, **NewEntry** displays a dialog box with which the user can select from a list of templates for adding new entries.</span></span> 
    
 <span data-ttu-id="78fae-125">_lpcbEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="78fae-125">_lpcbEIDNewEntry_</span></span>
  
> <span data-ttu-id="78fae-126">[out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="78fae-126">[out] A pointer to the byte count in the entry identifier pointed to by the  _lppEIDNewEntry_ parameter.</span></span> 
    
 <span data-ttu-id="78fae-127">_lppEIDNewEntry_</span><span class="sxs-lookup"><span data-stu-id="78fae-127">_lppEIDNewEntry_</span></span>
  
> <span data-ttu-id="78fae-128">[out] Указатель на указатель на идентификатор записи нового получателя.</span><span class="sxs-lookup"><span data-stu-id="78fae-128">[out] A pointer to a pointer to the new recipient's entry identifier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78fae-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78fae-129">Return value</span></span>

<span data-ttu-id="78fae-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="78fae-130">S_OK</span></span> 
  
> <span data-ttu-id="78fae-131">Новые записи адресной книги был успешно создан.</span><span class="sxs-lookup"><span data-stu-id="78fae-131">The new address book entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78fae-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="78fae-132">Remarks</span></span>

<span data-ttu-id="78fae-133">Метод **NewEntry** создает новую запись книги адреса, добавляемого непосредственно в контейнер или для использования с учетом исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="78fae-133">The **NewEntry** method creates a new address book entry, to be added directly into a container or to be used to address an outgoing message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="78fae-134">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="78fae-134">Notes to callers</span></span>

<span data-ttu-id="78fae-135">Новая запись будет добавлена к конкретному контейнеру, установите _lpEIDContainer_ идентификатор записи и _cbEIDContainer_ на число байтов в идентификатор записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="78fae-135">If you want the new entry to be added to a specific container, set  _lpEIDContainer_ to the container's entry identifier and  _cbEIDContainer_ to the byte count in the entry identifier.</span></span> 
  
<span data-ttu-id="78fae-136">Новая запись будет добавлена в список получателей исходящих сообщений, установите _lpEIDContainer_ NULL и _cbEIDContainer_ присваивается значение 0.</span><span class="sxs-lookup"><span data-stu-id="78fae-136">If you want the new entry to be added to the recipient list of an outgoing message, set  _lpEIDContainer_ to NULL and  _cbEIDContainer_ to zero.</span></span> 
  
<span data-ttu-id="78fae-137">Если вы хотите разрешить пользователю создавать клиентского приложения, чтобы выбрать тип записи, передайте ноль в _cbEIDNewEntryTpl_ и NULL в _lpEIDNewEntryTpl_.</span><span class="sxs-lookup"><span data-stu-id="78fae-137">If you want to allow the user of a client application to select the type of entry to be created, pass zero in  _cbEIDNewEntryTpl_ and NULL in  _lpEIDNewEntryTpl_.</span></span> <span data-ttu-id="78fae-138">Метод **NewEntry** отображаются в таблице одноразовых MAPI, список шаблонов, MAPI и каждый поставщик адресной книги поддерживают в сеансе.</span><span class="sxs-lookup"><span data-stu-id="78fae-138">The **NewEntry** method displays the MAPI one-off table, a list of templates supported by MAPI and by each address book provider in the session.</span></span> <span data-ttu-id="78fae-139">В каждый шаблон можно создать запись получателей для одного или нескольких типов адресов.</span><span class="sxs-lookup"><span data-stu-id="78fae-139">Each template can create a recipient entry for one or more address types.</span></span> 
  
<span data-ttu-id="78fae-140">Если вы хотите сохранить идентификатор записи новой записи, передайте допустимый указатели параметры _lpcbEIDNewEntry_ и _lppEIDNewEntry_ .</span><span class="sxs-lookup"><span data-stu-id="78fae-140">If you want to retain the entry identifier of the new entry, pass valid pointers in the  _lpcbEIDNewEntry_ and  _lppEIDNewEntry_ parameters.</span></span> <span data-ttu-id="78fae-141">Вы несете ответственность за освобождение этот идентификатор записи после завершения с ним с помощью вызова функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="78fae-141">You are responsible for freeing this entry identifier when you are finished with it by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="78fae-142">Чтобы использовать шаблон, определенного для добавления записи к контейнеру можно изменить, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="78fae-142">To use a particular template to add a new entry to a modifiable container, use the following procedure:</span></span>
  
1. <span data-ttu-id="78fae-143">Вызовите метод [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия конечного контейнера и установите для параметра _lpEntryID_ значение идентификатор записи контейнера.</span><span class="sxs-lookup"><span data-stu-id="78fae-143">Call the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open the destination container, and set the  _lpEntryID_ parameter to the entry identifier of the container.</span></span> 
    
2. <span data-ttu-id="78fae-144">Вызовите метод конечный контейнер [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и установите параметр _ulPropTag_ для **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) и параметр _lpiid_ IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="78fae-144">Call the destination container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, and set the  _ulPropTag_ parameter to **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) and the  _lpiid_ parameter to IID_IMAPITable.</span></span> <span data-ttu-id="78fae-145">Контейнер будет возвращать одноразовых таблице перечислены все шаблоны, поддерживаемые для создания новых записей.</span><span class="sxs-lookup"><span data-stu-id="78fae-145">The container will return a one-off table that lists all the templates that it supports for creating new entries.</span></span> 
    
3. <span data-ttu-id="78fae-146">Получите строку, которая представляет шаблон для определенного типа записи, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="78fae-146">Retrieve the row that represents the template for the particular type of entry you want to create.</span></span> <span data-ttu-id="78fae-147">В столбце **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) указывается тип адреса, который поддерживается в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="78fae-147">The **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) column indicates the address type that is supported by the template.</span></span>
    
4. <span data-ttu-id="78fae-148">Вызовите метод **NewEntry** и установите _lpEIDNewEntryTpl_ идентификатор записи выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="78fae-148">Call the **NewEntry** method, and set  _lpEIDNewEntryTpl_ to the entry identifier of the selected template.</span></span> <span data-ttu-id="78fae-149">Идентификатор записи будет столбец **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из шаблона строку в таблице одноразовых.</span><span class="sxs-lookup"><span data-stu-id="78fae-149">The entry identifier will be the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) column from the template's row in the one-off table.</span></span> <span data-ttu-id="78fae-150">Передайте ноль в _cbEIDContainer_ и NULL в _lpEIDContainer_.</span><span class="sxs-lookup"><span data-stu-id="78fae-150">Pass zero in  _cbEIDContainer_ and NULL in  _lpEIDContainer_.</span></span> <span data-ttu-id="78fae-151">Передайте допустимый указатель в параметре _lppEIDNewEntry_ , если вы хотите сохранить идентификатор записи новую запись.</span><span class="sxs-lookup"><span data-stu-id="78fae-151">Pass a valid pointer in the  _lppEIDNewEntry_ parameter if you want to retain the new entry's entry identifier.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="78fae-152">См. также</span><span class="sxs-lookup"><span data-stu-id="78fae-152">See also</span></span>



[<span data-ttu-id="78fae-153">IAddrBook::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="78fae-153">IAddrBook::OpenEntry</span></span>](iaddrbook-openentry.md)
  
[<span data-ttu-id="78fae-154">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="78fae-154">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="78fae-155">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="78fae-155">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="78fae-156">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="78fae-156">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

