---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356849"
---
# <a name="mnls_comparestringw"></a><span data-ttu-id="306a9-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="306a9-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="306a9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="306a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="306a9-105">Сравнивает две строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="306a9-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="306a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="306a9-106">Parameters</span></span>

 <span data-ttu-id="306a9-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="306a9-107">_lcid_</span></span>
  
> <span data-ttu-id="306a9-108">[in] Идентификатор locale.</span><span class="sxs-lookup"><span data-stu-id="306a9-108">[in] Locale identifier.</span></span> <span data-ttu-id="306a9-109">Подробные определения см. в _параметре Locale_ [compareString.](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="306a9-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="306a9-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="306a9-110">_dwFlags_</span></span>
  
> <span data-ttu-id="306a9-111">[in] Флаги для игнорирования диакритических и диакритических диакритических диакритических пометок.</span><span class="sxs-lookup"><span data-stu-id="306a9-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="306a9-112">Подробные определения см. в параметре _dwCmpFlags_ [compareStringEx.](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="306a9-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="306a9-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="306a9-113">_pstr1_</span></span>
  
> <span data-ttu-id="306a9-114">[in] Указатель на первую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="306a9-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="306a9-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="306a9-115">_cch1_</span></span>
  
> <span data-ttu-id="306a9-116">[in] Длина символов первой строки Юникода, за исключением завершающих символов null.</span><span class="sxs-lookup"><span data-stu-id="306a9-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="306a9-117">Приложение может предоставить отрицательное значение, если строка о конце null.</span><span class="sxs-lookup"><span data-stu-id="306a9-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="306a9-118">В этом случае **MNLS_CompareStringW** определяет длину автоматически.</span><span class="sxs-lookup"><span data-stu-id="306a9-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="306a9-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="306a9-119">_pstr2_</span></span>
  
> <span data-ttu-id="306a9-120">[in] Указатель на вторую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="306a9-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="306a9-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="306a9-121">_cch2_</span></span>
  
> <span data-ttu-id="306a9-122">[in] Длина символов второй строки Юникода, за исключением завершающих символов null.</span><span class="sxs-lookup"><span data-stu-id="306a9-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="306a9-123">Приложение может предоставить отрицательное значение, если строка о конце null.</span><span class="sxs-lookup"><span data-stu-id="306a9-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="306a9-124">В этом случае функция определяет длину автоматически.</span><span class="sxs-lookup"><span data-stu-id="306a9-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="306a9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="306a9-125">Return value</span></span>

<span data-ttu-id="306a9-126">Возвращает значения, описанные для [CompareStringEx.](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="306a9-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="306a9-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="306a9-127">Remarks</span></span>

<span data-ttu-id="306a9-128">Эта функция [обтекает compareStringW.](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="306a9-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="306a9-129">**MNLS_CompareStringW** принимает те же параметры и поведение, что [и CompareStringW.](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="306a9-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="306a9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="306a9-130">See also</span></span>



[<span data-ttu-id="306a9-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="306a9-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="306a9-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="306a9-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

