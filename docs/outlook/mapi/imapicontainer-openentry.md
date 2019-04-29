---
title: Имапиконтаинеропенентри
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423638"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="62f4c-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="62f4c-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="62f4c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62f4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62f4c-105">Открывает объект в контейнере, возвращая указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="62f4c-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="62f4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="62f4c-106">Parameters</span></span>

 <span data-ttu-id="62f4c-107">_Кбентрид_</span><span class="sxs-lookup"><span data-stu-id="62f4c-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="62f4c-108">возврата Число байтов в идентификаторе записи, на которое указывает параметр _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="62f4c-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="62f4c-109">_Лпентрид_</span><span class="sxs-lookup"><span data-stu-id="62f4c-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="62f4c-110">возврата Указатель на идентификатор записи объекта, который требуется открыть.</span><span class="sxs-lookup"><span data-stu-id="62f4c-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="62f4c-111">Если для _лпентрид_ ЗАДАНО значение null, открывается контейнер верхнего уровня в иерархии контейнера.</span><span class="sxs-lookup"><span data-stu-id="62f4c-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="62f4c-112">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="62f4c-112">_lpInterface_</span></span>
  
> <span data-ttu-id="62f4c-113">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="62f4c-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="62f4c-114">При передаче значения NULL в идентификатор возвращаемого стандартного интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="62f4c-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="62f4c-115">Для сообщений стандартным интерфейсом является [имапимессажесите: IUnknown](imapimessagesiteiunknown.md); для папок это [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="62f4c-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="62f4c-116">Стандартные интерфейсы для объектов адресных книг [: идистлист: IMAPIContainer](idistlistimapicontainer.md) для списка рассылки и [имаилусер: IMAPIProp](imailuserimapiprop.md) для пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="62f4c-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="62f4c-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62f4c-117">_ulFlags_</span></span>
  
> <span data-ttu-id="62f4c-118">возврата Битовая маска флагов, определяющих способ открытия объекта.</span><span class="sxs-lookup"><span data-stu-id="62f4c-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="62f4c-119">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="62f4c-119">The following flags can be set:</span></span>
    
<span data-ttu-id="62f4c-120">МАПИ_БЕСТ_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="62f4c-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="62f4c-121">ЗаПрашивает открытие объекта с максимальными сетевыми разрешениями, разрешенными для пользователя, и максимальным доступом к клиентскому приложению.</span><span class="sxs-lookup"><span data-stu-id="62f4c-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="62f4c-122">Например, если у клиента есть разрешение на чтение и запись, объект должен быть открыт с разрешением на чтение и запись; Если клиент имеет доступ только для чтения, объект должен быть открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="62f4c-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="62f4c-123">МАПИ_ДЕФЕРРЕД_ЕРРОРС</span><span class="sxs-lookup"><span data-stu-id="62f4c-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="62f4c-124">Разрешает успешное возвращение **OpenEntry** , возможно, перед тем, как объект будет полностью доступен для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="62f4c-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="62f4c-125">Если объект недоступен, то выполнение следующего вызова объекта может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="62f4c-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="62f4c-126">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="62f4c-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="62f4c-127">ЗаПрашивает разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="62f4c-127">Requests read/write permission.</span></span> <span data-ttu-id="62f4c-128">По умолчанию объекты открываются с доступом только для чтения, и клиенты не должны работать в предположении, что предоставлено разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="62f4c-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="62f4c-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="62f4c-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="62f4c-130">Показывает элементы, которые в настоящее время помечены как обратимо удаленные — то есть они находятся на стадии хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="62f4c-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="62f4c-131">_Лпулобжтипе_</span><span class="sxs-lookup"><span data-stu-id="62f4c-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="62f4c-132">вышли Указатель на тип открытого объекта.</span><span class="sxs-lookup"><span data-stu-id="62f4c-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="62f4c-133">_Лппунк_</span><span class="sxs-lookup"><span data-stu-id="62f4c-133">_lppUnk_</span></span>
  
> <span data-ttu-id="62f4c-134">вышли Указатель на указатель на реализацию интерфейса, используемый для доступа к открытому объекту.</span><span class="sxs-lookup"><span data-stu-id="62f4c-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62f4c-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="62f4c-135">Return value</span></span>

<span data-ttu-id="62f4c-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="62f4c-136">S_OK</span></span> 
  
> <span data-ttu-id="62f4c-137">Объект был успешно открыт.</span><span class="sxs-lookup"><span data-stu-id="62f4c-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="62f4c-138">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="62f4c-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="62f4c-139">Пользователь не имеет достаточных разрешений на открытие объекта или попытка открыть объект, доступный только для чтения, с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="62f4c-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="62f4c-140">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="62f4c-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="62f4c-141">Идентификатор записи, заданный параметром _лпентрид_ , не представляет объект.</span><span class="sxs-lookup"><span data-stu-id="62f4c-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="62f4c-142">МАПИ_Е_УНКНОВН_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="62f4c-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="62f4c-143">Идентификатор записи в параметре _лпентрид_ имеет формат, отличный от формата, распознаваемого контейнером.</span><span class="sxs-lookup"><span data-stu-id="62f4c-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="62f4c-144">Примечания</span><span class="sxs-lookup"><span data-stu-id="62f4c-144">Remarks</span></span>

<span data-ttu-id="62f4c-145">Метод **IMAPIContainer:: OpenEntry** открывает объект в контейнере и возвращает указатель на реализацию интерфейса, который будет использоваться для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="62f4c-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="62f4c-146">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="62f4c-146">Notes to callers</span></span>

<span data-ttu-id="62f4c-147">Так как поставщики услуг не обязаны возвращать реализацию интерфейса типа, указанного идентификатором интерфейса, в параметре _лпинтерфаце_ , проверьте значение, указываемое параметром _лпулобжтипе_ .</span><span class="sxs-lookup"><span data-stu-id="62f4c-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="62f4c-148">При необходимости приведите указатель, возвращенный в _лппунк_ , к указателю соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="62f4c-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="62f4c-149">По умолчанию поставщики услуг открывают объекты с доступом только для чтения, если не установлен флаг МАПИ_МОДИФИ или МАПИ_БЕСТ_АКЦЕСС.</span><span class="sxs-lookup"><span data-stu-id="62f4c-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="62f4c-150">Когда установлен один из этих флагов, поставщики услуг пытаются вернуть изменяемый объект.</span><span class="sxs-lookup"><span data-stu-id="62f4c-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="62f4c-151">Тем не менее, это не предполагается, так как вы запросили изменяемый объект, у которого открытый объект имеет разрешение на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="62f4c-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="62f4c-152">Необходимо либо запланировать вероятность последующего изменения, либо получить свойство **пр_акцесс_левел** объекта, чтобы определить уровень доступа, предоставленный **OpenEntry**.</span><span class="sxs-lookup"><span data-stu-id="62f4c-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="62f4c-153">См. также</span><span class="sxs-lookup"><span data-stu-id="62f4c-153">See also</span></span>



[<span data-ttu-id="62f4c-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="62f4c-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

