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
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810019"
---
# <a name="mnlscomparestringw"></a><span data-ttu-id="a7b03-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="a7b03-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="a7b03-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7b03-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7b03-105">Сравнение двух строк Юникод.</span><span class="sxs-lookup"><span data-stu-id="a7b03-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="a7b03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7b03-106">Parameters</span></span>

 <span data-ttu-id="a7b03-107">_код языка_</span><span class="sxs-lookup"><span data-stu-id="a7b03-107">_lcid_</span></span>
  
> <span data-ttu-id="a7b03-108">[in] Идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="a7b03-108">[in] Locale identifier.</span></span> <span data-ttu-id="a7b03-109">Параметр _Locale_ [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)подробные определения см.</span><span class="sxs-lookup"><span data-stu-id="a7b03-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="a7b03-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="a7b03-110">_dwFlags_</span></span>
  
> <span data-ttu-id="a7b03-111">[in] Флаги, следует ли игнорировать регистр и диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="a7b03-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="a7b03-112">Подробные определения в разделе параметр _dwCmpFlags_ [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7b03-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="a7b03-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="a7b03-113">_pstr1_</span></span>
  
> <span data-ttu-id="a7b03-114">[in] Указатель для первой строки Юникод для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a7b03-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="a7b03-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="a7b03-115">_cch1_</span></span>
  
> <span data-ttu-id="a7b03-116">[in] Длина в символах первой строки Юникод, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="a7b03-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="a7b03-117">Приложение может предоставлять отрицательным значением, если строка символом null.</span><span class="sxs-lookup"><span data-stu-id="a7b03-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="a7b03-118">В этом случае функция **MNLS_CompareStringW** определяет продолжительность автоматически.</span><span class="sxs-lookup"><span data-stu-id="a7b03-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="a7b03-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="a7b03-119">_pstr2_</span></span>
  
> <span data-ttu-id="a7b03-120">[in] Указатель на втором строку в кодировке Юникод для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a7b03-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="a7b03-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="a7b03-121">_cch2_</span></span>
  
> <span data-ttu-id="a7b03-122">[in] Длина в символах второй строки Юникод, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="a7b03-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="a7b03-123">Приложение может предоставлять отрицательным значением, если строка символом null.</span><span class="sxs-lookup"><span data-stu-id="a7b03-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="a7b03-124">В этом случае функция определяет продолжительность автоматически.</span><span class="sxs-lookup"><span data-stu-id="a7b03-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7b03-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a7b03-125">Return value</span></span>

<span data-ttu-id="a7b03-126">Возвращает значения, описанного для [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7b03-126">Returns the values described for [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a7b03-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7b03-127">Remarks</span></span>

<span data-ttu-id="a7b03-128">Эта функция является [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7b03-128">This function wraps [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="a7b03-129">**MNLS_CompareStringW** принимает те же параметры и имеет то же самое, что и [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7b03-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a7b03-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a7b03-130">See also</span></span>



[<span data-ttu-id="a7b03-131">CompareStringW</span><span class="sxs-lookup"><span data-stu-id="a7b03-131">CompareStringW</span></span>](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="a7b03-132">CompareStringEx</span><span class="sxs-lookup"><span data-stu-id="a7b03-132">CompareStringEx</span></span>](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

