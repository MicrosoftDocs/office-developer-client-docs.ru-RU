---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346398"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="e4922-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="e4922-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="e4922-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4922-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4922-105">Копирует одну или несколько записей, как правило, пользователей сообщений или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="e4922-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e4922-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e4922-106">Parameters</span></span>

 <span data-ttu-id="e4922-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="e4922-107">_lpEntries_</span></span>
  
> <span data-ttu-id="e4922-108">[in] Указатель на массив структур [ENTRYLIST,](entrylist.md) содержащий идентификаторы записей для копирования.</span><span class="sxs-lookup"><span data-stu-id="e4922-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="e4922-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e4922-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="e4922-110">[in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="e4922-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="e4922-111">Параметр _ulUIParam_ должен быть нулем, если флаг AB_NO_DIALOG в _параметре ulFlags._</span><span class="sxs-lookup"><span data-stu-id="e4922-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="e4922-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="e4922-112">_lpProgress_</span></span>
  
> <span data-ttu-id="e4922-113">[in] Указатель на объект прогресса, отображает индикатор прогресса или NULL.</span><span class="sxs-lookup"><span data-stu-id="e4922-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="e4922-114">Если _lpProgress_ является NULL, индикатор прогресса должен отображаться с помощью объекта progress, предоставленного MAPI с помощью [метода IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md)</span><span class="sxs-lookup"><span data-stu-id="e4922-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="e4922-115">Параметр  _lpProgress_ игнорируется, если флаг AB_NO_DIALOG установлен в  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e4922-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="e4922-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4922-116">_ulFlags_</span></span>
  
> <span data-ttu-id="e4922-117">[in] Битмаска флагов, которые контролируют, как выполняется операция копирования.</span><span class="sxs-lookup"><span data-stu-id="e4922-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="e4922-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e4922-118">The following flags can be set:</span></span>
    
<span data-ttu-id="e4922-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="e4922-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="e4922-120">Подавляет отображение индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="e4922-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="e4922-121">Если этот флаг не установлен, отображается индикатор прогресса.</span><span class="sxs-lookup"><span data-stu-id="e4922-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="e4922-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="e4922-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="e4922-123">Указывает на то, что должен быть выполнен свободный уровень проверки дублирующихся записей.</span><span class="sxs-lookup"><span data-stu-id="e4922-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="e4922-124">Реализация свободной проверки дубликатов записей — это конкретный поставщик.</span><span class="sxs-lookup"><span data-stu-id="e4922-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="e4922-125">Например, поставщик может определить свободный совпадение как любые две записи с одинаковым именем отображения.</span><span class="sxs-lookup"><span data-stu-id="e4922-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="e4922-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="e4922-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="e4922-127">Указывает на то, что должен быть выполнен строгий уровень проверки записи дублирующихся записей.</span><span class="sxs-lookup"><span data-stu-id="e4922-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="e4922-128">Реализация строгой проверки дубликатов записи является конкретным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e4922-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="e4922-129">Например, поставщик может определить строгое соответствие как любые две записи с одинаковым именем отображения и адресом обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e4922-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="e4922-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="e4922-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="e4922-131">Указывает, что новая запись должна заменить существующую, если установлено, что эти две записи являются дубликатами.</span><span class="sxs-lookup"><span data-stu-id="e4922-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4922-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4922-132">Return value</span></span>

<span data-ttu-id="e4922-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4922-133">S_OK</span></span> 
  
> <span data-ttu-id="e4922-134">Операция копирования прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="e4922-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="e4922-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="e4922-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="e4922-136">Операция копирования в целом прошла успешно, но одну или несколько записей не удалось скопировать.</span><span class="sxs-lookup"><span data-stu-id="e4922-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="e4922-137">Когда это значение возвращается, вызов должен быть обработан как успешный.</span><span class="sxs-lookup"><span data-stu-id="e4922-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="e4922-138">Чтобы проверить это значение, используйте **HR_FAILED** макрос.</span><span class="sxs-lookup"><span data-stu-id="e4922-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="e4922-139">Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="e4922-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4922-140">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4922-140">Remarks</span></span>

<span data-ttu-id="e4922-141">Метод **IABContainer::CopyEntries** копирует записи из одного контейнера или другого контейнера.</span><span class="sxs-lookup"><span data-stu-id="e4922-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="e4922-142">Вызов в **CopyEntries функционально** эквивалентен следующим вызовам для копирования каждой записи:</span><span class="sxs-lookup"><span data-stu-id="e4922-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="e4922-143">Метод [IABContainer::CreateEntry](iabcontainer-createentry.md) для создания новой записи.</span><span class="sxs-lookup"><span data-stu-id="e4922-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="e4922-144">Метод [IMAPIProp::GetProps](imapiprop-getprops.md) для чтения свойств из записи, которая будет скопирована.</span><span class="sxs-lookup"><span data-stu-id="e4922-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="e4922-145">Метод [IMAPIProp::SetProps](imapiprop-setprops.md) для записи свойств в новую запись.</span><span class="sxs-lookup"><span data-stu-id="e4922-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="e4922-146">Метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новой записи для выполнения сохранения.</span><span class="sxs-lookup"><span data-stu-id="e4922-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="e4922-147">Метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) новой записи для выпуска ссылки контейнера.</span><span class="sxs-lookup"><span data-stu-id="e4922-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e4922-148">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="e4922-148">Notes to implementers</span></span>

