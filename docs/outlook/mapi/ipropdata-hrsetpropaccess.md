---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d0054e54d56fbe1cc6d6d783ffcd6330d8ab2e6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564663"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="42dc3-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="42dc3-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="42dc3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42dc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42dc3-105">Задает уровень доступа или состояния для одной или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="42dc3-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="42dc3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42dc3-106">Parameters</span></span>

 <span data-ttu-id="42dc3-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="42dc3-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="42dc3-108">[in] Указатель на массив тегов свойств, которые указывают свойства, которые нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="42dc3-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="42dc3-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="42dc3-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="42dc3-110">[in] Массив битовой маски флаг.</span><span class="sxs-lookup"><span data-stu-id="42dc3-110">[in] An array of flag bitmasks.</span></span> <span data-ttu-id="42dc3-111">Каждый Битовая маска указывает уровни доступа или состояния или оба, для каждого свойства, определенный в массиве, параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="42dc3-111">Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to.</span></span> <span data-ttu-id="42dc3-112">Двух массивов являются позиционные первого битовой маски в _rgulAccess_ описывает первого свойства, указывающий _lpPropTagArray_ , и т. д.</span><span class="sxs-lookup"><span data-stu-id="42dc3-112">The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on.</span></span> <span data-ttu-id="42dc3-113">Для каждого свойства tag можно задать один уровень доступа флаг и флаг одного состояния.</span><span class="sxs-lookup"><span data-stu-id="42dc3-113">For each property tag, one access-level flag and one status flag can be set.</span></span> <span data-ttu-id="42dc3-114">В следующей таблице перечислены возможные флаги.</span><span class="sxs-lookup"><span data-stu-id="42dc3-114">The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="42dc3-115">**Флаг уровня доступа**</span><span class="sxs-lookup"><span data-stu-id="42dc3-115">**Access-level flag**</span></span>|<span data-ttu-id="42dc3-116">**Состояние флага**</span><span class="sxs-lookup"><span data-stu-id="42dc3-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42dc3-117">IPROP_READONLY, это означает, что свойство не может изменить</span><span class="sxs-lookup"><span data-stu-id="42dc3-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="42dc3-118">IPROP_CLEAN, это означает, что свойство не были изменены.</span><span class="sxs-lookup"><span data-stu-id="42dc3-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="42dc3-119">IPROP_READWRITE, это означает, что свойство может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="42dc3-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="42dc3-120">IPROP_DIRTY, это означает, что свойство были изменены.</span><span class="sxs-lookup"><span data-stu-id="42dc3-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="42dc3-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="42dc3-121">Return value</span></span>

<span data-ttu-id="42dc3-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="42dc3-122">S_OK</span></span> 
  
> <span data-ttu-id="42dc3-123">Флаги уровень доступа и состояние были успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="42dc3-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="42dc3-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="42dc3-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="42dc3-125">Предпринята попытка для задания свойства на объект только для чтения или объект, для которого вызывающий не имеет разрешений.</span><span class="sxs-lookup"><span data-stu-id="42dc3-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="42dc3-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="42dc3-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="42dc3-127">Параметр _rgulAccess_ содержит недопустимое сочетание флаги, такие как IPROP_READONLY и IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="42dc3-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42dc3-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="42dc3-128">Remarks</span></span>

<span data-ttu-id="42dc3-129">Метод **IPropData::HrSetPropAccess** изменяет уровень доступа и состояние для свойств, которые определяются теги свойства в структуре [SPropTagArray](sproptagarray.md) указывает параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="42dc3-129">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="42dc3-130">Для каждого свойства существует соответствующие записи в массиве _rgulAccess_ .</span><span class="sxs-lookup"><span data-stu-id="42dc3-130">For each property, there is a corresponding entry in the  _rgulAccess_ array.</span></span> <span data-ttu-id="42dc3-131">Операция может быть присвоено один флаг, указывающий, уровень доступа этого свойства, а другой флаг, указывающий, его состояние.</span><span class="sxs-lookup"><span data-stu-id="42dc3-131">The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="42dc3-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="42dc3-132">Notes to callers</span></span>

<span data-ttu-id="42dc3-133">Используйте **HrSetPropAccess** для определения при изменении значения отдельного свойства и изменить уровень доступа для одной или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="42dc3-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42dc3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="42dc3-134">See also</span></span>



[<span data-ttu-id="42dc3-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="42dc3-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="42dc3-136">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="42dc3-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

