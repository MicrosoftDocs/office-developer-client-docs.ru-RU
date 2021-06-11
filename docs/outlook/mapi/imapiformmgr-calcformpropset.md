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
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="fe04e-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="fe04e-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="fe04e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe04e-105">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="fe04e-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="fe04e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe04e-106">Parameters</span></span>

 <span data-ttu-id="fe04e-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="fe04e-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="fe04e-108">[in] Указатель на массив объектов информации о формах, которые определяют формы, для которых нужно возвращать свойства.</span><span class="sxs-lookup"><span data-stu-id="fe04e-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="fe04e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fe04e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="fe04e-110">[in] Битмашка флагов, которая управляет тем, как возвращается массив свойств в параметре _ppResults._</span><span class="sxs-lookup"><span data-stu-id="fe04e-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="fe04e-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="fe04e-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="fe04e-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="fe04e-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="fe04e-113">Возвращенный массив содержит пересечение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="fe04e-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="fe04e-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="fe04e-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="fe04e-115">Возвращенный массив содержит объединение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="fe04e-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="fe04e-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fe04e-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="fe04e-117">Строки, возвращенные в массиве, находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="fe04e-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="fe04e-118">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="fe04e-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="fe04e-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="fe04e-119">_ppResults_</span></span>
  
> <span data-ttu-id="fe04e-120">[вышел] Указатель на указатель на возвращенную [структуру SMAPIFormPropArray,](smapiformproparray.md) которая содержит свойства, которые используются формами.</span><span class="sxs-lookup"><span data-stu-id="fe04e-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe04e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe04e-121">Return value</span></span>

<span data-ttu-id="fe04e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe04e-122">S_OK</span></span> 
  
> <span data-ttu-id="fe04e-123">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="fe04e-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="fe04e-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="fe04e-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="fe04e-125">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="fe04e-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe04e-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe04e-126">Remarks</span></span>

<span data-ttu-id="fe04e-127">Зрители форм называют **метод IMAPIFormMgr::CalcFormPropSet** для получения массива свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="fe04e-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="fe04e-128">**CalcFormPropSet** принимает пересечение или объединение наборов свойств этих форм в зависимости от флага, заданного в параметре  _ulFlags,_ и возвращает структуру **SMAPIFormPropArray,** содержаную в результате группу свойств.</span><span class="sxs-lookup"><span data-stu-id="fe04e-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="fe04e-129">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="fe04e-129">Notes to implementers</span></span>

<span data-ttu-id="fe04e-130">Если зритель формы передает флаг MAPI_UNICODE в параметре  _ulFlags,_ все строки должны быть возвращены в виде строк Юникод.</span><span class="sxs-lookup"><span data-stu-id="fe04e-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="fe04e-131">Поставщики библиотек форм, которые не поддерживают строки Юникод, должны MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE будет пройдена.</span><span class="sxs-lookup"><span data-stu-id="fe04e-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fe04e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="fe04e-132">See also</span></span>



[<span data-ttu-id="fe04e-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="fe04e-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="fe04e-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe04e-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

