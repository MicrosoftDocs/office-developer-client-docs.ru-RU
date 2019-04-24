---
title: Иабконтаинеркреатинтри
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287030"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="76b5d-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="76b5d-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="76b5d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76b5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76b5d-105">Создает новую запись, которая может быть пользователем обмена сообщениями, списком рассылки или другим контейнером.</span><span class="sxs-lookup"><span data-stu-id="76b5d-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="76b5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76b5d-106">Parameters</span></span>

 <span data-ttu-id="76b5d-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="76b5d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="76b5d-108">возврата Количество байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="76b5d-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="76b5d-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="76b5d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="76b5d-110">возврата Указатель на идентификатор записи шаблона для создания новых записей определенного типа.</span><span class="sxs-lookup"><span data-stu-id="76b5d-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="76b5d-111">_Улкреатефлагс_</span><span class="sxs-lookup"><span data-stu-id="76b5d-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="76b5d-112">возврата Битовая маска флагов, определяющих порядок выполнения создания записи.</span><span class="sxs-lookup"><span data-stu-id="76b5d-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="76b5d-113">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="76b5d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="76b5d-114">КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ</span><span class="sxs-lookup"><span data-stu-id="76b5d-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="76b5d-115">Необходимо выполнить свободный уровень проверки повторяющихся записей.</span><span class="sxs-lookup"><span data-stu-id="76b5d-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="76b5d-116">Реализация свободной проверки повторяющихся записей определяется поставщиком.</span><span class="sxs-lookup"><span data-stu-id="76b5d-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="76b5d-117">Например, поставщик может определить нестрогое совпадение как любые две записи с одинаковым отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="76b5d-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="76b5d-118">КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ</span><span class="sxs-lookup"><span data-stu-id="76b5d-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="76b5d-119">Необходимо выполнить определенный уровень проверки дубликатов записей.</span><span class="sxs-lookup"><span data-stu-id="76b5d-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="76b5d-120">Реализация проверки на уникальность повторяющихся записей определяется поставщиком.</span><span class="sxs-lookup"><span data-stu-id="76b5d-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="76b5d-121">Например, поставщик может определить в качестве значения для всех двух элементов с одинаковым отображаемым именем и адресом для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="76b5d-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="76b5d-122">КРЕАТЕ_РЕПЛАЦЕ</span><span class="sxs-lookup"><span data-stu-id="76b5d-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="76b5d-123">Новая запись должна заменить существующую, если она определена как дубликаты.</span><span class="sxs-lookup"><span data-stu-id="76b5d-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="76b5d-124">_Лппмапипропентри_</span><span class="sxs-lookup"><span data-stu-id="76b5d-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="76b5d-125">вышли Указатель на указатель на вновь созданный элемент.</span><span class="sxs-lookup"><span data-stu-id="76b5d-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="76b5d-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76b5d-126">Return value</span></span>

<span data-ttu-id="76b5d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="76b5d-127">S_OK</span></span> 
  
> <span data-ttu-id="76b5d-128">Новая запись успешно создана.</span><span class="sxs-lookup"><span data-stu-id="76b5d-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76b5d-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="76b5d-129">Remarks</span></span>

<span data-ttu-id="76b5d-130">Метод **иабконтаинер:: креатинтри** создает новую запись определенного типа в указанном контейнере, возвращая указатель на реализацию интерфейса для последующего доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="76b5d-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="76b5d-131">Новая запись создается с помощью шаблона, выбранного из списка доступных шаблонов контейнера, опубликованных в обратной таблице.</span><span class="sxs-lookup"><span data-stu-id="76b5d-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="76b5d-132">Вызывающие абоненты обращаются к одноразовой таблице контейнера, вызывая метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и запрашивая свойство **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="76b5d-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="76b5d-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="76b5d-133">Notes to implementers</span></span>