<span data-ttu-id="e4922-149">Все контейнеры, поддерживают **метод IABContainer::CopyEntries,** должны быть модификабельными.</span><span class="sxs-lookup"><span data-stu-id="e4922-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="e4922-150">Установите флаг AB_MODIFIABLE контейнера в **свойстве PR_CONTAINER_FLAGS** [(PidTagContainerFlags),](pidtagcontainerflags-canonical-property.md)чтобы указать, что он является модификационным.</span><span class="sxs-lookup"><span data-stu-id="e4922-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="e4922-151">Необходимо поддерживать все флаги; однако интерпретация и использование этих флагов специфична для реализации, то есть можно определить, что означают семантика флагов CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT в контексте реализации.</span><span class="sxs-lookup"><span data-stu-id="e4922-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="e4922-152">Если вы не можете или не можете определить, является ли запись дублирующей, всегда разрешайте ее копирование.</span><span class="sxs-lookup"><span data-stu-id="e4922-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="e4922-153">Если флаг CREATE_REPLACE, всегда копируйте запись независимо от CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT и является ли запись дубликатом.</span><span class="sxs-lookup"><span data-stu-id="e4922-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="e4922-154">Если CREATE_REPLACE не установлена и CREATE_CHECK_DUP_STRICT установлена, проверьте, есть ли дубликаты.</span><span class="sxs-lookup"><span data-stu-id="e4922-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="e4922-155">Если запись определена как дубликат, не копируйте запись.</span><span class="sxs-lookup"><span data-stu-id="e4922-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="e4922-156">Вам не нужно поддерживать CREATE_REPLACE; не поддержка CREATE_REPLACE означает, что вы можете безопасно игнорировать его и всегда выполнять копию.</span><span class="sxs-lookup"><span data-stu-id="e4922-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="e4922-157">Возврат предупреждения MAPI_W_PARTIAL_COMPLETION только в том случае, если недюпликированная запись не может быть скопирована.</span><span class="sxs-lookup"><span data-stu-id="e4922-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e4922-158">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e4922-158">Notes to callers</span></span>

<span data-ttu-id="e4922-159">Используйте флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT, чтобы указать поставщику, как вы хотите, чтобы контейнер выполнял проверку дубликатов записи.</span><span class="sxs-lookup"><span data-stu-id="e4922-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="e4922-160">Если необходимо добавить запись независимо от того, является ли она дубликатом, либо не установите ни один из этих флагов, ни CREATE_REPLACE флага.</span><span class="sxs-lookup"><span data-stu-id="e4922-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="e4922-161">CREATE_REPLACE указывает, что вам не важно, является ли запись дубликатом; вы всегда хотите, чтобы она заменила исходную запись.</span><span class="sxs-lookup"><span data-stu-id="e4922-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4922-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e4922-162">See also</span></span>



[<span data-ttu-id="e4922-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="e4922-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="e4922-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="e4922-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="e4922-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e4922-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="e4922-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="e4922-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="e4922-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="e4922-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

