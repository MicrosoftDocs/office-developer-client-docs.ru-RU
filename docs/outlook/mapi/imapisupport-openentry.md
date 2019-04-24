---
title: Имаписуппортопенентри
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326349"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="65460-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="65460-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="65460-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65460-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65460-105">Открывает объект и возвращает указатель интерфейса для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="65460-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="65460-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="65460-106">Parameters</span></span>

 <span data-ttu-id="65460-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="65460-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="65460-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="65460-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="65460-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="65460-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="65460-110">возврата Указатель на идентификатор записи объекта, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="65460-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="65460-111">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="65460-111">_lpInterface_</span></span>
  
> <span data-ttu-id="65460-112">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="65460-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="65460-113">Передача результатов NULL в стандартный интерфейс возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="65460-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="65460-114">Например, если открываемый объект является сообщением, стандартный интерфейс — [iMessage](imessageimapiprop.md); для папок это [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="65460-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="65460-115">Стандартные интерфейсы для объектов адресных книг — [идистлист](idistlistimapicontainer.md) для списка рассылки и [имаилусер](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="65460-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="65460-116">_Улопенфлагс_</span><span class="sxs-lookup"><span data-stu-id="65460-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="65460-117">возврата Битовая маска флагов, определяющих способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="65460-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="65460-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="65460-118">The following flags can be set:</span></span>
    
<span data-ttu-id="65460-119">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="65460-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="65460-120">Запрос на открытие объекта с максимальными сетевыми разрешениями, разрешенными для вызывающего абонента.</span><span class="sxs-lookup"><span data-stu-id="65460-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="65460-121">Например, если у вызывающего абонента есть разрешение на чтение и запись, объект должен быть открыт для чтения и записи; Если вызывающий абонент имеет разрешение "только чтение", объект должен быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="65460-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="65460-122">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="65460-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="65460-123">Разрешает успешное возвращение **OpenEntry** , возможно, перед тем, как объект будет полностью доступен вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="65460-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="65460-124">Если объект недоступен, то выполнение последующего вызова объекта может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="65460-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="65460-125">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="65460-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="65460-126">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="65460-126">Requests read/write permission.</span></span> <span data-ttu-id="65460-127">По умолчанию объекты открываются как доступные только для чтения, и абоненты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="65460-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="65460-128">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="65460-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="65460-129">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="65460-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="65460-130">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="65460-130">_lppUnk_</span></span>
  
> <span data-ttu-id="65460-131">вышли Указатель на указатель на открытый объект.</span><span class="sxs-lookup"><span data-stu-id="65460-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65460-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65460-132">Return value</span></span>

<span data-ttu-id="65460-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="65460-133">S_OK</span></span> 
  
> <span data-ttu-id="65460-134">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="65460-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="65460-135">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="65460-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="65460-136">Предпринята попытка изменить объект, предназначенный только для чтения, или попытка получить доступ к объекту, для которого у пользователя недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="65460-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="65460-137">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="65460-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="65460-138">Отсутствует объект, связанный с идентификатором записи, переданным в параметре _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="65460-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="65460-139">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="65460-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="65460-140">Идентификатор записи, переданный в параметре _лпентрид_ , имеет нераспознаваемый формат.</span><span class="sxs-lookup"><span data-stu-id="65460-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="65460-141">Это значение обычно возвращается, если поставщик адресной книги, который содержит объект, не открыт.</span><span class="sxs-lookup"><span data-stu-id="65460-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65460-142">Замечания</span><span class="sxs-lookup"><span data-stu-id="65460-142">Remarks</span></span>

<span data-ttu-id="65460-143">Метод **имаписуппорт:: OpenEntry** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="65460-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="65460-144">Поставщики услуг вызывают **имаписуппорт:: OpenEntry** для получения указателя на интерфейс, который можно использовать для доступа к определенному объекту.</span><span class="sxs-lookup"><span data-stu-id="65460-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="65460-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="65460-145">Notes to callers</span></span>

<span data-ttu-id="65460-146">Call **имаписуппорт:: OpenEntry** только в том случае, если вы не знаете тип открываемого объекта.</span><span class="sxs-lookup"><span data-stu-id="65460-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="65460-147">Если вы знаете, что открываете папку или сообщение, вызовите [IMsgStore:: OpenEntry](imsgstore-openentry.md) .</span><span class="sxs-lookup"><span data-stu-id="65460-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="65460-148">Если вы знаете, что открываете контейнер адресной книги, пользователя обмена сообщениями или списка рассылки, вызовите [IAddrBook:: OpenEntry](iaddrbook-openentry.md).</span><span class="sxs-lookup"><span data-stu-id="65460-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="65460-149">Эти более конкретные методы работают быстрее, чем **имаписуппорт:: OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="65460-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="65460-150">**Имаписуппорт:: OpenEntry** открывает все объекты только для чтения, если вы не установили флаг МАПИ_МОДИФИ или мапи_бест_акцесс в параметре _ulFlags_ и у вас достаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="65460-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="65460-151">Установка одного из этих флагов не гарантирует определенный тип доступа; предоставленные разрешения зависят от уровня доступа, объекта и поставщика услуг, владеющего объектом.</span><span class="sxs-lookup"><span data-stu-id="65460-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="65460-152">Чтобы определить уровень доступа открытого объекта, извлеките его свойство **пр_акцесс_левел** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="65460-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="65460-153">Проверьте значение, возвращенное в параметре _лпулобжтипе_ , чтобы определить, что возвращаемый тип объекта является ожидаемым.</span><span class="sxs-lookup"><span data-stu-id="65460-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="65460-154">Если тип объекта является ожидаемым, приведите указатель из параметра _лппунк_ к указателю соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="65460-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="65460-155">Например, если вы открываете папку, приведите _лппунк_ к указателю типа лпмапифолдер.</span><span class="sxs-lookup"><span data-stu-id="65460-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65460-156">См. также</span><span class="sxs-lookup"><span data-stu-id="65460-156">See also</span></span>



[<span data-ttu-id="65460-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="65460-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

