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
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579720"
---
# <a name="validateparms"></a><span data-ttu-id="f85b2-103">ValidateParms</span><span class="sxs-lookup"><span data-stu-id="f85b2-103">ValidateParms</span></span>

  
  
<span data-ttu-id="f85b2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f85b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f85b2-105">Вызывает функцию внутреннего и проверять параметры клиентских приложений не имеет разрешений для поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="f85b2-105">Calls an internal function to check the parameters client applications have passed to service providers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f85b2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f85b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="f85b2-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="f85b2-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="f85b2-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="f85b2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f85b2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f85b2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f85b2-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="f85b2-110">Called by:</span></span>  <br/> |<span data-ttu-id="f85b2-111">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="f85b2-111">Service providers</span></span>  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a><span data-ttu-id="f85b2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f85b2-112">Parameters</span></span>

 <span data-ttu-id="f85b2-113">_eMethod_</span><span class="sxs-lookup"><span data-stu-id="f85b2-113">_eMethod_</span></span>
  
> <span data-ttu-id="f85b2-114">[in] Указывает перечисление, метод для проверки.</span><span class="sxs-lookup"><span data-stu-id="f85b2-114">[in] Specifies, by enumeration, the method to validate.</span></span> 
    
 <span data-ttu-id="f85b2-115">_Первый_</span><span class="sxs-lookup"><span data-stu-id="f85b2-115">_First_</span></span>
  
> <span data-ttu-id="f85b2-116">[in] Указатель на первый аргумент в стеке.</span><span class="sxs-lookup"><span data-stu-id="f85b2-116">[in] Pointer to the first argument on the stack.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f85b2-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f85b2-117">Return value</span></span>

<span data-ttu-id="f85b2-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f85b2-118">S_OK</span></span> 
  
> <span data-ttu-id="f85b2-119">Все параметры являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="f85b2-119">All of the parameters are valid.</span></span> 
    
<span data-ttu-id="f85b2-120">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f85b2-120">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f85b2-121">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="f85b2-121">One or more of the parameters are not valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f85b2-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="f85b2-122">Remarks</span></span>

<span data-ttu-id="f85b2-123">Параметры, переданные между MAPI и службой поставщиков предполагается, что правильно и подвергаются только проверки отладка с помощью макроса [CheckParms](checkparms.md) .</span><span class="sxs-lookup"><span data-stu-id="f85b2-123">Parameters passed between MAPI and service providers are assumed to be correct and undergo only debug validation with the [CheckParms](checkparms.md) macro.</span></span> <span data-ttu-id="f85b2-124">Поставщики должен проверить, все параметры, переданные в клиентских приложениях, но клиенты должны предполагается правильность параметров и MAPI.</span><span class="sxs-lookup"><span data-stu-id="f85b2-124">Providers should check all parameters passed in by client applications, but clients should assume that MAPI and provider parameters are correct.</span></span> <span data-ttu-id="f85b2-125">Использование макроса **HR_FAILED** для проверки возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f85b2-125">Use the **HR_FAILED** macro to test return values.</span></span> 
  
 <span data-ttu-id="f85b2-126">**ValidateParms** называется по-разному в зависимости от того, является ли вызывающий кода C или C++.</span><span class="sxs-lookup"><span data-stu-id="f85b2-126">**ValidateParms** is called differently depending on whether the calling code is C or C++.</span></span> <span data-ttu-id="f85b2-127">C++ передает неявный параметр известных как _это_ для каждого вызова метода, который становится явные в C и представляет собой адрес объекта.</span><span class="sxs-lookup"><span data-stu-id="f85b2-127">C++ passes an implicit parameter known as  _this_ to each method call, which becomes explicit in C and is the address of the object.</span></span> <span data-ttu-id="f85b2-128">Первый параметр _eMethod_является перечислителя из интерфейса и метод проверки и сообщает о том, какие параметры следует ожидать для поиска в стеке.</span><span class="sxs-lookup"><span data-stu-id="f85b2-128">The first parameter,  _eMethod_, is an enumerator made from the interface and method being validated and tells what parameters to expect to find on the stack.</span></span> <span data-ttu-id="f85b2-129">Второй параметр – C и C++ различные.</span><span class="sxs-lookup"><span data-stu-id="f85b2-129">The second parameter is different for C and C++.</span></span> <span data-ttu-id="f85b2-130">В C++ он вызывает _первый_и является первым параметром в метод при проверке.</span><span class="sxs-lookup"><span data-stu-id="f85b2-130">In C++ it is called  _First_, and it is the first parameter to the method being validated.</span></span> <span data-ttu-id="f85b2-131">Второй параметр для языка C, _ppThis_представляет собой адрес первого параметра в метод, который всегда указателя на объект.</span><span class="sxs-lookup"><span data-stu-id="f85b2-131">The second parameter for the C language,  _ppThis_, is the address of the first parameter to the method which is always an object pointer.</span></span> <span data-ttu-id="f85b2-132">В обоих случаях второй параметр содержит адрес в начало списка параметров метода и на основе _eMethod_, перемещает вниз стека и проверяет параметры.</span><span class="sxs-lookup"><span data-stu-id="f85b2-132">In both cases, the second parameter gives the address of the beginning of the method's parameter list, and based on  _eMethod_, moves down the stack and validates the parameters.</span></span> 
  
