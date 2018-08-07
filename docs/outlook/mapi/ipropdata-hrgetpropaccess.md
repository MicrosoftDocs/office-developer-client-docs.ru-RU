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
ms.openlocfilehash: 8441a4898659a5cd278265cb0199bb9097244aa3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809517"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="d24b9-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="d24b9-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="d24b9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d24b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d24b9-105">Получает уровень доступа и состояние для одной или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="d24b9-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="d24b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d24b9-106">Parameters</span></span>

 <span data-ttu-id="d24b9-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="d24b9-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="d24b9-108">[in, out] На входе массив тегов свойств, которые указывают свойства, для которого нужно извлечь уровни доступа и состоянии; в противном случае указатель на значение NULL, это означает, что **HrGetPropAccess** следует извлечь уровни доступа и состояние для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="d24b9-108">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties.</span></span> <span data-ttu-id="d24b9-109">На выходе были извлечены массив теги свойства для каких флаги доступа и состояние.</span><span class="sxs-lookup"><span data-stu-id="d24b9-109">On output, an array of property tags for which access and status flags were retrieved.</span></span> <span data-ttu-id="d24b9-110">Флаги хранятся в массиве указывает параметр _lprgulAccess_ .</span><span class="sxs-lookup"><span data-stu-id="d24b9-110">The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="d24b9-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="d24b9-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="d24b9-112">[out] Указатель на массив битовой маски флаг.</span><span class="sxs-lookup"><span data-stu-id="d24b9-112">[out] A pointer to an array of flag bitmasks.</span></span> <span data-ttu-id="d24b9-113">Каждый Битовая маска указывает уровни доступа или состояния или оба, для каждого из свойств, указанных в массиве указывает параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="d24b9-113">Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="d24b9-114">Двух массивов являются позиционные первого Битовая маска, указывающая, что _lprgulAccess_ моменты, которые описываются первого свойства, _lpPropTagArray_ указывает, и т. д.</span><span class="sxs-lookup"><span data-stu-id="d24b9-114">The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on.</span></span> <span data-ttu-id="d24b9-115">Для каждого свойства tag можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="d24b9-115">For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="d24b9-116">**Флаг уровня доступа**</span><span class="sxs-lookup"><span data-stu-id="d24b9-116">**Access-level flag**</span></span>|<span data-ttu-id="d24b9-117">**Состояние флага**</span><span class="sxs-lookup"><span data-stu-id="d24b9-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d24b9-118">IPROP_READONLY, это означает, что свойство не подлежит изменению.</span><span class="sxs-lookup"><span data-stu-id="d24b9-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="d24b9-119">IPROP_CLEAN, это означает, что свойство не были изменены.</span><span class="sxs-lookup"><span data-stu-id="d24b9-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="d24b9-120">IPROP_READWRITE, это означает, что свойство может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="d24b9-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="d24b9-121">IPROP_DIRTY, это означает, что свойство были изменены.</span><span class="sxs-lookup"><span data-stu-id="d24b9-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="d24b9-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="d24b9-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d24b9-123">S_OK</span></span> 
  
> <span data-ttu-id="d24b9-124">Флаги состояние и уровень доступа для свойств были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="d24b9-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d24b9-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="d24b9-125">Remarks</span></span>

<span data-ttu-id="d24b9-126">Метод **IPropData::HrGetPropAccess** получает набор флагов, которое указывает, уровень доступа и состояние для одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="d24b9-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d24b9-127">Примечания для вызывающих объектов:</span><span class="sxs-lookup"><span data-stu-id="d24b9-127">Notes to callers:</span></span>

<span data-ttu-id="d24b9-128">**HrGetPropAccess** можно использовать в следующих целях:</span><span class="sxs-lookup"><span data-stu-id="d24b9-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="d24b9-129">Чтобы определить ли это клиент, изменения или удаления для записи свойств.</span><span class="sxs-lookup"><span data-stu-id="d24b9-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="d24b9-130">Чтобы клиент не изменять или удалять свойства с помощью методов [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="d24b9-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="d24b9-131">Если одно из свойств в массиве тег свойства, на который указывает _lppPropTagArray_ была удалена, **HrGetPropAccess** задает запись массива 0 для вывода.</span><span class="sxs-lookup"><span data-stu-id="d24b9-131">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output.</span></span> <span data-ttu-id="d24b9-132">Если _lppPropTagArray_ значение NULL и одно из свойств объекта был удален, удаленные свойство возвращается в массиве.</span><span class="sxs-lookup"><span data-stu-id="d24b9-132">If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="d24b9-133">Если свойство был изменен, его IPROP_DIRTY флаг имеет значение в соответствующей записи в массиве, указывающий _lprgulAccess_ .</span><span class="sxs-lookup"><span data-stu-id="d24b9-133">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to.</span></span> <span data-ttu-id="d24b9-134">Будет установлено ни IPROP_READONLY, ни IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="d24b9-134">Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="d24b9-135">Если свойство не были изменены или удалены, будет установлен только флаг IPROP_READONLY или IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="d24b9-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d24b9-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d24b9-136">See also</span></span>



[<span data-ttu-id="d24b9-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="d24b9-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="d24b9-138">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d24b9-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

