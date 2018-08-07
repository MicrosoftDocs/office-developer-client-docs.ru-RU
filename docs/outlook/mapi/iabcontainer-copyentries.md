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
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808704"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="dd792-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="dd792-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="dd792-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd792-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd792-105">Копирует один или несколько операций, пользователи обычно обмена мгновенными сообщениями или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="dd792-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dd792-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd792-106">Parameters</span></span>

 <span data-ttu-id="dd792-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="dd792-107">_lpEntries_</span></span>
  
> <span data-ttu-id="dd792-108">[in] Указатель на массив структур [ENTRYLIST](entrylist.md) , который содержит идентификаторы записей записей для копирования.</span><span class="sxs-lookup"><span data-stu-id="dd792-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="dd792-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="dd792-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="dd792-110">[in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.</span><span class="sxs-lookup"><span data-stu-id="dd792-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="dd792-111">Параметр _ulUIParam_ должно быть равно нулю, если флаг AB_NO_DIALOG установлен в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dd792-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="dd792-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="dd792-112">_lpProgress_</span></span>
  
> <span data-ttu-id="dd792-113">[in] Указатель на объект хода выполнения, который отображает индикатор выполнения или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dd792-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="dd792-114">Если _lpProgress_ имеет значение NULL, с помощью объекта ход выполнения, предоставляемые MAPI через метод [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) должно отображаться индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dd792-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="dd792-115">Параметр _lpProgress_ игнорируется, если флаг AB_NO_DIALOG установлен в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="dd792-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="dd792-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd792-116">_ulFlags_</span></span>
  
> <span data-ttu-id="dd792-117">[in] Битовая маска флаги, который определяет, как выполняется операция копирования.</span><span class="sxs-lookup"><span data-stu-id="dd792-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="dd792-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="dd792-118">The following flags can be set:</span></span>
    
<span data-ttu-id="dd792-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="dd792-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="dd792-120">Запрещает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dd792-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="dd792-121">Если этот флаг не установлен, отображается индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="dd792-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="dd792-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="dd792-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="dd792-123">Указывает, что свободный уровень проверки повторяющихся запись должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="dd792-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="dd792-124">Реализация проверки свободном дубликат зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="dd792-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="dd792-125">Например поставщик можно определить неточное соответствие две записи, с одинаковым отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="dd792-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="dd792-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="dd792-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="dd792-127">Указывает, что strict уровень проверки повторяющихся запись должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="dd792-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="dd792-128">Реализация strict дубликат проверки зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="dd792-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="dd792-129">Например поставщик можно определить строгое соответствие две записи, оба с одинаковым отображать имя и адрес для сообщений.</span><span class="sxs-lookup"><span data-stu-id="dd792-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="dd792-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="dd792-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="dd792-131">Указывает, что новая запись необходимо заменить существующий, если определено, что они дубликатов.</span><span class="sxs-lookup"><span data-stu-id="dd792-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd792-132">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="dd792-132">Return value</span></span>

<span data-ttu-id="dd792-133">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="dd792-133">S_OK</span></span> 
  
> <span data-ttu-id="dd792-134">Операция копирования выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dd792-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="dd792-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="dd792-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="dd792-136">Операции копирования в целом прошло успешно, но не удалось скопировать один или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="dd792-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="dd792-137">При возвращении это значение вызова необходимо обрабатывать об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="dd792-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="dd792-138">Чтобы проверить это значение, используйте макрос **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="dd792-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="dd792-139">Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="dd792-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd792-140">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd792-140">Remarks</span></span>

