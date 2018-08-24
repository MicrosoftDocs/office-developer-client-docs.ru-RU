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
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589569"
---
# <a name="mnlsisbadstringptrw"></a><span data-ttu-id="f383c-103">MNLS_IsBadStringPtrW</span><span class="sxs-lookup"><span data-stu-id="f383c-103">MNLS_IsBadStringPtrW</span></span>

  
  
<span data-ttu-id="f383c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f383c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f383c-105">Проверяет, что указатель на строку широкий действительна.</span><span class="sxs-lookup"><span data-stu-id="f383c-105">Verifies that a pointer to a wide string is valid.</span></span>
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a><span data-ttu-id="f383c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f383c-106">Parameters</span></span>

 <span data-ttu-id="f383c-107">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="f383c-107">_lpsz_</span></span>
  
> <span data-ttu-id="f383c-108">[in] Указатель на строку расширенных символов.</span><span class="sxs-lookup"><span data-stu-id="f383c-108">[in] A pointer to the wide character string.</span></span>
    
 <span data-ttu-id="f383c-109">_ucchMax_</span><span class="sxs-lookup"><span data-stu-id="f383c-109">_ucchMax_</span></span>
  
> <span data-ttu-id="f383c-110">[in] Максимальная длина строки в символы, включая конца строки.</span><span class="sxs-lookup"><span data-stu-id="f383c-110">[in] The maximum length of the string in characters including terminator.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f383c-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f383c-111">Return value</span></span>

<span data-ttu-id="f383c-112">Возвращает логическое значение true, если строка неисправно.</span><span class="sxs-lookup"><span data-stu-id="f383c-112">Returns a Boolean that is true if the string is bad.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f383c-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="f383c-113">Remarks</span></span>

<span data-ttu-id="f383c-114">Эта функция является [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f383c-114">This function wraps [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span> <span data-ttu-id="f383c-115">Для получения дополнительных сведений см [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f383c-115">For more information, see [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).</span></span>
  

