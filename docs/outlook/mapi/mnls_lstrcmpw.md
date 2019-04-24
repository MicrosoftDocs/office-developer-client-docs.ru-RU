---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Дата последнего изменения: 18 июня 2012 г.'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356842"
---
# <a name="mnlslstrcmpw"></a><span data-ttu-id="c001b-103">MNLS_lstrcmpW</span><span class="sxs-lookup"><span data-stu-id="c001b-103">MNLS_lstrcmpW</span></span>

 
  
<span data-ttu-id="c001b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c001b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c001b-105">Сравнивает две строки Юникода.</span><span class="sxs-lookup"><span data-stu-id="c001b-105">Compares two Unicode strings.</span></span>
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="c001b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c001b-106">Parameters</span></span>

 <span data-ttu-id="c001b-107">_lpString1_</span><span class="sxs-lookup"><span data-stu-id="c001b-107">_lpString1_</span></span>
  
> <span data-ttu-id="c001b-108">возврата Указатель на первую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c001b-108">[in] Pointer to the first Unicode string to compare.</span></span>
    
 <span data-ttu-id="c001b-109">_lpString2_</span><span class="sxs-lookup"><span data-stu-id="c001b-109">_lpString2_</span></span>
  
> <span data-ttu-id="c001b-110">возврата Указатель на вторую строку Юникода для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c001b-110">[in] Pointer to the second Unicode string to compare.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c001b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c001b-111">Return value</span></span>

<span data-ttu-id="c001b-112">Возвращает значения, описанные для эквивалентного вызова **мнлс_компарестрингв** , за исключением кстр_екуал.</span><span class="sxs-lookup"><span data-stu-id="c001b-112">Returns the values described for an equivalent call to **MNLS_CompareStringW** except for CSTR_EQUAL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c001b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c001b-113">Remarks</span></span>

 <span data-ttu-id="c001b-114">_Мнлс_лстркмпв_ выполняет сравнение, вызывая [мнлс_компарестрингв](mnls_comparestringw.md) с языковым стандартом жетусердефаултлЦид, 0 для флагов и – 1 для cch1 и cch2.</span><span class="sxs-lookup"><span data-stu-id="c001b-114">_MNLS_lstrcmpW_ performs a comparison by calling [MNLS_CompareStringW](mnls_comparestringw.md) with a locale of GetUserDefaultLCID, 0 for flags, and -1 for cch1 and cch2.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c001b-115">См. также</span><span class="sxs-lookup"><span data-stu-id="c001b-115">See also</span></span>



[<span data-ttu-id="c001b-116">ЖетусердефаултлЦид</span><span class="sxs-lookup"><span data-stu-id="c001b-116">GetUserDefaultLCID</span></span>](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

