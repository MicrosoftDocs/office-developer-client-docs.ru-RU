---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b15dc4e467644c2a0c3856372b550c3b55469f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808897"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="4a68f-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="4a68f-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="4a68f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a68f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a68f-105">Возвращает массив свойств, используемых все формы, установленные в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="4a68f-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="4a68f-106">���������</span><span class="sxs-lookup"><span data-stu-id="4a68f-106">Parameters</span></span>

 <span data-ttu-id="4a68f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4a68f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4a68f-108">[in] Битовая маска флаги, который определяет, как возвращается массив свойства с помощью параметра _ppResults_ .</span><span class="sxs-lookup"><span data-stu-id="4a68f-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="4a68f-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="4a68f-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="4a68f-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="4a68f-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="4a68f-111">Возвращаемый массив содержит пересечение свойства форм.</span><span class="sxs-lookup"><span data-stu-id="4a68f-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="4a68f-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="4a68f-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="4a68f-113">Возвращаемый массив содержит объединение форм свойства.</span><span class="sxs-lookup"><span data-stu-id="4a68f-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="4a68f-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a68f-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4a68f-115">Строки, возвращаемой в массиве являются в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="4a68f-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="4a68f-116">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="4a68f-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="4a68f-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="4a68f-117">_ppResults_</span></span>
  
> <span data-ttu-id="4a68f-118">[out] Указатель на указатель на структуру возвращенные [SMAPIFormPropArray](smapiformproparray.md) .</span><span class="sxs-lookup"><span data-stu-id="4a68f-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="4a68f-119">Эта структура содержит все свойства, используемые с установленным формам.</span><span class="sxs-lookup"><span data-stu-id="4a68f-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4a68f-120">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4a68f-120">Return value</span></span>

<span data-ttu-id="4a68f-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="4a68f-121">S_OK</span></span> 
  
> <span data-ttu-id="4a68f-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4a68f-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="4a68f-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4a68f-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4a68f-124">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="4a68f-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4a68f-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="4a68f-125">Remarks</span></span>

<span data-ttu-id="4a68f-126">Клиентские приложения вызовите метод **IMAPIFormContainer::CalcFormPropSet** для получения массива свойства, используемые все формы, установленные в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="4a68f-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="4a68f-127">**IMAPIFormContainer::CalcFormPropSet** работает как метод [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , за исключением того, что он работает в каждую форму, зарегистрированные в конкретным контейнером.</span><span class="sxs-lookup"><span data-stu-id="4a68f-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4a68f-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="4a68f-128">Notes to implementers</span></span>

<span data-ttu-id="4a68f-129">Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4a68f-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4a68f-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4a68f-130">Notes to callers</span></span>

 <span data-ttu-id="4a68f-131">**IMAPIFormContainer::CalcFormPropSet** принимает пересечения или объединение наборов свойств форм, в зависимости от флаг в параметре _ulFlags_ и возвращает структуру **SMAPIFormPropArray** , которая содержит Итоговый группа свойств.</span><span class="sxs-lookup"><span data-stu-id="4a68f-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="4a68f-132">Если клиент передает флаг MAPI_UNICODE _ulFlags_, все возвращенные строки содержат Юникод.</span><span class="sxs-lookup"><span data-stu-id="4a68f-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a68f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="4a68f-133">See also</span></span>



[<span data-ttu-id="4a68f-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="4a68f-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="4a68f-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="4a68f-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="4a68f-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a68f-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

