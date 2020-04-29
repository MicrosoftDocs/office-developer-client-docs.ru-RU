---
title: ипропдатахрсетпропакцесс
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
# <a name="ipropdatahrsetpropaccess"></a><span data-ttu-id="c7e64-103">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="c7e64-103">IPropData::HrSetPropAccess</span></span>

  
  
<span data-ttu-id="c7e64-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7e64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7e64-105">Задает уровень доступа или состояние для одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="c7e64-105">Sets the access level or status for one or more of the object's properties.</span></span>
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="c7e64-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7e64-106">Parameters</span></span>

 <span data-ttu-id="c7e64-107">_лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="c7e64-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c7e64-108">возврата Указатель на массив тегов свойств, указывающий свойства, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="c7e64-108">[in] A pointer to an array of property tags that indicate the properties to be modified.</span></span> 
    
 <span data-ttu-id="c7e64-109">_ргулакцесс_</span><span class="sxs-lookup"><span data-stu-id="c7e64-109">_rgulAccess_</span></span>
  
> <span data-ttu-id="c7e64-110">возврата Массив битовых масок флагов.</span><span class="sxs-lookup"><span data-stu-id="c7e64-110">[in] An array of flag bitmasks.</span></span> <span data-ttu-id="c7e64-111">Каждая битовая маска указывает уровни доступа или состояние, или и то, и другое, для каждого из свойств, определенных в массиве, на который указывает параметр _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="c7e64-111">Each bitmask indicates the access levels or status, or both, for each of the properties identified in the array that the  _lpPropTagArray_ parameter points to.</span></span> <span data-ttu-id="c7e64-112">Два массива располагаются в первой битовой маске в _ргулакцесс_ , в которой описывается первое свойство, на которое указывает _лппроптагаррай_ , и т. д.</span><span class="sxs-lookup"><span data-stu-id="c7e64-112">The two arrays are positional in that the first bitmask in  _rgulAccess_ describes the first property that  _lpPropTagArray_ points to, and so on.</span></span> <span data-ttu-id="c7e64-113">Для каждого тега свойства можно задать один флаг уровня доступа и один флаг состояния.</span><span class="sxs-lookup"><span data-stu-id="c7e64-113">For each property tag, one access-level flag and one status flag can be set.</span></span> <span data-ttu-id="c7e64-114">В следующей таблице приведены возможные флаги.</span><span class="sxs-lookup"><span data-stu-id="c7e64-114">The following table shows the possible flags.</span></span> 
    
|<span data-ttu-id="c7e64-115">**Флаг уровня доступа**</span><span class="sxs-lookup"><span data-stu-id="c7e64-115">**Access-level flag**</span></span>|<span data-ttu-id="c7e64-116">**Флаг состояния**</span><span class="sxs-lookup"><span data-stu-id="c7e64-116">**Status flag**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7e64-117">IPROP_READONLY, что указывает на то, что свойство не может быть изменено</span><span class="sxs-lookup"><span data-stu-id="c7e64-117">IPROP_READONLY, which indicates that the property cannot be modified</span></span>  <br/> |<span data-ttu-id="c7e64-118">IPROP_CLEAN, которое указывает, что свойство не было изменено.</span><span class="sxs-lookup"><span data-stu-id="c7e64-118">IPROP_CLEAN, which indicates that the property has not been modified.</span></span>  <br/> |
|<span data-ttu-id="c7e64-119">IPROP_READWRITE, которое указывает, что свойство можно изменить.</span><span class="sxs-lookup"><span data-stu-id="c7e64-119">IPROP_READWRITE, which indicates that the property can be modified.</span></span>  <br/> |<span data-ttu-id="c7e64-120">IPROP_DIRTY, показывающее, что свойство было изменено.</span><span class="sxs-lookup"><span data-stu-id="c7e64-120">IPROP_DIRTY, which indicates that the property has been modified.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="c7e64-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7e64-121">Return value</span></span>

<span data-ttu-id="c7e64-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7e64-122">S_OK</span></span> 
  
> <span data-ttu-id="c7e64-123">Флаги уровня доступа и состояния успешно заданы.</span><span class="sxs-lookup"><span data-stu-id="c7e64-123">The access-level and status flags have been successfully set.</span></span>
    
<span data-ttu-id="c7e64-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c7e64-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c7e64-125">Предпринята попытка задать свойство для объекта, доступного только для чтения, или объект, для которого вызывающий не хватает разрешений.</span><span class="sxs-lookup"><span data-stu-id="c7e64-125">An attempt was made to set a property on a read-only object or an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="c7e64-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7e64-126">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="c7e64-127">Параметр _ргулакцесс_ содержит недопустимое сочетание флагов, таких как IPROP_READONLY и IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="c7e64-127">The  _rgulAccess_ parameter contains an invalid combination of flags, such as IPROP_READONLY and IPROP_READWRITE.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7e64-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7e64-128">Remarks</span></span>

<span data-ttu-id="c7e64-129">Метод **ипропдата:: хрсетпропакцесс** изменяет уровень доступа и состояние для свойств, определяемых тегами свойств в структуре [спроптагаррай](sproptagarray.md) , на которую указывает параметр _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="c7e64-129">The **IPropData::HrSetPropAccess** method changes the access level and status for the properties that are identified by the property tags in the [SPropTagArray](sproptagarray.md) structure pointed to by the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="c7e64-130">Для каждого свойства существует соответствующая запись в массиве _ргулакцесс_ .</span><span class="sxs-lookup"><span data-stu-id="c7e64-130">For each property, there is a corresponding entry in the  _rgulAccess_ array.</span></span> <span data-ttu-id="c7e64-131">Для записи можно задать один флаг, указывающий на уровень доступа свойства и другой флаг, указывающий на его состояние.</span><span class="sxs-lookup"><span data-stu-id="c7e64-131">The entry can be set to one flag that indicates the property's access level and another flag that indicates its status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c7e64-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c7e64-132">Notes to callers</span></span>

<span data-ttu-id="c7e64-133">Используйте **хрсетпропакцесс** , чтобы определить, изменяется ли определенное значение свойства, а также для изменения уровня доступа для одного или нескольких свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="c7e64-133">Use **HrSetPropAccess** to determine when a particular property value changes and to change the access level for one or more of an object's properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7e64-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c7e64-134">See also</span></span>



[<span data-ttu-id="c7e64-135">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="c7e64-135">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="c7e64-136">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c7e64-136">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

