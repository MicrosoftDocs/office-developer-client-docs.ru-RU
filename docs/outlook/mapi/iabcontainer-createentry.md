---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2f8a6baa9a910b91e633084f1d9cd8ac52b24d5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575604"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="292cf-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="292cf-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="292cf-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="292cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="292cf-105">Создает новый объект, который может быть обмена сообщениями пользователя, в список рассылки или другой контейнер.</span><span class="sxs-lookup"><span data-stu-id="292cf-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="292cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="292cf-106">Parameters</span></span>

 <span data-ttu-id="292cf-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="292cf-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="292cf-108">[in] Число байт в идентификаторе запись указывает параметр _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="292cf-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="292cf-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="292cf-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="292cf-110">[in] Указатель на идентификатор записи шаблон для создания новых записей определенного типа.</span><span class="sxs-lookup"><span data-stu-id="292cf-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="292cf-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="292cf-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="292cf-112">[in] Битовая маска флаги, который определяет, как выполняется операция создания.</span><span class="sxs-lookup"><span data-stu-id="292cf-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="292cf-113">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="292cf-113">The following flags can be set:</span></span>
    
<span data-ttu-id="292cf-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="292cf-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="292cf-115">Следует выполнять свободном уровень проверки повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="292cf-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="292cf-116">Реализация проверки свободном дубликат зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="292cf-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="292cf-117">Например поставщик можно определить неточное соответствие две записи, с одинаковым отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="292cf-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="292cf-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="292cf-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="292cf-119">Следует выполнять строго уровень проверки повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="292cf-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="292cf-120">Реализация strict дубликат проверки зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="292cf-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="292cf-121">Например поставщик можно определить строгое соответствие две записи, оба с одинаковым отображать имя и адрес для сообщений.</span><span class="sxs-lookup"><span data-stu-id="292cf-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="292cf-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="292cf-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="292cf-123">Новая запись необходимо заменить существующий, если определено, что они дубликатов.</span><span class="sxs-lookup"><span data-stu-id="292cf-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="292cf-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="292cf-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="292cf-125">[out] Указатель на указатель на созданный элемент.</span><span class="sxs-lookup"><span data-stu-id="292cf-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="292cf-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="292cf-126">Return value</span></span>

<span data-ttu-id="292cf-127">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="292cf-127">S_OK</span></span> 
  
> <span data-ttu-id="292cf-128">Новая запись успешно создан.</span><span class="sxs-lookup"><span data-stu-id="292cf-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="292cf-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="292cf-129">Remarks</span></span>

<span data-ttu-id="292cf-130">Метод **IABContainer::CreateEntry** создает новую запись определенного типа в указанном контейнере, указатель возвращается в реализации интерфейса дальнейший доступ к записи.</span><span class="sxs-lookup"><span data-stu-id="292cf-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="292cf-131">Новая запись создается с помощью шаблона, который был выбран из контейнера списка доступных шаблонов, опубликованные в одноразовых таблице.</span><span class="sxs-lookup"><span data-stu-id="292cf-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="292cf-132">Абоненты доступ к таблице одноразовых контейнер путем вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и разрешения на запрос свойства **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="292cf-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="292cf-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="292cf-133">Notes to implementers</span></span>

<span data-ttu-id="292cf-134">Все контейнеры, поддерживающие метод **IABContainer::CreateEntry** значения можно изменить.</span><span class="sxs-lookup"><span data-stu-id="292cf-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="292cf-135">Установите флаг AB_MODIFIABLE контейнера в своем свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), чтобы указать, что он или нет.</span><span class="sxs-lookup"><span data-stu-id="292cf-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="292cf-136">Вы должны поддерживать все флажки _ulCreateFlags_ .</span><span class="sxs-lookup"><span data-stu-id="292cf-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="292cf-137">Тем не менее, интерпретации и использовании этих флагов зависит от реализации, то есть, вы можете определить означает в контексте внедрения семантика CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="292cf-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="292cf-138">Если не удается или не определить, является ли запись дубликата всегда разрешать записи, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="292cf-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="292cf-139">Некоторые поставщики реализации строго запись при проверке соответствия отображаемое имя системы обмена сообщениями адрес и ключа поиска в запись; прочие ограничения совпадение, чтобы отобразить имя и адрес.</span><span class="sxs-lookup"><span data-stu-id="292cf-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="292cf-140">Проверка свободного запись часто реализуется проверка только отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="292cf-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="292cf-141">Примечания для размещения специалистов по внедрению поставщик адресной книги</span><span class="sxs-lookup"><span data-stu-id="292cf-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="292cf-142">Если контейнера можно создавать записи на основе шаблонов других поставщиков, внедрения **CreateEntry** предоставьте хранилища для некоторых или всех свойств, связанных с созданные операции.</span><span class="sxs-lookup"><span data-stu-id="292cf-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="292cf-143">Например при указании хранилища для свойства элемента **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) можно создать его диалоговое окно сведений о без необходимости зависят от внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="292cf-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="292cf-144">Если контейнера можно создавать записи, которые поддерживают свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), внедрения **CreateEntry** необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="292cf-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="292cf-145">Вызовите метод [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="292cf-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="292cf-146">**OpenTemplateID** включает код внешнего поставщика для записи для привязки к создаваемой новую запись.</span><span class="sxs-lookup"><span data-stu-id="292cf-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="292cf-147">Внешний поставщиков поддерживает этот процесс привязки для контроля за операции, созданные из своих шаблонов в контейнеры узла поставщиками адресной книги.</span><span class="sxs-lookup"><span data-stu-id="292cf-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="292cf-148">Выполнить инициализацию и внесите в новый объект со всеми свойствами из записи в внешнего поставщика, возвращенный объект с помощью параметра _lppMAPIPropNew_ из **OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="292cf-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="292cf-149">При успешном **OpenTemplateID** скопируйте свойства в реализации указывает параметр _lppMAPIPropNew_ , а не непосредственно к реализации, на который указывает параметр _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="292cf-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="292cf-150">Инициализация новую запись в автономном режиме, как и любой другой записи от внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="292cf-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="292cf-151">Если **OpenTemplateID** возвращает ошибку, **CreateEntry** следует с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="292cf-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="292cf-152">Не разрешать записи, которую требуется создать.</span><span class="sxs-lookup"><span data-stu-id="292cf-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="292cf-153">Так как внешнего поставщика можно оценить данные в ваш поставщик, не создают запись с идентификатором шаблона, который не был успешно привязан к внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="292cf-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="292cf-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="292cf-154">Notes to callers</span></span>

<span data-ttu-id="292cf-155">При возврате **CreateEntry** , можно или не удается для немедленного доступа к идентификатор записи для новой записи.</span><span class="sxs-lookup"><span data-stu-id="292cf-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="292cf-156">Некоторые поставщиками адресной книги не сделать его доступным только после вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новая запись.</span><span class="sxs-lookup"><span data-stu-id="292cf-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="292cf-157">Несмотря на то, что повторяющихся проверки флаги передаются в качестве параметров для **CreateEntry**, дубликат проверку не выполняется до вызова метода **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="292cf-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="292cf-158">Таким образом связанных с ними ошибки, например MAPI_E_COLLISION, это означает, что была предпринята попытка создание уже существующей записи, возвращаемые **SaveChanges** , а не **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="292cf-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="292cf-159">См. также</span><span class="sxs-lookup"><span data-stu-id="292cf-159">See also</span></span>



[<span data-ttu-id="292cf-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="292cf-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="292cf-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="292cf-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="292cf-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="292cf-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="292cf-163">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="292cf-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="292cf-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="292cf-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

