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
ms.openlocfilehash: dd7d310c8e801ba1246a0ce948aced9fa6a1a8af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810028"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="d5c04-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="d5c04-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="d5c04-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5c04-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5c04-105">Проверяет, что указатель на строку широкий действительна.</span><span class="sxs-lookup"><span data-stu-id="d5c04-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="d5c04-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5c04-106">Parameters</span></span>

 <span data-ttu-id="d5c04-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="d5c04-107">_lpsz_</span></span>
  
> <span data-ttu-id="d5c04-108">[in] Указатель на строку расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="d5c04-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="d5c04-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="d5c04-109">_ucchMax_</span></span>
  
> <span data-ttu-id="d5c04-110">[in] Максимальная длина строки в символы, включая конца строки.</span><span class="sxs-lookup"><span data-stu-id="d5c04-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5c04-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d5c04-111">Return value</span></span>

<span data-ttu-id="d5c04-112">Возвращает логическое значение true, если строка неисправно.</span><span class="sxs-lookup"><span data-stu-id="d5c04-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5c04-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="d5c04-113">Remarks</span></span>

<span data-ttu-id="d5c04-114">Эта функция является [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5c04-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="d5c04-115">Для получения дополнительных сведений см [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5c04-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

