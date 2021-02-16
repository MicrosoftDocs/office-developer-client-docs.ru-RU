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
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411276"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="c911e-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="c911e-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="c911e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c911e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c911e-105">Создает новую запись, которая может быть пользователем системы обмена сообщениями, списком рассылки или другим контейнером.</span><span class="sxs-lookup"><span data-stu-id="c911e-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="c911e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c911e-106">Parameters</span></span>

 <span data-ttu-id="c911e-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c911e-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c911e-108">[in] Количество вхождений в идентификаторе записи, на которые указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="c911e-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c911e-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="c911e-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c911e-110">[in] Указатель на идентификатор записи шаблона для создания новых записей определенного типа.</span><span class="sxs-lookup"><span data-stu-id="c911e-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="c911e-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="c911e-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="c911e-112">[in] Битоваяmas флагов, которая управляет процессом создания записей.</span><span class="sxs-lookup"><span data-stu-id="c911e-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="c911e-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c911e-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c911e-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="c911e-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="c911e-115">Должен выполняться свободный уровень проверки дублирующихся записей.</span><span class="sxs-lookup"><span data-stu-id="c911e-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c911e-116">Реализация свободной проверки записей является конкретной для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c911e-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c911e-117">Например, поставщик может определить свободное совпадение как любые две записи с одинаковым отображаемой именем.</span><span class="sxs-lookup"><span data-stu-id="c911e-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="c911e-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="c911e-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="c911e-119">Должен выполняться строгий уровень проверки записей.</span><span class="sxs-lookup"><span data-stu-id="c911e-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c911e-120">Реализация строгой проверки дубликатов записей является конкретной для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c911e-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c911e-121">Например, поставщик может определить строгое соответствие как любые две записи с одинаковым отображаемого имени и адресом обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c911e-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="c911e-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="c911e-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="c911e-123">Новая запись должна заменить существующую, если определено, что эти две записи дублируются.</span><span class="sxs-lookup"><span data-stu-id="c911e-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="c911e-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="c911e-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="c911e-125">[out] Указатель на указатель на созданную запись.</span><span class="sxs-lookup"><span data-stu-id="c911e-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c911e-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c911e-126">Return value</span></span>

<span data-ttu-id="c911e-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c911e-127">S_OK</span></span> 
  
> <span data-ttu-id="c911e-128">Новая запись успешно создана.</span><span class="sxs-lookup"><span data-stu-id="c911e-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c911e-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="c911e-129">Remarks</span></span>

<span data-ttu-id="c911e-130">Метод **IABContainer::CreateEntry** создает новую запись определенного типа в указанном контейнере, возвращая указатель на реализацию интерфейса для дальнейшего доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="c911e-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="c911e-131">Новая запись создается с помощью шаблона, выбранного в списке доступных шаблонов контейнера, опубликованных в его одностолковой таблице.</span><span class="sxs-lookup"><span data-stu-id="c911e-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="c911e-132">Звоняющие имеют доступ к одноразовой таблице контейнера, вызывая его метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и запрашивая свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c911e-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c911e-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c911e-133">Notes to implementers</span></span>

