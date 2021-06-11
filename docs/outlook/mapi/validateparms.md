---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436807"
---
# <a name="validateparms"></a><span data-ttu-id="9fb09-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="9fb09-103">ValidateParms</span></span>

  
  
<span data-ttu-id="9fb09-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fb09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fb09-105">Вызывает внутреннюю функцию для проверки параметров, которые клиентские приложения передали поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="9fb09-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fb09-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9fb09-106">Header file:</span></span>  <br/> |<span data-ttu-id="9fb09-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="9fb09-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="9fb09-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9fb09-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9fb09-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9fb09-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9fb09-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9fb09-110">Called by:</span></span>  <br/> |<span data-ttu-id="9fb09-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9fb09-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="9fb09-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fb09-112">Parameters</span></span>

 <span data-ttu-id="9fb09-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="9fb09-113">_eMethod_</span></span>
  
> <span data-ttu-id="9fb09-114">[in] Указывает путем переумерия метод проверки.</span><span class="sxs-lookup"><span data-stu-id="9fb09-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="9fb09-115">_First_</span><span class="sxs-lookup"><span data-stu-id="9fb09-115">_First_</span></span>
  
> <span data-ttu-id="9fb09-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="9fb09-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9fb09-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9fb09-117">Return value</span></span>

<span data-ttu-id="9fb09-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9fb09-118">S_OK</span></span> 
  
> <span data-ttu-id="9fb09-119">Все параметры действительны.</span><span class="sxs-lookup"><span data-stu-id="9fb09-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="9fb09-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="9fb09-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="9fb09-121">Один или несколько параметров не допустимы.</span><span class="sxs-lookup"><span data-stu-id="9fb09-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9fb09-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="9fb09-122">Remarks</span></span>

<span data-ttu-id="9fb09-123">Параметры, переданные между MAPI и поставщиками услуг, считаются правильными и проходят проверку только отладки с помощью макроса [CheckParms.](checkparms.md)</span><span class="sxs-lookup"><span data-stu-id="9fb09-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="9fb09-124">Поставщики должны проверять все параметры, переданные в клиентских приложениях, но клиенты должны предполагать, что параметры MAPI и поставщика являются правильными.</span><span class="sxs-lookup"><span data-stu-id="9fb09-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="9fb09-125">Используйте **макрос HR_FAILED** для проверки значений возврата.</span><span class="sxs-lookup"><span data-stu-id="9fb09-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="9fb09-126">**ПроверкаParms** вызывается по-разному в зависимости от того, является ли код вызова C или C++.</span><span class="sxs-lookup"><span data-stu-id="9fb09-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="9fb09-127">C++ передает неявный  параметр, известный как этот, для каждого вызова метода, который становится явным в C и является адресом объекта.</span><span class="sxs-lookup"><span data-stu-id="9fb09-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="9fb09-128">Первый параметр  _eMethod_— это код, сделанный из проверяемого интерфейса и метода, и указывает, какие параметры следует найти в стеке.</span><span class="sxs-lookup"><span data-stu-id="9fb09-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="9fb09-129">Второй параметр отличается для C и C++.</span><span class="sxs-lookup"><span data-stu-id="9fb09-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="9fb09-130">В C++ он называется  _First_ и является первым параметром проверяемого метода.</span><span class="sxs-lookup"><span data-stu-id="9fb09-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="9fb09-131">Вторым параметром для языка C,  _ppThis,_ является адрес первого параметра методу, который всегда является указателем объекта.</span><span class="sxs-lookup"><span data-stu-id="9fb09-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="9fb09-132">В обоих случаях второй параметр дает адрес начала списка параметров метода и на основе  _eMethod_ перемещается вниз по стеку и проверяет параметры.</span><span class="sxs-lookup"><span data-stu-id="9fb09-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="9fb09-133">Поставщики, реализующие общие интерфейсы, такие как **IMAPITable** и **IMAPIProp,** всегда должны проверять параметры с помощью функции **ValidateParms,** чтобы убедиться в согласованности всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="9fb09-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="9fb09-134">Дополнительные функции проверки параметров были определены для некоторых сложных типов параметров, которые будут использоваться вместо этого по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9fb09-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="9fb09-135">См. справочные разделы для следующих функций:</span><span class="sxs-lookup"><span data-stu-id="9fb09-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="9fb09-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="9fb09-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="9fb09-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="9fb09-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="9fb09-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="9fb09-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="9fb09-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="9fb09-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="9fb09-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="9fb09-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="9fb09-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="9fb09-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="9fb09-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="9fb09-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="9fb09-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="9fb09-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="9fb09-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="9fb09-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="9fb09-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="9fb09-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="9fb09-146">Унаследованные методы используют ту же проверку параметров, что и интерфейс, от которого они наследуют.</span><span class="sxs-lookup"><span data-stu-id="9fb09-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="9fb09-147">Например, проверка параметров **для IMessage** и **IMAPIProp** должна быть одинаковой.</span><span class="sxs-lookup"><span data-stu-id="9fb09-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9fb09-148">См. также</span><span class="sxs-lookup"><span data-stu-id="9fb09-148">See also</span></span>



[<span data-ttu-id="9fb09-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="9fb09-149">UlValidateParms</span></span>](ulvalidateparms.md)

