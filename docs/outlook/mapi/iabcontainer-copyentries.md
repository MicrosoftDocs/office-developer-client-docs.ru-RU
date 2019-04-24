---
title: Иабконтаинеркопентриес
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
# <a name="iabcontainercopyentries"></a><span data-ttu-id="62e62-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="62e62-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="62e62-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62e62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62e62-105">Копирует одну или несколько записей, как правило, пользователи системы обмена сообщениями или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="62e62-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="62e62-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62e62-106">Parameters</span></span>

 <span data-ttu-id="62e62-107">_Лпентриес_</span><span class="sxs-lookup"><span data-stu-id="62e62-107">_lpEntries_</span></span>
  
> <span data-ttu-id="62e62-108">возврата Указатель на массив структур [ентрилист](entrylist.md) , который содержит идентификаторы записей для копирования.</span><span class="sxs-lookup"><span data-stu-id="62e62-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="62e62-109">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="62e62-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="62e62-110">возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.</span><span class="sxs-lookup"><span data-stu-id="62e62-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="62e62-111">Если в параметре _ulFlags_ ЗАДАН флаг аб_но_диалог, параметр _улуипарам_ должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="62e62-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="62e62-112">_Лппрогресс_</span><span class="sxs-lookup"><span data-stu-id="62e62-112">_lpProgress_</span></span>
  
> <span data-ttu-id="62e62-113">возврата Указатель на объект Progress, который отображает индикатор хода выполнения, или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="62e62-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="62e62-114">Если _лппрогресс_ имеет значение null, индикатор хода выполнения должен отображаться с использованием объекта Progress, ПРЕДОСТАВЛЕНного MAPI, с помощью метода [Имаписуппорт::D опрогрессдиалог](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="62e62-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="62e62-115">Параметр _лппрогресс_ игнорируется, если установлен флаг Аб_но_диалог в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="62e62-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="62e62-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62e62-116">_ulFlags_</span></span>
  
> <span data-ttu-id="62e62-117">возврата Битовая маска флагов, определяющих порядок выполнения операции копирования.</span><span class="sxs-lookup"><span data-stu-id="62e62-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="62e62-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="62e62-118">The following flags can be set:</span></span>
    
<span data-ttu-id="62e62-119">АБ_НО_ДИАЛОГ</span><span class="sxs-lookup"><span data-stu-id="62e62-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="62e62-120">Отключает отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="62e62-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="62e62-121">Если этот флаг не установлен, отображается индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="62e62-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="62e62-122">КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ</span><span class="sxs-lookup"><span data-stu-id="62e62-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="62e62-123">Указывает, что следует выполнить нестрогий уровень проверки повторяющихся записей.</span><span class="sxs-lookup"><span data-stu-id="62e62-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="62e62-124">Реализация свободной проверки повторяющихся записей определяется поставщиком.</span><span class="sxs-lookup"><span data-stu-id="62e62-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="62e62-125">Например, поставщик может определить нестрогое совпадение как любые две записи с одинаковым отображаемым именем.</span><span class="sxs-lookup"><span data-stu-id="62e62-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="62e62-126">КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ</span><span class="sxs-lookup"><span data-stu-id="62e62-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="62e62-127">Указывает, что необходимо выполнить определенный уровень проверки дубликатов записей.</span><span class="sxs-lookup"><span data-stu-id="62e62-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="62e62-128">Реализация проверки на уникальность повторяющихся записей определяется поставщиком.</span><span class="sxs-lookup"><span data-stu-id="62e62-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="62e62-129">Например, поставщик может определить в качестве значения для всех двух элементов с одинаковым отображаемым именем и адресом для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="62e62-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="62e62-130">КРЕАТЕ_РЕПЛАЦЕ</span><span class="sxs-lookup"><span data-stu-id="62e62-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="62e62-131">Указывает, что новая запись должна заменить существующую, если она определена как дубликаты.</span><span class="sxs-lookup"><span data-stu-id="62e62-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62e62-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62e62-132">Return value</span></span>

<span data-ttu-id="62e62-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="62e62-133">S_OK</span></span> 
  
> <span data-ttu-id="62e62-134">Операция копирования успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="62e62-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="62e62-135">МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН</span><span class="sxs-lookup"><span data-stu-id="62e62-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="62e62-136">Операция копирования успешно выполнена, но не удалось скопировать одну или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="62e62-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="62e62-137">Когда возвращается это значение, вызов должен обрабатываться как успешный.</span><span class="sxs-lookup"><span data-stu-id="62e62-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="62e62-138">Чтобы проверить это значение, используйте макрос **хр_фаилед** .</span><span class="sxs-lookup"><span data-stu-id="62e62-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="62e62-139">Дополнительные сведения см. [в разделе Использование макросов для обработки ошибок](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="62e62-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="62e62-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62e62-140">Remarks</span></span>

