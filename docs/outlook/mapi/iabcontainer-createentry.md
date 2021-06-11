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
# <a name="iabcontainercreateentry"></a><span data-ttu-id="d7efe-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="d7efe-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="d7efe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7efe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7efe-105">Создает новую запись, которая может быть пользователем обмена сообщениями, списком рассылки или другим контейнером.</span><span class="sxs-lookup"><span data-stu-id="d7efe-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="d7efe-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d7efe-106">Parameters</span></span>

 <span data-ttu-id="d7efe-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="d7efe-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="d7efe-108">[in] Количество bytes в идентификаторе записи, на который указывает параметр _lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="d7efe-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="d7efe-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="d7efe-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="d7efe-110">[in] Указатель на идентификатор записи шаблона для создания новых записей определенного типа.</span><span class="sxs-lookup"><span data-stu-id="d7efe-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="d7efe-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="d7efe-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="d7efe-112">[in] Битмашка флагов, которые контролируют выполнение создания записи.</span><span class="sxs-lookup"><span data-stu-id="d7efe-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="d7efe-113">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d7efe-113">The following flags can be set:</span></span>
    
<span data-ttu-id="d7efe-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="d7efe-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="d7efe-115">Должен быть выполнен свободный уровень проверки дублирующихся записей.</span><span class="sxs-lookup"><span data-stu-id="d7efe-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="d7efe-116">Реализация свободной проверки дубликатов записей — это конкретный поставщик.</span><span class="sxs-lookup"><span data-stu-id="d7efe-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="d7efe-117">Например, поставщик может определить свободный совпадение как любые две записи с одинаковым именем отображения.</span><span class="sxs-lookup"><span data-stu-id="d7efe-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="d7efe-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="d7efe-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="d7efe-119">Должен быть выполнен строгий уровень проверки записи дубликата.</span><span class="sxs-lookup"><span data-stu-id="d7efe-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="d7efe-120">Реализация строгой проверки дубликатов записи является конкретным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d7efe-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="d7efe-121">Например, поставщик может определить строгое соответствие как любые две записи с одинаковым именем отображения и адресом обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d7efe-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="d7efe-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="d7efe-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="d7efe-123">Новая запись должна заменить существующую, если установлено, что эти две записи являются дубликатами.</span><span class="sxs-lookup"><span data-stu-id="d7efe-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="d7efe-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="d7efe-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="d7efe-125">[вышел] Указатель на указатель на вновь созданную запись.</span><span class="sxs-lookup"><span data-stu-id="d7efe-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d7efe-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7efe-126">Return value</span></span>

<span data-ttu-id="d7efe-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7efe-127">S_OK</span></span> 
  
> <span data-ttu-id="d7efe-128">Новая запись была успешно создана.</span><span class="sxs-lookup"><span data-stu-id="d7efe-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d7efe-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7efe-129">Remarks</span></span>

