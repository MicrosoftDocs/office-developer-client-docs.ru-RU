---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356856"
---
# <a name="mnls_isbadstringptrw"></a><span data-ttu-id="c51f2-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="c51f2-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="c51f2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c51f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c51f2-105">Проверяет, является ли указатель на широкую строку допустимым.</span><span class="sxs-lookup"><span data-stu-id="c51f2-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="c51f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c51f2-106">Parameters</span></span>

 <span data-ttu-id="c51f2-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="c51f2-107">_lpsz_</span></span>
  
> <span data-ttu-id="c51f2-108">[in] Указатель на широкую строку символов.</span><span class="sxs-lookup"><span data-stu-id="c51f2-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="c51f2-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="c51f2-109">_ucchMax_</span></span>
  
> <span data-ttu-id="c51f2-110">[in] Максимальная длина строки в символах, включая терминатор.</span><span class="sxs-lookup"><span data-stu-id="c51f2-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c51f2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c51f2-111">Return value</span></span>

<span data-ttu-id="c51f2-112">Возвращает boolean, который имеет true, если строка является плохой.</span><span class="sxs-lookup"><span data-stu-id="c51f2-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c51f2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c51f2-113">Remarks</span></span>

<span data-ttu-id="c51f2-114">Эта функция [обтекает isBadStringPtr.](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c51f2-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="c51f2-115">Дополнительные сведения см. в [isBadStringPtr.](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c51f2-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

