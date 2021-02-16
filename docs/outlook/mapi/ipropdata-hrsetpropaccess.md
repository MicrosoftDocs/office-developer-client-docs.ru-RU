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
ms.openlocfilehash: 9e443302e49bad4a586b657a6de298dafbeefab4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437856"
---
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="51ec5-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="51ec5-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="51ec5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51ec5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51ec5-105">Задает уровень доступа или состояние для одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="51ec5-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="51ec5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51ec5-106">Parameters</span></span>

 <span data-ttu-id="51ec5-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="51ec5-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="51ec5-108">[in] Указатель на массив тегов свойств, которые указывают изменимые свойства.</span><span class="sxs-lookup"><span data-stu-id="51ec5-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="51ec5-109">_rgulAccess_</span><span class="sxs-lookup"><span data-stu-id="51ec5-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="51ec5-110">[in] Массив битовых заметок.</span><span class="sxs-lookup"><span data-stu-id="51ec5-110">[in] An array of flag bitmasks.</span></span> <span data-ttu-id="51ec5-111">Каждая битоваяmask указывает уровни доступа, состояние или оба свойства для каждого из свойств, указанных в массиве, на которое указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="51ec5-111">Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to.</span></span> <span data-ttu-id="51ec5-112">Два массива являются позициональными, так как первая битоваяmask в  _rgulAccess_ описывает первое свойство, на которое  _указывает lpPropTagArray,_ и так далее.</span><span class="sxs-lookup"><span data-stu-id="51ec5-112">The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on.</span></span> <span data-ttu-id="51ec5-113">Для каждого тега свойства можно установить один флаг уровня доступа и один флаг состояния.</span><span class="sxs-lookup"><span data-stu-id="51ec5-113">For each property tag, one access-level flag and one status flag can be set.</span></span> <span data-ttu-id="51ec5-114">В следующей таблице показаны возможные флаги.</span><span class="sxs-lookup"><span data-stu-id="51ec5-114">The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="51ec5-115">**Флаг уровня доступа**</span><span class="sxs-lookup"><span data-stu-id="51ec5-115">**Access-level flag**</span></span>|<span data-ttu-id="51ec5-116">**Флаг состояния**</span><span class="sxs-lookup"><span data-stu-id="51ec5-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51ec5-117">IPROP_READONLY, что указывает на то, что свойство не может быть изменено</span><span class="sxs-lookup"><span data-stu-id="51ec5-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="51ec5-118">IPROP_CLEAN, что указывает на то, что свойство не было изменено.</span><span class="sxs-lookup"><span data-stu-id="51ec5-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="51ec5-119">IPROP_READWRITE, что указывает на то, что свойство можно изменить.</span><span class="sxs-lookup"><span data-stu-id="51ec5-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="51ec5-120">IPROP_DIRTY, что указывает на то, что свойство было изменено.</span><span class="sxs-lookup"><span data-stu-id="51ec5-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="51ec5-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51ec5-121">Return value</span></span>

<span data-ttu-id="51ec5-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="51ec5-122">S_OK</span></span> 
  
> <span data-ttu-id="51ec5-123">Флаги уровня доступа и состояния успешно установлены.</span><span class="sxs-lookup"><span data-stu-id="51ec5-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="51ec5-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="51ec5-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="51ec5-125">Предпринята попытка установить свойство для объекта, доступного только для чтения, или объекта, для которого у вызываемого объекта недостаточно разрешений.</span><span class="sxs-lookup"><span data-stu-id="51ec5-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="51ec5-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="51ec5-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="51ec5-127">Параметр  _rgulAccess_ содержит недопустимое сочетание флагов, например IPROP_READONLY и IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="51ec5-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="51ec5-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="51ec5-128">Remarks</span></span>

<span data-ttu-id="51ec5-129">Метод **IPropData::HrSetPropAccess** изменяет уровень доступа и состояние свойств, которые определены тегами свойств в структуре [SPropTagArray,](sproptagarray.md) на которые указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="51ec5-129">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="51ec5-130">Для каждого свойства в массиве  _rgulAccess_ есть соответствующая запись.</span><span class="sxs-lookup"><span data-stu-id="51ec5-130">For each property, there is a corresponding entry in the  _rgulAccess_ array.</span></span> <span data-ttu-id="51ec5-131">Для записи можно установить один флаг, который указывает уровень доступа свойства, а другой флаг, который указывает его состояние.</span><span class="sxs-lookup"><span data-stu-id="51ec5-131">The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51ec5-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="51ec5-132">Notes to callers</span></span>

<span data-ttu-id="51ec5-133">Используйте **HrSetPropAccess,** чтобы определить, когда изменяется определенное значение свойства, и изменить уровень доступа для одного или более свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="51ec5-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51ec5-134">См. также</span><span class="sxs-lookup"><span data-stu-id="51ec5-134">See also</span></span>



[<span data-ttu-id="51ec5-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="51ec5-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="51ec5-136">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51ec5-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

