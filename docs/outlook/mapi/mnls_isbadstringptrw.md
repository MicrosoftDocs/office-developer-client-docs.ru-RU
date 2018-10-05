---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Последнее изменение: 20 февраля 2012 г.'
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398740"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="a0ced-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="a0ced-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="a0ced-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0ced-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0ced-105">Проверяет, что указатель на строку широкий действительна.</span><span class="sxs-lookup"><span data-stu-id="a0ced-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="a0ced-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0ced-106">Parameters</span></span>

 <span data-ttu-id="a0ced-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a0ced-107">_lpsz_</span></span>
  
> <span data-ttu-id="a0ced-108">[in] Указатель на строку расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="a0ced-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="a0ced-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="a0ced-109">_ucchMax_</span></span>
  
> <span data-ttu-id="a0ced-110">[in] Максимальная длина строки в символы, включая конца строки.</span><span class="sxs-lookup"><span data-stu-id="a0ced-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0ced-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0ced-111">Return value</span></span>

<span data-ttu-id="a0ced-112">Возвращает логическое значение true, если строка неисправно.</span><span class="sxs-lookup"><span data-stu-id="a0ced-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0ced-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0ced-113">Remarks</span></span>

<span data-ttu-id="a0ced-114">Эта функция является [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0ced-114">This function wraps [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="a0ced-115">Для получения дополнительных сведений см [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0ced-115">For more information, see [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).</span></span>
  

