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
# <a name="validateparms"></a><span data-ttu-id="b23f6-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="b23f6-103">ValidateParms</span></span>

  
  
<span data-ttu-id="b23f6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b23f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b23f6-105">Вызывает внутреннюю функцию для проверки параметров клиентские приложения, которые передаются поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="b23f6-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b23f6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b23f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="b23f6-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b23f6-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b23f6-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b23f6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b23f6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b23f6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b23f6-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b23f6-110">Called by:</span></span>  <br/> |<span data-ttu-id="b23f6-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b23f6-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="b23f6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b23f6-112">Parameters</span></span>

 <span data-ttu-id="b23f6-113">_емесод_</span><span class="sxs-lookup"><span data-stu-id="b23f6-113">_eMethod_</span></span>
  
> <span data-ttu-id="b23f6-114">возврата Определяет, по перечислению, метод, который необходимо проверить.</span><span class="sxs-lookup"><span data-stu-id="b23f6-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="b23f6-115">_First_</span><span class="sxs-lookup"><span data-stu-id="b23f6-115">_First_</span></span>
  
> <span data-ttu-id="b23f6-116">возврата Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="b23f6-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b23f6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b23f6-117">Return value</span></span>

<span data-ttu-id="b23f6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b23f6-118">S_OK</span></span> 
  
> <span data-ttu-id="b23f6-119">Все параметры являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="b23f6-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="b23f6-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b23f6-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b23f6-121">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="b23f6-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b23f6-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="b23f6-122">Remarks</span></span>

<span data-ttu-id="b23f6-123">Параметры, передаваемые между MAPI и поставщиками услуг, считаются верными и подвергнуты отладке только при проверке с помощью макроса [чеккпармс](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="b23f6-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="b23f6-124">Поставщики должны проверить все параметры, переданные клиентскими приложениями, но клиенты должны предполагать, что параметры MAPI и provider указаны правильно.</span><span class="sxs-lookup"><span data-stu-id="b23f6-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="b23f6-125">Используйте макрос **HR_FAILED** для проверки возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="b23f6-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="b23f6-126">**Валидатепармс** вызывается по-разному в зависимости от того, является ли вызывающий код кодом C или C++.</span><span class="sxs-lookup"><span data-stu-id="b23f6-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="b23f6-127">C++ передает неявный _параметр, известный для каждого_ вызова метода, который становится явным в C и является адресом объекта.</span><span class="sxs-lookup"><span data-stu-id="b23f6-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="b23f6-128">Первый параметр, _емесод_, представляет собой перечислитель из интерфейса и метода, которые проверяются, и сообщает, какие параметры должны быть найдены в стеке.</span><span class="sxs-lookup"><span data-stu-id="b23f6-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="b23f6-129">Второй параметр отличается для C и C++.</span><span class="sxs-lookup"><span data-stu-id="b23f6-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="b23f6-130">В C++ он вызывается _первым_, а является первым параметром проверяемого метода.</span><span class="sxs-lookup"><span data-stu-id="b23f6-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="b23f6-131">Второй параметр для языка C, _ппсис_, представляет собой адрес первого параметра метода, который всегда является указателем объекта.</span><span class="sxs-lookup"><span data-stu-id="b23f6-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="b23f6-132">В обоих случаях второй параметр задает адрес начала списка параметров метода и на основе _емесод_перемещает вниз по стеку и проверяет параметры.</span><span class="sxs-lookup"><span data-stu-id="b23f6-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="b23f6-133">Поставщики, реализующие общие интерфейсы, такие как **IMAPITable** и **IMAPIProp** , должны всегда проверять параметры с помощью функции **валидатепармс** , чтобы обеспечить согласованность всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b23f6-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="b23f6-134">Для некоторых сложных типов параметров были определены дополнительные функции проверки параметров, а не соответствующие типы.</span><span class="sxs-lookup"><span data-stu-id="b23f6-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="b23f6-135">В справочных материалах представлены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="b23f6-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="b23f6-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="b23f6-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="b23f6-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="b23f6-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="b23f6-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="b23f6-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="b23f6-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="b23f6-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="b23f6-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="b23f6-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="b23f6-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="b23f6-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="b23f6-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="b23f6-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="b23f6-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="b23f6-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="b23f6-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="b23f6-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="b23f6-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b23f6-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="b23f6-146">Унаследованные методы используют ту же проверку параметров, что и интерфейс, от которого они наследуются.</span><span class="sxs-lookup"><span data-stu-id="b23f6-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="b23f6-147">Например, проверка параметров для **iMessage** и **IMAPIProp** должна быть одинаковой.</span><span class="sxs-lookup"><span data-stu-id="b23f6-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b23f6-148">См. также</span><span class="sxs-lookup"><span data-stu-id="b23f6-148">See also</span></span>



[<span data-ttu-id="b23f6-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="b23f6-149">UlValidateParms</span></span>](ulvalidateparms.md)