<span data-ttu-id="c911e-134">Все контейнеры, которые поддерживают метод **IABContainer::CreateEntry,** должны быть модификуемыми.</span><span class="sxs-lookup"><span data-stu-id="c911e-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="c911e-135">Задайте флаг AB_MODIFIABLE контейнера в свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)чтобы указать, что его можно модификатировать.</span><span class="sxs-lookup"><span data-stu-id="c911e-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="c911e-136">Необходимо поддерживать все флаги _ulCreateFlags._</span><span class="sxs-lookup"><span data-stu-id="c911e-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="c911e-137">Однако интерпретация и использование этих флагов является конкретной реализацией, то есть вы можете определить, что семантика CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT означает в контексте реализации.</span><span class="sxs-lookup"><span data-stu-id="c911e-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="c911e-138">Если вы не можете определить, является ли запись дубликатом, всегда разрешайте ее создавать.</span><span class="sxs-lookup"><span data-stu-id="c911e-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="c911e-139">Некоторые поставщики реализуют строгую проверку записи путем совпадения отображаемой записи, адреса обмена сообщениями и ключа поиска в записи; другие поставщики ограничивают совпадение отображаемой именем и адресом.</span><span class="sxs-lookup"><span data-stu-id="c911e-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="c911e-140">Свободные проверки записей часто реализуются путем проверки только отображаемой записи.</span><span class="sxs-lookup"><span data-stu-id="c911e-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="c911e-141">Примечания для поставщиков адресной книги для хост-адресов</span><span class="sxs-lookup"><span data-stu-id="c911e-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="c911e-142">Если контейнер может создавать записи из шаблонов других поставщиков, реализация **CreateEntry** должна предоставить хранилище для некоторых или всех свойств, связанных с созданными записями.</span><span class="sxs-lookup"><span data-stu-id="c911e-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="c911e-143">Например, если вы предоставляете хранилище для свойства **PR_DETAILS_TABLE** записи [(PidTagDetailsTable),](pidtagdetailstable-canonical-property.md)вы можете создать его диалоговое окно сведений без необходимости зависеть от внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="c911e-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="c911e-144">Если контейнер может создавать записи, которые поддерживают **свойство PR_TEMPLATEID** ([PidTagTemplateid),](pidtagtemplateid-canonical-property.md)реализация **CreateEntry** должна сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="c911e-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="c911e-145">Вызовите [метод IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md)</span><span class="sxs-lookup"><span data-stu-id="c911e-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="c911e-146">**OpenTemplateID** позволяет коду внешнего поставщика для записи привязываться к создаемой записи.</span><span class="sxs-lookup"><span data-stu-id="c911e-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="c911e-147">Внешние поставщики поддерживают этот процесс привязки, чтобы контролировать записи, созданные из их шаблонов, в контейнеры поставщиков адресных книг хост-адресов.</span><span class="sxs-lookup"><span data-stu-id="c911e-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="c911e-148">Выполните любую необходимую инициализацию и заполните новый объект всеми свойствами из записи во внешнем поставщике, которую объект вернул в _параметре lppMAPIPropNew_ из **OpenTemplateID.**</span><span class="sxs-lookup"><span data-stu-id="c911e-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="c911e-149">Если **openTemplateID** успешно, скопируйте свойства в реализацию, на которая указывает параметр _lppMAPIPropNew,_ а не непосредственно на реализацию, на которая указывает параметр _lpMAPIPropData._</span><span class="sxs-lookup"><span data-stu-id="c911e-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="c911e-150">Инициализировать новую запись для автономного использования так же, как и любую другую запись от внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="c911e-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="c911e-151">Если **OpenTemplateID** возвращает ошибку, **сбой CreateEntry.**</span><span class="sxs-lookup"><span data-stu-id="c911e-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="c911e-152">Не разрешайте создавать запись.</span><span class="sxs-lookup"><span data-stu-id="c911e-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="c911e-153">Так как внешние поставщики могут делать предположения о данных в поставщике, не создавайте запись с идентификатором шаблона, который не был успешно привязан к внешнему поставщику.</span><span class="sxs-lookup"><span data-stu-id="c911e-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c911e-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c911e-154">Notes to callers</span></span>

<span data-ttu-id="c911e-155">Когда **CreateEntry** возвращает, вы можете или не сможете сразу получить доступ к идентификатору записи для новой записи.</span><span class="sxs-lookup"><span data-stu-id="c911e-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="c911e-156">Некоторые поставщики адресных книг не делают ее доступной до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой записи.</span><span class="sxs-lookup"><span data-stu-id="c911e-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="c911e-157">Хотя в **CreateEntry** в качестве параметров передаются дублирующиеся флажки проверки, повторная проверка не будет происходить до тех пор, пока не будет вызван **saveChanges.**</span><span class="sxs-lookup"><span data-stu-id="c911e-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="c911e-158">Поэтому связанные ошибки, такие как MAPI_E_COLLISION, которые указывают на то, что была предпринята попытка создать уже существующую запись, возвращаются **saveChanges,** а не **CreateEntry.**</span><span class="sxs-lookup"><span data-stu-id="c911e-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c911e-159">См. также</span><span class="sxs-lookup"><span data-stu-id="c911e-159">See also</span></span>



[<span data-ttu-id="c911e-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="c911e-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="c911e-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="c911e-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="c911e-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c911e-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c911e-163">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="c911e-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="c911e-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c911e-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