<span data-ttu-id="62e62-141">Метод **иабконтаинер:: копентриес** копирует записи из одного и того же контейнера или другого контейнера.</span><span class="sxs-lookup"><span data-stu-id="62e62-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="62e62-142">Вызов **копентриес** функционально эквивалентен выполнению следующих вызовов для каждой копируемой записи:</span><span class="sxs-lookup"><span data-stu-id="62e62-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="62e62-143">Метод [иабконтаинер:: креатинтри](iabcontainer-createentry.md) для создания новой записи.</span><span class="sxs-lookup"><span data-stu-id="62e62-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="62e62-144">Метод [IMAPIProp::](imapiprop-getprops.md) -PROPS для чтения свойств копируемой записи.</span><span class="sxs-lookup"><span data-stu-id="62e62-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="62e62-145">Метод [IMAPIProp:: SetProps](imapiprop-setprops.md) для записи свойств в новую запись.</span><span class="sxs-lookup"><span data-stu-id="62e62-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="62e62-146">Новый метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для выполнения операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="62e62-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="62e62-147">Метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) новой записи, чтобы освободить ссылку на контейнер.</span><span class="sxs-lookup"><span data-stu-id="62e62-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="62e62-148">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="62e62-148">Notes to implementers</span></span>

<span data-ttu-id="62e62-149">Все контейнеры, поддерживающие метод **иабконтаинер:: копентриес** , должны быть изменяемыми.</span><span class="sxs-lookup"><span data-stu-id="62e62-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="62e62-150">Установите флаг АБ_МОДИФИАБЛЕ контейнера в его свойстве \*\*пр_контаинер_флагс\*\* ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), чтобы указать, что он является изменяемым.</span><span class="sxs-lookup"><span data-stu-id="62e62-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="62e62-151">Необходимо поддерживать все флажки; Тем не менее, интерпретация и использование этих флагов зависит от реализации, то есть можно определить, что означает семантику флагов КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ и КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ в контексте реализации.</span><span class="sxs-lookup"><span data-stu-id="62e62-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="62e62-152">Если не удается определить, является ли запись повторяющейся, всегда разрешите копирование записи.</span><span class="sxs-lookup"><span data-stu-id="62e62-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="62e62-153">Если установлен флаг КРЕАТЕ_РЕПЛАЦЕ, всегда копируйте запись независимо от того, задано ли КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ или КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ, а также указывает, является ли запись повторяющейся.</span><span class="sxs-lookup"><span data-stu-id="62e62-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="62e62-154">Если КРЕАТЕ_РЕПЛАЦЕ не задано, а КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ задано, проверьте наличие дубликатов.</span><span class="sxs-lookup"><span data-stu-id="62e62-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="62e62-155">Если запись определена как повторяющаяся, не копируйте эту запись.</span><span class="sxs-lookup"><span data-stu-id="62e62-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="62e62-156">Не требуется поддержка КРЕАТЕ_РЕПЛАЦЕ; не поддерживающий КРЕАТЕ_РЕПЛАЦЕ означает, что вы можете спокойно проигнорировать его и всегда выполнять копирование.</span><span class="sxs-lookup"><span data-stu-id="62e62-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="62e62-157">ВозВращать предупреждение МАПИ_В_ПАРТИАЛ_КОМПЛЕТИОН только в том случае, если невозможно скопировать недублирующую запись.</span><span class="sxs-lookup"><span data-stu-id="62e62-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="62e62-158">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="62e62-158">Notes to callers</span></span>

<span data-ttu-id="62e62-159">Используйте флаги КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ и КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ, чтобы указать поставщику, как вы хотите, чтобы контейнер выполнил проверку на уникальную запись.</span><span class="sxs-lookup"><span data-stu-id="62e62-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="62e62-160">Если необходимо добавить запись независимо от того, является ли она дубликатом, не задавайте один из этих флагов или установите флаг КРЕАТЕ_РЕПЛАЦЕ.</span><span class="sxs-lookup"><span data-stu-id="62e62-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="62e62-161">КРЕАТЕ_РЕПЛАЦЕ указывает, что вы не следите, является ли запись повторяющейся; Вы всегда хотите, чтобы оно заменило исходную запись.</span><span class="sxs-lookup"><span data-stu-id="62e62-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="62e62-162">См. также</span><span class="sxs-lookup"><span data-stu-id="62e62-162">See also</span></span>



[<span data-ttu-id="62e62-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="62e62-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="62e62-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="62e62-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="62e62-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62e62-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="62e62-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="62e62-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="62e62-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="62e62-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

