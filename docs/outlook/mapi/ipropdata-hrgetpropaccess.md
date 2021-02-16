---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433439"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="55590-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="55590-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="55590-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55590-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55590-105">Извлекает уровень доступа и состояние для одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="55590-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="55590-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55590-106">Parameters</span></span>

 <span data-ttu-id="55590-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="55590-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="55590-108">[in, out] При вводе массив тегов свойств, которые указывают свойства, для которых необходимо получить уровни доступа и состояние; в противном случае указатель на значение NULL указывает, что **HrGetPropAccess** должен получать уровни доступа и состояние для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="55590-108">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties.</span></span> <span data-ttu-id="55590-109">В выходных данных массив тегов свойств, для которых были извлечены флаги доступа и состояния.</span><span class="sxs-lookup"><span data-stu-id="55590-109">On output, an array of property tags for which access and status flags were retrieved.</span></span> <span data-ttu-id="55590-110">Флаги хранятся в массиве, на который указывает параметр _lprgulAccess._</span><span class="sxs-lookup"><span data-stu-id="55590-110">The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="55590-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="55590-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="55590-112">[out] Указатель на массив битовых заметок.</span><span class="sxs-lookup"><span data-stu-id="55590-112">[out] A pointer to an array of flag bitmasks.</span></span> <span data-ttu-id="55590-113">Каждая битоваяmask указывает уровни доступа, состояние или оба свойства для каждого из свойств, указанных в массиве, на который указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="55590-113">Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="55590-114">Два массива являются позициональными в том, что первая битоваяmask, на которую указывает  _lprgulAccess,_ описывает первое свойство, на которое  _указывает lpPropTagArray,_ и так далее.</span><span class="sxs-lookup"><span data-stu-id="55590-114">The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on.</span></span> <span data-ttu-id="55590-115">Для каждого тега свойства можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="55590-115">For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="55590-116">**Флаг уровня доступа**</span><span class="sxs-lookup"><span data-stu-id="55590-116">**Access-level flag**</span></span>|<span data-ttu-id="55590-117">**Флаг состояния**</span><span class="sxs-lookup"><span data-stu-id="55590-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55590-118">IPROP_READONLY, что означает, что свойство не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="55590-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="55590-119">IPROP_CLEAN, что указывает на то, что свойство не было изменено.</span><span class="sxs-lookup"><span data-stu-id="55590-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="55590-120">IPROP_READWRITE, что указывает на то, что свойство можно изменить.</span><span class="sxs-lookup"><span data-stu-id="55590-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="55590-121">IPROP_DIRTY, что указывает на то, что свойство было изменено.</span><span class="sxs-lookup"><span data-stu-id="55590-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="55590-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55590-122">Return value</span></span>

<span data-ttu-id="55590-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="55590-123">S_OK</span></span> 
  
> <span data-ttu-id="55590-124">Успешно возвращены флаги уровня доступа и состояния для свойств.</span><span class="sxs-lookup"><span data-stu-id="55590-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="55590-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="55590-125">Remarks</span></span>

<span data-ttu-id="55590-126">Метод **IPropData::HrGetPropAccess** извлекает набор флагов, который указывает уровень доступа и состояние для одного или более свойств.</span><span class="sxs-lookup"><span data-stu-id="55590-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="55590-127">Примечания для вызывающих.</span><span class="sxs-lookup"><span data-stu-id="55590-127">Notes to callers:</span></span>

<span data-ttu-id="55590-128">**HrGetPropAccess можно** использовать для следующих целей:</span><span class="sxs-lookup"><span data-stu-id="55590-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="55590-129">Чтобы определить, изменил ли клиент или удалил свойство для нашего клиента.</span><span class="sxs-lookup"><span data-stu-id="55590-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="55590-130">Чтобы запретить клиенту изменять или удалять свойство с помощью методов [IMAPIProp.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="55590-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="55590-131">Если одно из свойств в массиве тегов свойств, на которые указывает  _lppPropTagArray,_ удалено, **HrGetPropAccess** устанавливает для записи массива значение 0 при выходе.</span><span class="sxs-lookup"><span data-stu-id="55590-131">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output.</span></span> <span data-ttu-id="55590-132">Если для  _lppPropTagArray_ установлено NULL и одно из свойств объекта удалено, удаленное свойство возвращается в массиве.</span><span class="sxs-lookup"><span data-stu-id="55590-132">If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="55590-133">Если свойство было изменено, его флаг IPROP_DIRTY в соответствующей записи в массиве, на который указывает _lprgulAccess._</span><span class="sxs-lookup"><span data-stu-id="55590-133">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to.</span></span> <span data-ttu-id="55590-134">Ни IPROP_READONLY, ни IPROP_READWRITE не будет установлено.</span><span class="sxs-lookup"><span data-stu-id="55590-134">Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="55590-135">Если свойство не было изменено или удалено, будет установлен только IPROP_READONLY или IPROP_READWRITE флаг.</span><span class="sxs-lookup"><span data-stu-id="55590-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55590-136">См. также</span><span class="sxs-lookup"><span data-stu-id="55590-136">See also</span></span>



[<span data-ttu-id="55590-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="55590-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="55590-138">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="55590-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

