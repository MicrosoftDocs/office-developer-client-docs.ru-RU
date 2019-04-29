---
title: Имапиформмгркалкформпропсет
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
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="85e80-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="85e80-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="85e80-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85e80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85e80-105">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="85e80-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="85e80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85e80-106">Parameters</span></span>

 <span data-ttu-id="85e80-107">_пфрминфоаррай_</span><span class="sxs-lookup"><span data-stu-id="85e80-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="85e80-108">возврата Указатель на массив объектов данных формы, определяющий формы, для которых возвращаются свойства.</span><span class="sxs-lookup"><span data-stu-id="85e80-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="85e80-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="85e80-109">_ulFlags_</span></span>
  
> <span data-ttu-id="85e80-110">возврата Битовая маска флагов, определяющих, как возвращается массив свойств в параметре _ппресултс_ .</span><span class="sxs-lookup"><span data-stu-id="85e80-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="85e80-111">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="85e80-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="85e80-112">ФОРМПРОПСЕТ_ИНТЕРСЕКТИОН</span><span class="sxs-lookup"><span data-stu-id="85e80-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="85e80-113">Возвращаемый массив содержит пересечение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="85e80-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="85e80-114">ФОРМПРОПСЕТ_УНИОН</span><span class="sxs-lookup"><span data-stu-id="85e80-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="85e80-115">Возвращаемый массив содержит объединение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="85e80-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="85e80-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="85e80-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="85e80-117">Возвращаемые в массиве строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="85e80-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="85e80-118">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="85e80-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="85e80-119">_Ппресултс_</span><span class="sxs-lookup"><span data-stu-id="85e80-119">_ppResults_</span></span>
  
> <span data-ttu-id="85e80-120">вышли Указатель на указатель на возвращаемую структуру [смапиформпропаррай](smapiformproparray.md) , которая содержит свойства, используемые формами.</span><span class="sxs-lookup"><span data-stu-id="85e80-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85e80-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85e80-121">Return value</span></span>

<span data-ttu-id="85e80-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="85e80-122">S_OK</span></span> 
  
> <span data-ttu-id="85e80-123">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="85e80-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="85e80-124">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="85e80-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="85e80-125">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="85e80-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85e80-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="85e80-126">Remarks</span></span>

<span data-ttu-id="85e80-127">Средства просмотра форм вызывают метод **имапиформмгр:: калкформпропсет** , чтобы получить массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="85e80-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="85e80-128">**Калкформпропсет** принимает либо пересечение, либо объединение наборов свойств этих форм, в зависимости от флага, установленного в параметре _ulFlags_ , и возвращает структуру **смапиформпропаррай** , содержащую результирующую группу параметры.</span><span class="sxs-lookup"><span data-stu-id="85e80-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="85e80-129">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="85e80-129">Notes to implementers</span></span>

<span data-ttu-id="85e80-130">Если средство просмотра формы передает флаг МАПИ_УНИКОДЕ в параметре _ulFlags_ , все строки должны быть возвращены в виде строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="85e80-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="85e80-131">Поставщики библиотеки форм, не поддерживающие строки Юникода, должны возвращать МАПИ_Е_БАД_ЧАРВИДС, если МАПИ_УНИКОДЕ передается.</span><span class="sxs-lookup"><span data-stu-id="85e80-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85e80-132">См. также</span><span class="sxs-lookup"><span data-stu-id="85e80-132">See also</span></span>



[<span data-ttu-id="85e80-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="85e80-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="85e80-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85e80-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