<span data-ttu-id="f85b2-133">Поставщики, реализующие общие интерфейсы, такие как **IMAPITable** и **IMAPIProp** всегда следует выполнять проверку параметров с помощью функции **ValidateParms** , чтобы сделать что согласованность между всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f85b2-133">Providers implementing common interfaces such as **IMAPITable** and **IMAPIProp** should always check parameters using the **ValidateParms** function in order to make sure consistency across all providers.</span></span> <span data-ttu-id="f85b2-134">Функции проверки дополнительный параметр были определены для некоторых сложных типов параметров для использования вместо соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="f85b2-134">Additional parameter validation functions have been defined for some complex parameter types to be used instead as appropriate.</span></span> <span data-ttu-id="f85b2-135">Можно найти ссылки на разделы для следующих функций:</span><span class="sxs-lookup"><span data-stu-id="f85b2-135">See the reference topics for the following functions:</span></span> 
  
- [<span data-ttu-id="f85b2-136">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="f85b2-136">FBadColumnSet</span></span>](fbadcolumnset.md)
    
- [<span data-ttu-id="f85b2-137">FBadEntryList</span><span class="sxs-lookup"><span data-stu-id="f85b2-137">FBadEntryList</span></span>](fbadentrylist.md)
    
- [<span data-ttu-id="f85b2-138">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f85b2-138">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="f85b2-139">FBadProp</span><span class="sxs-lookup"><span data-stu-id="f85b2-139">FBadProp</span></span>](fbadprop.md)
    
- [<span data-ttu-id="f85b2-140">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="f85b2-140">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="f85b2-141">FBadRestriction</span><span class="sxs-lookup"><span data-stu-id="f85b2-141">FBadRestriction</span></span>](fbadrestriction.md)
    
- [<span data-ttu-id="f85b2-142">FBadRglpszW</span><span class="sxs-lookup"><span data-stu-id="f85b2-142">FBadRglpszW</span></span>](fbadrglpszw.md)
    
- [<span data-ttu-id="f85b2-143">FBadRow</span><span class="sxs-lookup"><span data-stu-id="f85b2-143">FBadRow</span></span>](fbadrow.md)
    
- [<span data-ttu-id="f85b2-144">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="f85b2-144">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="f85b2-145">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f85b2-145">FBadSortOrderSet</span></span>](fbadsortorderset.md)
    
<span data-ttu-id="f85b2-146">Унаследованные методы используйте одинаковые параметр проверки как интерфейс, от которого они унаследованы.</span><span class="sxs-lookup"><span data-stu-id="f85b2-146">Inherited methods use the same parameter validation as the interface from which they inherit.</span></span> <span data-ttu-id="f85b2-147">Например проверка параметров для **IMessage** и **IMAPIProp** должно совпадать.</span><span class="sxs-lookup"><span data-stu-id="f85b2-147">For example, the parameter checking for **IMessage** and **IMAPIProp** should be the same.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f85b2-148">См. также</span><span class="sxs-lookup"><span data-stu-id="f85b2-148">See also</span></span>



[<span data-ttu-id="f85b2-149">UlValidateParms</span><span class="sxs-lookup"><span data-stu-id="f85b2-149">UlValidateParms</span></span>](ulvalidateparms.md)