<span data-ttu-id="dd792-141">Метод **IABContainer::CopyEntries** копирует записи из другой контейнер или же контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd792-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="dd792-142">Вызов **CopyEntries** функционально эквивалентна выполнение следующих вызовов для каждой записи для копирования:</span><span class="sxs-lookup"><span data-stu-id="dd792-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="dd792-143">Метод [IABContainer::CreateEntry](iabcontainer-createentry.md) , чтобы создать новую запись.</span><span class="sxs-lookup"><span data-stu-id="dd792-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="dd792-144">Метод [IMAPIProp::GetProps](imapiprop-getprops.md) для чтения свойства из записи, которую требуется скопировать.</span><span class="sxs-lookup"><span data-stu-id="dd792-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="dd792-145">Метод [IMAPIProp::SetProps](imapiprop-setprops.md) для записи свойств в новую запись.</span><span class="sxs-lookup"><span data-stu-id="dd792-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="dd792-146">Метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) новую запись для выполнения сохранения.</span><span class="sxs-lookup"><span data-stu-id="dd792-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="dd792-147">Метод [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) новую запись для освобождения ссылку контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd792-147">The new entry's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="dd792-148">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="dd792-148">Notes to implementers</span></span>

<span data-ttu-id="dd792-149">Все контейнеры, поддерживающие метод **IABContainer::CopyEntries** значения можно изменить.</span><span class="sxs-lookup"><span data-stu-id="dd792-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="dd792-150">Установите флаг AB_MODIFIABLE контейнера в своем свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), чтобы указать, что он или нет.</span><span class="sxs-lookup"><span data-stu-id="dd792-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="dd792-151">Должна поддерживать все флажки; Тем не менее, интерпретации и использовании этих флагов зависит от реализации, то есть, вы можете определить означает в контексте внедрения семантика флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT.</span><span class="sxs-lookup"><span data-stu-id="dd792-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="dd792-152">Если не удается или не определить, является ли запись дубликата всегда разрешать записи, которую требуется скопировать.</span><span class="sxs-lookup"><span data-stu-id="dd792-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="dd792-153">Если флаг CREATE_REPLACE имеет значение, всегда копировать записи вне зависимости от ли CREATE_CHECK_DUP_LOOSE или CREATE_CHECK_DUP_STRICT устанавливается и ли операция совпадает со значением.</span><span class="sxs-lookup"><span data-stu-id="dd792-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="dd792-154">Если CREATE_CHECK_DUP_STRICT имеет значение CREATE_REPLACE не установлена, проверьте наличие дубликатов.</span><span class="sxs-lookup"><span data-stu-id="dd792-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="dd792-155">Если запись определяется дубликатом, не копируйте записи.</span><span class="sxs-lookup"><span data-stu-id="dd792-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="dd792-156">Необходимо поддерживать CREATE_REPLACE; не поддерживает CREATE_REPLACE означает, что можно проигнорировать и всегда выполнить копирование.</span><span class="sxs-lookup"><span data-stu-id="dd792-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="dd792-157">Возвращает предупреждение MAPI_W_PARTIAL_COMPLETION только в том случае, если не удается скопировать неповторяющихся запись.</span><span class="sxs-lookup"><span data-stu-id="dd792-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dd792-158">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dd792-158">Notes to callers</span></span>

<span data-ttu-id="dd792-159">Используйте флаги CREATE_CHECK_DUP_LOOSE и CREATE_CHECK_DUP_STRICT для указания к поставщику того, как контейнер для выполнения проверки повторяющихся запись.</span><span class="sxs-lookup"><span data-stu-id="dd792-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="dd792-160">Если вам потребуется добавлена независимо от того, будет ли это дублировать записи, не задавайте для этих флагов или установить флаг CREATE_REPLACE.</span><span class="sxs-lookup"><span data-stu-id="dd792-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="dd792-161">CREATE_REPLACE указывает, что не нужно, если запись уже существует; всегда необходимо заменить исходной записи.</span><span class="sxs-lookup"><span data-stu-id="dd792-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd792-162">См. также</span><span class="sxs-lookup"><span data-stu-id="dd792-162">See also</span></span>



[<span data-ttu-id="dd792-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="dd792-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="dd792-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="dd792-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="dd792-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd792-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="dd792-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="dd792-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="dd792-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dd792-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

