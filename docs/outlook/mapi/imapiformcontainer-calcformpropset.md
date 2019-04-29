---
title: Имапиформконтаинеркалкформпропсет
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
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414916"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="293b6-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="293b6-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="293b6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="293b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="293b6-105">Возвращает массив свойств, используемых всеми формами, установленными в контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="293b6-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="293b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="293b6-106">Parameters</span></span>

 <span data-ttu-id="293b6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="293b6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="293b6-108">возврата Битовая маска флагов, определяющих, как возвращается массив свойств в параметре _ппресултс_ .</span><span class="sxs-lookup"><span data-stu-id="293b6-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="293b6-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="293b6-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="293b6-110">ФОРМПРОПСЕТ_ИНТЕРСЕКТИОН</span><span class="sxs-lookup"><span data-stu-id="293b6-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="293b6-111">Возвращаемый массив содержит пересечение свойств формы.</span><span class="sxs-lookup"><span data-stu-id="293b6-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="293b6-112">ФОРМПРОПСЕТ_УНИОН</span><span class="sxs-lookup"><span data-stu-id="293b6-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="293b6-113">Возвращаемый массив содержит объединение свойств Forms.</span><span class="sxs-lookup"><span data-stu-id="293b6-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="293b6-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="293b6-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="293b6-115">Возвращаемые в массиве строки представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="293b6-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="293b6-116">Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="293b6-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="293b6-117">_Ппресултс_</span><span class="sxs-lookup"><span data-stu-id="293b6-117">_ppResults_</span></span>
  
> <span data-ttu-id="293b6-118">вышли Указатель на указатель на возвращаемую структуру [смапиформпропаррай](smapiformproparray.md) .</span><span class="sxs-lookup"><span data-stu-id="293b6-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="293b6-119">Эта структура содержит все свойства, используемые установленными формами.</span><span class="sxs-lookup"><span data-stu-id="293b6-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="293b6-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="293b6-120">Return value</span></span>

<span data-ttu-id="293b6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="293b6-121">S_OK</span></span> 
  
> <span data-ttu-id="293b6-122">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="293b6-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="293b6-123">МАПИ_Е_БАД_ЧАРВИДС</span><span class="sxs-lookup"><span data-stu-id="293b6-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="293b6-124">Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="293b6-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="293b6-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="293b6-125">Remarks</span></span>

<span data-ttu-id="293b6-126">Клиентские приложения вызывают метод **имапиформконтаинер:: калкформпропсет** для получения массива свойств, используемых всеми формами, установленными в контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="293b6-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="293b6-127">**Имапиформконтаинер:: калкформпропсет** работает аналогично методу [Имапиформмгр:: калкформпропсет](imapiformmgr-calcformpropset.md) , за исключением того, что он работает с каждой формой, зарегистрированной в определенном контейнере.</span><span class="sxs-lookup"><span data-stu-id="293b6-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="293b6-128">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="293b6-128">Notes to implementers</span></span>

<span data-ttu-id="293b6-129">Поставщики библиотеки форм, не поддерживающие строки Юникода, должны возвращать МАПИ_Е_БАД_ЧАРВИДС, если МАПИ_УНИКОДЕ передается.</span><span class="sxs-lookup"><span data-stu-id="293b6-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="293b6-130">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="293b6-130">Notes to callers</span></span>

 <span data-ttu-id="293b6-131">**Имапиформконтаинер:: калкформпропсет** принимает либо пересечение, либо объединение наборов свойств формы, в зависимости от флага, установленного в параметре _ulFlags_ , и возвращает структуру **смапиформпропаррай** , содержащую Результирующая группа свойств.</span><span class="sxs-lookup"><span data-stu-id="293b6-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="293b6-132">Если клиент передает флаг МАПИ_УНИКОДЕ в _ulFlags_, все возвращенные строки кодируются в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="293b6-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="293b6-133">См. также</span><span class="sxs-lookup"><span data-stu-id="293b6-133">See also</span></span>



[<span data-ttu-id="293b6-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="293b6-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="293b6-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="293b6-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="293b6-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="293b6-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

