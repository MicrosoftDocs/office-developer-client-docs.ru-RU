---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Дата последнего изменения: 20 февраля 2012 г.'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356849"
---
# <a name="mnls_comparestringw"></a><span data-ttu-id="8a9d9-103">MNLS_CompareStringW</span><span class="sxs-lookup"><span data-stu-id="8a9d9-103">MNLS_CompareStringW</span></span>

  
  
<span data-ttu-id="8a9d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a9d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a9d9-105">Сравнивает две строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a><span data-ttu-id="8a9d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a9d9-106">Parameters</span></span>

 <span data-ttu-id="8a9d9-107">_lcid_</span><span class="sxs-lookup"><span data-stu-id="8a9d9-107">_lcid_</span></span>
  
> <span data-ttu-id="8a9d9-108">возврата Идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-108">[in] Locale identifier.</span></span> <span data-ttu-id="8a9d9-109">Подробные сведения об определениях приведены в параметре _locale языка_ [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a9d9-109">For detailed definitions, see the  _Locale_ parameter of [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="8a9d9-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="8a9d9-110">_dwFlags_</span></span>
  
> <span data-ttu-id="8a9d9-111">возврата Флаги для игнорирования регистра и диакритических знаков.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-111">[in] Flags to ignore case and diacritics.</span></span> <span data-ttu-id="8a9d9-112">Подробные определения приведены в параметре _Двкмпфлагс_ [компарестринжекс](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a9d9-112">For detailed definitions, see the  _dwCmpFlags_ parameter of [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
    
 <span data-ttu-id="8a9d9-113">_pstr1_</span><span class="sxs-lookup"><span data-stu-id="8a9d9-113">_pstr1_</span></span>
  
> <span data-ttu-id="8a9d9-114">возврата Указатель на первую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-114">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="8a9d9-115">_cch1_</span><span class="sxs-lookup"><span data-stu-id="8a9d9-115">_cch1_</span></span>
  
> <span data-ttu-id="8a9d9-116">возврата Длина в символах первой строки Юникода за исключением завершающего знака null.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-116">[in] Length in characters of the first Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="8a9d9-117">Приложение может предоставить отрицательное значение, если строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-117">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="8a9d9-118">В этом случае функция **MNLS_CompareStringW** автоматически определяет длину.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-118">In this case, the **MNLS_CompareStringW** function determines the length automatically.</span></span> 
    
 <span data-ttu-id="8a9d9-119">_pstr2_</span><span class="sxs-lookup"><span data-stu-id="8a9d9-119">_pstr2_</span></span>
  
> <span data-ttu-id="8a9d9-120">возврата Указатель на вторую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-120">[in] Pointer to the second Unicode string to compare.</span></span>
    
 <span data-ttu-id="8a9d9-121">_cch2_</span><span class="sxs-lookup"><span data-stu-id="8a9d9-121">_cch2_</span></span>
  
> <span data-ttu-id="8a9d9-122">возврата Длина в символах второй строки Юникода, за исключением завершающего знака null.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-122">[in] Length in characters of the second Unicode string, excluding the terminating null character.</span></span> <span data-ttu-id="8a9d9-123">Приложение может предоставить отрицательное значение, если строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-123">The application can supply a negative value if the string is null-terminated.</span></span> <span data-ttu-id="8a9d9-124">В этом случае функция определяет длину автоматически.</span><span class="sxs-lookup"><span data-stu-id="8a9d9-124">In this case, the function determines the length automatically.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8a9d9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a9d9-125">Return value</span></span>

<span data-ttu-id="8a9d9-126">Возвращает значения, описанные для [компарестринжекс](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a9d9-126">Returns the values described for [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a9d9-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="8a9d9-127">Remarks</span></span>

<span data-ttu-id="8a9d9-128">Эта функция служит оболочкой для [компарестрингв](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a9d9-128">This function wraps [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span> <span data-ttu-id="8a9d9-129">**MNLS_CompareStringW** имеет те же параметры и имеет такое же поведение, что и [компарестрингв](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a9d9-129">**MNLS_CompareStringW** takes the same parameters and has the same behavior as [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8a9d9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="8a9d9-130">See also</span></span>



[<span data-ttu-id="8a9d9-131">компарестрингв</span><span class="sxs-lookup"><span data-stu-id="8a9d9-131">CompareStringW</span></span>](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[<span data-ttu-id="8a9d9-132">компарестринжекс</span><span class="sxs-lookup"><span data-stu-id="8a9d9-132">CompareStringEx</span></span>](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