<span data-ttu-id="d7efe-130">Метод **IABContainer::CreateEntry** создает новую запись определенного типа в указанном контейнере, возвращая указатель в реализацию интерфейса для дальнейшего доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="d7efe-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="d7efe-131">Новая запись создается с помощью шаблона, выбранного из списка доступных шаблонов контейнера, опубликованных в его разовой таблице.</span><span class="sxs-lookup"><span data-stu-id="d7efe-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="d7efe-132">Звонители могут получить доступ к разовой таблице контейнера, позвонив по методу [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **и** запросив свойство [PR_CREATE_TEMPLATES (PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="d7efe-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d7efe-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d7efe-133">Notes to implementers</span></span>

<span data-ttu-id="d7efe-134">Все контейнеры, поддерживают **метод IABContainer::CreateEntry,** должны быть модификабельными.</span><span class="sxs-lookup"><span data-stu-id="d7efe-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="d7efe-135">Установите флаг AB_MODIFIABLE контейнера в **свойстве PR_CONTAINER_FLAGS** [(PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)чтобы указать, что он является модификационным.</span><span class="sxs-lookup"><span data-stu-id="d7efe-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="d7efe-136">Необходимо поддерживать все флаги _ulCreateFlags._</span><span class="sxs-lookup"><span data-stu-id="d7efe-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="d7efe-137">Однако интерпретация и использование этих флагов специфична для реализации, то есть можно определить, что означают семантика CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT в контексте реализации.</span><span class="sxs-lookup"><span data-stu-id="d7efe-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="d7efe-138">Если вы не можете или не можете определить, является ли запись дубликатом, всегда разрешайте создать запись.</span><span class="sxs-lookup"><span data-stu-id="d7efe-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="d7efe-139">Некоторые поставщики реализуют строгие проверки входа, сообразуя имя отображения, адрес обмена сообщениями и ключ поиска в записи; другие поставщики ограничивают совпадение отображением имени и адреса.</span><span class="sxs-lookup"><span data-stu-id="d7efe-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="d7efe-140">Проверка свободного входа часто реализуется, проверяя только имя дисплея.</span><span class="sxs-lookup"><span data-stu-id="d7efe-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="d7efe-141">Заметки для организаторов поставщиков адресных книг</span><span class="sxs-lookup"><span data-stu-id="d7efe-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="d7efe-142">Если контейнер может создавать записи из шаблонов других поставщиков, реализация **CreateEntry** должна обеспечить хранение некоторых или всех свойств, связанных с созданными записями.</span><span class="sxs-lookup"><span data-stu-id="d7efe-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="d7efe-143">Например, если вы предоставляете **хранилище** для свойства PR_DETAILS_TABLE входа [(PidTagDetailsTable),](pidtagdetailstable-canonical-property.md)вы можете создать диалоговое окно его сведений без необходимости зависеть от иностранного поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7efe-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="d7efe-144">Если контейнер может создавать **записи, поддерживаюные свойство PR_TEMPLATEID** [(PidTagTemplateid),](pidtagtemplateid-canonical-property.md)реализация **CreateEntry** должна сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="d7efe-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="d7efe-145">Вызов метода [IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md)</span><span class="sxs-lookup"><span data-stu-id="d7efe-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="d7efe-146">**OpenTemplateID** позволяет коду иностранного поставщика для входа привязаться к создаемой новой записи.</span><span class="sxs-lookup"><span data-stu-id="d7efe-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="d7efe-147">Иностранные поставщики поддерживают этот процесс привязки для поддержания контроля над записями, созданными из их шаблонов, в контейнеры поставщиков адресных книг хост-адресов.</span><span class="sxs-lookup"><span data-stu-id="d7efe-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="d7efe-148">Выполните любую необходимую инициализацию и заполнять новый объект всеми свойствами из записи в иностранном поставщике, возвращаемом объектом в _параметре lppMAPIPropNew_ из **OpenTemplateID.**</span><span class="sxs-lookup"><span data-stu-id="d7efe-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="d7efe-149">Если **openTemplateID** успешно, скопируйте свойства для реализации, на которые указывает параметр _lppMAPIPropNew,_ а не непосредственно к реализации, на который указывает параметр _lpMAPIPropData._</span><span class="sxs-lookup"><span data-stu-id="d7efe-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="d7efe-150">Инициализация новой записи для автономного использования, как и любая другая запись от иностранного поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7efe-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="d7efe-151">Если **OpenTemplateID** возвращает ошибку, **CreateEntry** должен не сбой.</span><span class="sxs-lookup"><span data-stu-id="d7efe-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="d7efe-152">Не допускайте создания записи.</span><span class="sxs-lookup"><span data-stu-id="d7efe-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="d7efe-153">Так как иностранный поставщик может делать предположения о данных в поставщике, не создайте запись с идентификатором шаблона, который не был успешно привязан к иностранному поставщику.</span><span class="sxs-lookup"><span data-stu-id="d7efe-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d7efe-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d7efe-154">Notes to callers</span></span>

<span data-ttu-id="d7efe-155">Когда **CreateEntry** возвращается, вы можете или не сможете сразу получить доступ к идентификатору записи для новой записи.</span><span class="sxs-lookup"><span data-stu-id="d7efe-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="d7efe-156">Некоторые поставщики адресных книг не делают ее доступной до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="d7efe-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="d7efe-157">Несмотря на то, что дублирующие флаги проверки передаются в качестве параметров **в CreateEntry,** операция проверки дубликатов не будет происходить до тех пор, пока не будет **вызвано saveChanges.**</span><span class="sxs-lookup"><span data-stu-id="d7efe-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="d7efe-158">Поэтому связанные ошибки, такие как MAPI_E_COLLISION, которые указывают на то, что была предпринята попытка создать уже существующую запись, возвращаются **saveChanges,** а не **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="d7efe-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7efe-159">См. также</span><span class="sxs-lookup"><span data-stu-id="d7efe-159">See also</span></span>



[<span data-ttu-id="d7efe-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="d7efe-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="d7efe-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="d7efe-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="d7efe-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d7efe-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="d7efe-163">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="d7efe-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="d7efe-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="d7efe-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

