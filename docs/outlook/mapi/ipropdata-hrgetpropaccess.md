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
ms.openlocfilehash: 64b0c0501a6ef4471f97e82b231ef430681f1306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573392"
---
# <a name="ipropdatahrgetpropaccess"></a><span data-ttu-id="8c2c2-103">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="8c2c2-103">IPropData::HrGetPropAccess</span></span>

  
  
<span data-ttu-id="8c2c2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c2c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c2c2-105">Получает уровень доступа и состояние для одной или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-105">Retrieves the access level and status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="8c2c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c2c2-106">Parameters</span></span>

 <span data-ttu-id="8c2c2-107">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="8c2c2-107">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="8c2c2-108">[in, out] На входе массив тегов свойств, которые указывают свойства, для которого нужно извлечь уровни доступа и состоянии; в противном случае указатель на значение NULL, это означает, что **HrGetPropAccess** следует извлечь уровни доступа и состояние для всех свойств.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-108">[in, out] On input, an array of property tags that indicate the properties for which to retrieve access levels and status; otherwise, a pointer to NULL, which indicates that **HrGetPropAccess** should retrieve access levels and status for all properties.</span></span> <span data-ttu-id="8c2c2-109">На выходе были извлечены массив теги свойства для каких флаги доступа и состояние.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-109">On output, an array of property tags for which access and status flags were retrieved.</span></span> <span data-ttu-id="8c2c2-110">Флаги хранятся в массиве указывает параметр _lprgulAccess_ .</span><span class="sxs-lookup"><span data-stu-id="8c2c2-110">The flags are stored in the array pointed to by the  _lprgulAccess_ parameter.</span></span> 
    
 <span data-ttu-id="8c2c2-111">_lprgulAccess_</span><span class="sxs-lookup"><span data-stu-id="8c2c2-111">_lprgulAccess_</span></span>
  
> <span data-ttu-id="8c2c2-112">[out] Указатель на массив битовой маски флаг.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-112">[out] A pointer to an array of flag bitmasks.</span></span> <span data-ttu-id="8c2c2-113">Каждый Битовая маска указывает уровни доступа или состояния или оба, для каждого из свойств, указанных в массиве указывает параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="8c2c2-113">Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="8c2c2-114">Двух массивов являются позиционные первого Битовая маска, указывающая, что _lprgulAccess_ моменты, которые описываются первого свойства, _lpPropTagArray_ указывает, и т. д.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-114">The two arrays are positional in that the first bitmask that  _lprgulAccess_ points to describes the first property that  _lpPropTagArray_ points to, and so on.</span></span> <span data-ttu-id="8c2c2-115">Для каждого свойства tag можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-115">For each property tag, the following flags can be set:</span></span> 
    
|<span data-ttu-id="8c2c2-116">**Флаг уровня доступа**</span><span class="sxs-lookup"><span data-stu-id="8c2c2-116">**Access-level flag**</span></span>|<span data-ttu-id="8c2c2-117">**Состояние флага**</span><span class="sxs-lookup"><span data-stu-id="8c2c2-117">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8c2c2-118">IPROP_READONLY, это означает, что свойство не подлежит изменению.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-118">IPROP_READONLY, which indicates that the property cannot be modified.</span></span>  <br/> |<span data-ttu-id="8c2c2-119">IPROP_CLEAN, это означает, что свойство не были изменены.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-119">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="8c2c2-120">IPROP_READWRITE, это означает, что свойство может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-120">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="8c2c2-121">IPROP_DIRTY, это означает, что свойство были изменены.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-121">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="8c2c2-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="8c2c2-122">Return value</span></span>

<span data-ttu-id="8c2c2-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="8c2c2-123">S_OK</span></span> 
  
> <span data-ttu-id="8c2c2-124">Флаги состояние и уровень доступа для свойств были успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-124">The access level and status flags for the properties were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8c2c2-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c2c2-125">Remarks</span></span>

<span data-ttu-id="8c2c2-126">Метод **IPropData::HrGetPropAccess** получает набор флагов, которое указывает, уровень доступа и состояние для одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-126">The **IPropData::HrGetPropAccess** method retrieves a set of flags that indicates the access level and status for one or more properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8c2c2-127">Примечания для вызывающих объектов:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-127">Notes to callers:</span></span>

<span data-ttu-id="8c2c2-128">**HrGetPropAccess** можно использовать в следующих целях:</span><span class="sxs-lookup"><span data-stu-id="8c2c2-128">You can use **HrGetPropAccess** for the following purposes:</span></span> 
  
- <span data-ttu-id="8c2c2-129">Чтобы определить ли это клиент, изменения или удаления для записи свойств.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-129">To determine whether a client changed or deleted a writable property.</span></span>
    
- <span data-ttu-id="8c2c2-130">Чтобы клиент не изменять или удалять свойства с помощью методов [IMAPIProp](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8c2c2-130">To prevent a client from changing or deleting a property by using the [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
    
<span data-ttu-id="8c2c2-131">Если одно из свойств в массиве тег свойства, на который указывает _lppPropTagArray_ была удалена, **HrGetPropAccess** задает запись массива 0 для вывода.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-131">If one of the properties in the property tag array pointed to by  _lppPropTagArray_ has been deleted, **HrGetPropAccess** sets the array entry to 0 on output.</span></span> <span data-ttu-id="8c2c2-132">Если _lppPropTagArray_ значение NULL и одно из свойств объекта был удален, удаленные свойство возвращается в массиве.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-132">If you set  _lppPropTagArray_ to NULL and one of the object's properties has been deleted, the deleted property is returned in the array.</span></span> 
  
<span data-ttu-id="8c2c2-133">Если свойство был изменен, его IPROP_DIRTY флаг имеет значение в соответствующей записи в массиве, указывающий _lprgulAccess_ .</span><span class="sxs-lookup"><span data-stu-id="8c2c2-133">If a property has been modified, its IPROP_DIRTY flag is set in the corresponding entry in the array that  _lprgulAccess_ points to.</span></span> <span data-ttu-id="8c2c2-134">Будет установлено ни IPROP_READONLY, ни IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-134">Neither IPROP_READONLY nor IPROP_READWRITE will be set.</span></span> 
  
<span data-ttu-id="8c2c2-135">Если свойство не были изменены или удалены, будет установлен только флаг IPROP_READONLY или IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="8c2c2-135">If a property has not been modified or deleted, only the IPROP_READONLY or IPROP_READWRITE flag will be set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8c2c2-136">См. также</span><span class="sxs-lookup"><span data-stu-id="8c2c2-136">See also</span></span>



[<span data-ttu-id="8c2c2-137">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="8c2c2-137">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="8c2c2-138">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8c2c2-138">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

