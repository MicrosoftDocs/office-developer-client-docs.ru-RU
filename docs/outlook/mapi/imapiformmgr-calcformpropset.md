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
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808916"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="5b000-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="5b000-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="5b000-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5b000-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5b000-105">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="5b000-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="5b000-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b000-106">Parameters</span></span>

 <span data-ttu-id="5b000-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="5b000-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="5b000-108">[in] Указатель на массив объектов данные формы, чтобы указать форм, для которого возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="5b000-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="5b000-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b000-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5b000-110">[in] Битовая маска флаги, который определяет, как возвращается массив свойства с помощью параметра _ppResults_ .</span><span class="sxs-lookup"><span data-stu-id="5b000-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="5b000-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="5b000-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="5b000-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="5b000-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="5b000-113">Возвращаемый массив содержит пересечение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="5b000-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="5b000-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="5b000-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="5b000-115">Возвращаемый массив содержит объединение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="5b000-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="5b000-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5b000-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5b000-117">Строки, возвращаемой в массиве являются в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="5b000-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="5b000-118">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5b000-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="5b000-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="5b000-119">_ppResults_</span></span>
  
> <span data-ttu-id="5b000-120">[out] Указатель на указатель на возвращенный [SMAPIFormPropArray](smapiformproparray.md) структуру, которая содержит свойства, используйте формы.</span><span class="sxs-lookup"><span data-stu-id="5b000-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5b000-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="5b000-121">Return value</span></span>

<span data-ttu-id="5b000-122">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="5b000-122">S_OK</span></span> 
  
> <span data-ttu-id="5b000-123">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="5b000-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="5b000-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5b000-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5b000-125">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="5b000-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b000-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="5b000-126">Remarks</span></span>

<span data-ttu-id="5b000-127">Средства просмотра формы вызвать метод **IMAPIFormMgr::CalcFormPropSet** для получения массива свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="5b000-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="5b000-128">**CalcFormPropSet** принимает либо пересечения или объединение эти формы свойство задает, в зависимости от флаг в параметр _ulFlags_ и возвращает структуру **SMAPIFormPropArray** , содержащий итоговый группу свойства.</span><span class="sxs-lookup"><span data-stu-id="5b000-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5b000-129">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="5b000-129">Notes to implementers</span></span>

<span data-ttu-id="5b000-130">Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки должны возвращаться Юникод.</span><span class="sxs-lookup"><span data-stu-id="5b000-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="5b000-131">Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="5b000-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b000-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5b000-132">See also</span></span>



[<span data-ttu-id="5b000-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="5b000-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="5b000-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b000-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

