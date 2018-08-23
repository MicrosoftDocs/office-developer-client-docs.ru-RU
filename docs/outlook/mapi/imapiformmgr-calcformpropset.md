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
ms.openlocfilehash: 5380b6541e609c17a9005c3390c6d5db06155306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567246"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="7568b-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="7568b-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="7568b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7568b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7568b-105">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="7568b-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="7568b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7568b-106">Parameters</span></span>

 <span data-ttu-id="7568b-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="7568b-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="7568b-108">[in] Указатель на массив объектов данные формы, чтобы указать форм, для которого возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="7568b-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="7568b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7568b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7568b-110">[in] Битовая маска флаги, который определяет, как возвращается массив свойства с помощью параметра _ppResults_ .</span><span class="sxs-lookup"><span data-stu-id="7568b-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="7568b-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="7568b-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="7568b-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="7568b-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="7568b-113">Возвращаемый массив содержит пересечение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="7568b-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="7568b-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="7568b-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="7568b-115">Возвращаемый массив содержит объединение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="7568b-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="7568b-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7568b-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7568b-117">Строки, возвращаемой в массиве являются в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="7568b-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="7568b-118">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="7568b-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7568b-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="7568b-119">_ppResults_</span></span>
  
> <span data-ttu-id="7568b-120">[out] Указатель на указатель на возвращенный [SMAPIFormPropArray](smapiformproparray.md) структуру, которая содержит свойства, используйте формы.</span><span class="sxs-lookup"><span data-stu-id="7568b-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7568b-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7568b-121">Return value</span></span>

<span data-ttu-id="7568b-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7568b-122">S_OK</span></span> 
  
> <span data-ttu-id="7568b-123">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="7568b-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="7568b-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7568b-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7568b-125">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="7568b-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7568b-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="7568b-126">Remarks</span></span>

<span data-ttu-id="7568b-127">Средства просмотра формы вызвать метод **IMAPIFormMgr::CalcFormPropSet** для получения массива свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="7568b-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="7568b-128">**CalcFormPropSet** принимает либо пересечения или объединение эти формы свойство задает, в зависимости от флаг в параметр _ulFlags_ и возвращает структуру **SMAPIFormPropArray** , содержащий итоговый группу свойства.</span><span class="sxs-lookup"><span data-stu-id="7568b-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7568b-129">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="7568b-129">Notes to implementers</span></span>

<span data-ttu-id="7568b-130">Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки должны возвращаться Юникод.</span><span class="sxs-lookup"><span data-stu-id="7568b-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="7568b-131">Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="7568b-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7568b-132">См. также</span><span class="sxs-lookup"><span data-stu-id="7568b-132">See also</span></span>



[<span data-ttu-id="7568b-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="7568b-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="7568b-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7568b-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

