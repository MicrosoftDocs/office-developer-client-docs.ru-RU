---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Последнее изменение: 20 февраля 2012 г.'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396213"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="f7bde-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="f7bde-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="f7bde-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7bde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7bde-105">Сравнение двух строк Юникод.</span><span class="sxs-lookup"><span data-stu-id="f7bde-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="f7bde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7bde-106">Parameters</span></span>

 <span data-ttu-id="f7bde-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="f7bde-107">_lcid_</span></span>
  
> <span data-ttu-id="f7bde-108">[in] Идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="f7bde-108">[in] Locale identifier.</span></span> <span data-ttu-id="f7bde-109">Параметр _Locale_ [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)подробные определения см.</span><span class="sxs-lookup"><span data-stu-id="f7bde-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="f7bde-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="f7bde-110">_dwFlags_</span></span>
  
> <span data-ttu-id="f7bde-111">[in] Флаги, следует ли игнорировать регистр и диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="f7bde-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="f7bde-112">Подробные определения в разделе параметр _dwCmpFlags_ [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7bde-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="f7bde-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="f7bde-113">_pstr1_</span></span>
  
> <span data-ttu-id="f7bde-114">[in] Указатель для первой строки Юникод для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f7bde-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="f7bde-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="f7bde-115">_cch1_</span></span>
  
> <span data-ttu-id="f7bde-116">[in] Длина в символах первой строки Юникод, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="f7bde-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="f7bde-117">Приложение может предоставлять отрицательным значением, если строка символом null.</span><span class="sxs-lookup"><span data-stu-id="f7bde-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="f7bde-118">В этом случае функция **MNLS_CompareStringW** определяет продолжительность автоматически.</span><span class="sxs-lookup"><span data-stu-id="f7bde-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="f7bde-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="f7bde-119">_pstr2_</span></span>
  
> <span data-ttu-id="f7bde-120">[in] Указатель на втором строку в кодировке Юникод для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f7bde-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="f7bde-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="f7bde-121">_cch2_</span></span>
  
> <span data-ttu-id="f7bde-122">[in] Длина в символах второй строки Юникод, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="f7bde-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="f7bde-123">Приложение может предоставлять отрицательным значением, если строка символом null.</span><span class="sxs-lookup"><span data-stu-id="f7bde-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="f7bde-124">В этом случае функция определяет продолжительность автоматически.</span><span class="sxs-lookup"><span data-stu-id="f7bde-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7bde-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7bde-125">Return value</span></span>

<span data-ttu-id="f7bde-126">Возвращает значения, описанного для [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7bde-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7bde-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7bde-127">Remarks</span></span>

<span data-ttu-id="f7bde-128">Эта функция является [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7bde-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="f7bde-129">**MNLS_CompareStringW** принимает те же параметры и имеет то же самое, что и [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7bde-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7bde-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f7bde-130">See also</span></span>



[<span data-ttu-id="f7bde-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="f7bde-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="f7bde-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="f7bde-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