<span data-ttu-id="76b5d-134">Все контейнеры, поддерживающие метод **иабконтаинер:: креатинтри** , должны быть изменяемыми.</span><span class="sxs-lookup"><span data-stu-id="76b5d-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="76b5d-135">Установите флаг АБ_МОДИФИАБЛЕ контейнера в его свойстве \*\*пр_контаинер_флагс\*\* ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), чтобы указать, что он является изменяемым.</span><span class="sxs-lookup"><span data-stu-id="76b5d-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="76b5d-136">Вы должны поддерживать все флаги _улкреатефлагс_ .</span><span class="sxs-lookup"><span data-stu-id="76b5d-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="76b5d-137">Однако интерпретация и использование этих флагов зависит от реализации, то есть можно определить семантику КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ и КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ в контексте реализации.</span><span class="sxs-lookup"><span data-stu-id="76b5d-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="76b5d-138">Если не удается определить, является ли запись повторяющейся, всегда разрешите создание записи.</span><span class="sxs-lookup"><span data-stu-id="76b5d-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="76b5d-139">Некоторые поставщики реализуют четкие проверки ввода, сопоставляя отображаемое имя, адрес для обмена сообщениями и ключ поиска в записи; другие поставщики ограничивают подходящими для отображаемого имени и адреса.</span><span class="sxs-lookup"><span data-stu-id="76b5d-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="76b5d-140">НеСтрогая проверка ввода часто реализуется только путем проверки отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="76b5d-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="76b5d-141">Примечания для размещения средств реализации поставщика адресных книг</span><span class="sxs-lookup"><span data-stu-id="76b5d-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="76b5d-142">Если ваш контейнер может создавать записи из шаблонов других поставщиков, ваша реализация **креатинтри** должна предоставлять хранилище для некоторых или всех свойств, связанных с созданными записями.</span><span class="sxs-lookup"><span data-stu-id="76b5d-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="76b5d-143">Например, если вы предоставляете хранилище для свойства **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)), вы можете создать его диалоговое окно со сведениями, не зависят от внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="76b5d-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="76b5d-144">Если ваш контейнер может создавать записи, поддерживающие свойство **пр_темплатеид** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), реализация **креатинтри** должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="76b5d-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="76b5d-145">ВыЗовите метод [имаписуппорт:: опентемплатеид](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="76b5d-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="76b5d-146">**Опентемплатеид** включает код внешнего поставщика для записи, которая будет привязана к создаваемой новой записи.</span><span class="sxs-lookup"><span data-stu-id="76b5d-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="76b5d-147">Внешние поставщики поддерживают этот процесс привязки для поддержания контроля над записями, созданными из их шаблонов, в контейнерах поставщиков адресных книг узла.</span><span class="sxs-lookup"><span data-stu-id="76b5d-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="76b5d-148">Выполните все необходимые действия по инициализации и заполните новый объект всеми свойствами из записи в внешнем поставщике, который возвращает объект в параметре _лппмапипропнев_ из **опентемплатеид**.</span><span class="sxs-lookup"><span data-stu-id="76b5d-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="76b5d-149">Если **опентемплатеид** успешно, скопируйте свойства в реализацию, на которую указывает параметр _лппмапипропнев_ , а не непосредственно к реализации, на которую указывает параметр _лпмапипропдата_ .</span><span class="sxs-lookup"><span data-stu-id="76b5d-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="76b5d-150">Инициализируйте новую запись для использования в автономном режиме, как и любой другой ввод из внешнего поставщика.</span><span class="sxs-lookup"><span data-stu-id="76b5d-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="76b5d-151">Если **опентемплатеид** возвращает ошибку, **креатинтри** не должно вызывать ошибку.</span><span class="sxs-lookup"><span data-stu-id="76b5d-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="76b5d-152">Не разрешать создание записи.</span><span class="sxs-lookup"><span data-stu-id="76b5d-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="76b5d-153">Так как внешний поставщик может делать предположения относительно данных в вашем поставщике, не создавайте запись с идентификатором шаблона, который не был успешно привязан к внешнему поставщику.</span><span class="sxs-lookup"><span data-stu-id="76b5d-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="76b5d-154">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="76b5d-154">Notes to callers</span></span>

<span data-ttu-id="76b5d-155">Когда возвращается значение **креатинтри** , вы можете или не сможете немедленно получить доступ к идентификатору записи для новой записи.</span><span class="sxs-lookup"><span data-stu-id="76b5d-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="76b5d-156">Некоторые поставщики адресных книг не делают ее доступными до тех пор, пока не будет вызван метод New записи [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="76b5d-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="76b5d-157">Несмотря на то что в качестве параметров в **креатинтри**передаются флаги проверки дубликатов, операция проверки на совпадение не выполняется, пока не будет вызван метод **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="76b5d-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="76b5d-158">Таким образом, связанные ошибки, такие как МАПИ_Е_КОЛЛИСИОН, которые указывают, что была предпринята попытка создать уже существующую запись, она возвращается методом **SaveChanges** , а не **креатинтри**.</span><span class="sxs-lookup"><span data-stu-id="76b5d-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="76b5d-159">См. также</span><span class="sxs-lookup"><span data-stu-id="76b5d-159">See also</span></span>



[<span data-ttu-id="76b5d-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="76b5d-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="76b5d-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="76b5d-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="76b5d-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="76b5d-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="76b5d-163">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="76b5d-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="76b5d-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="76b5d-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

