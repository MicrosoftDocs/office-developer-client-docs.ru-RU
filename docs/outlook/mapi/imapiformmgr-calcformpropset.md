---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436428"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="41a9d-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="41a9d-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="41a9d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41a9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41a9d-105">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="41a9d-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="41a9d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41a9d-106">Parameters</span></span>

 <span data-ttu-id="41a9d-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="41a9d-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="41a9d-108">[in] Указатель на массив информационных объектов формы, которые определяют формы, для которых возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="41a9d-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="41a9d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41a9d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="41a9d-110">[in] Битоваяmas флагов, которая управляет возвратом массива свойств в _параметре ppResults._</span><span class="sxs-lookup"><span data-stu-id="41a9d-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="41a9d-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="41a9d-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="41a9d-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="41a9d-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="41a9d-113">Возвращенный массив содержит пересечение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="41a9d-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="41a9d-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="41a9d-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="41a9d-115">Возвращенный массив содержит объединение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="41a9d-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="41a9d-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="41a9d-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="41a9d-117">Строки, возвращенные в массиве, имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="41a9d-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="41a9d-118">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="41a9d-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="41a9d-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="41a9d-119">_ppResults_</span></span>
  
> <span data-ttu-id="41a9d-120">[out] Указатель на указатель на возвращенную структуру [SMAPIFormPropArray,](smapiformproparray.md) которая содержит свойства, которые используются формами.</span><span class="sxs-lookup"><span data-stu-id="41a9d-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="41a9d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41a9d-121">Return value</span></span>

<span data-ttu-id="41a9d-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="41a9d-122">S_OK</span></span> 
  
> <span data-ttu-id="41a9d-123">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="41a9d-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="41a9d-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="41a9d-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="41a9d-125">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="41a9d-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41a9d-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="41a9d-126">Remarks</span></span>

<span data-ttu-id="41a9d-127">Посетители форм вызывают метод **IMAPIFormMgr::CalcFormPropSet,** чтобы получить массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="41a9d-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="41a9d-128">**CalcFormPropSet** принимает пересечение или объединение наборов свойств этих форм в зависимости от флага, установленного в параметре  _ulFlags,_ и возвращает структуру **SMAPIFormPropArray,** которая содержит итоговую группу свойств.</span><span class="sxs-lookup"><span data-stu-id="41a9d-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="41a9d-129">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="41a9d-129">Notes to implementers</span></span>

<span data-ttu-id="41a9d-130">Если просмотр формы передает флаг MAPI_UNICODE в  _параметре ulFlags,_ все строки должны быть возвращены в виде строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="41a9d-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="41a9d-131">Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается.</span><span class="sxs-lookup"><span data-stu-id="41a9d-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41a9d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="41a9d-132">See also</span></span>



[<span data-ttu-id="41a9d-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="41a9d-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="41a9d-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41a9d-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

