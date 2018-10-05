---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Последнее изменение: 18 июня 2012 г.'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386350"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="397a3-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="397a3-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="397a3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="397a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="397a3-105">Сравнение двух строк Юникод.</span><span class="sxs-lookup"><span data-stu-id="397a3-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="397a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="397a3-106">Parameters</span></span>

 <span data-ttu-id="397a3-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="397a3-107">_lpString1_</span></span>
  
> <span data-ttu-id="397a3-108">[in] Указатель для первой строки Юникод для сравнения.</span><span class="sxs-lookup"><span data-stu-id="397a3-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="397a3-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="397a3-109">_lpString2_</span></span>
  
> <span data-ttu-id="397a3-110">[in] Указатель на втором строку в кодировке Юникод для сравнения.</span><span class="sxs-lookup"><span data-stu-id="397a3-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="397a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="397a3-111">Return value</span></span>

<span data-ttu-id="397a3-112">Возвращает значения, описанного при вызове эквивалентный **MNLS_CompareStringW** за исключением CSTR_EQUAL.</span><span class="sxs-lookup"><span data-stu-id="397a3-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="397a3-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="397a3-113">Remarks</span></span>

 <span data-ttu-id="397a3-114">_MNLS_lstrcmpW_ выполняет сравнение путем вызова [MNLS_CompareStringW](mnls_comparestringw.md) с локальным GetUserDefaultLCID 0 для флаги и значение -1 для cch1 и cch2.</span><span class="sxs-lookup"><span data-stu-id="397a3-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="397a3-115">См. также</span><span class="sxs-lookup"><span data-stu-id="397a3-115">See also</span></span>



[<span data-ttu-id="397a3-116">GetUserDefaultLCID</span><span class="sxs-lookup"><span data-stu-id="397a3-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

