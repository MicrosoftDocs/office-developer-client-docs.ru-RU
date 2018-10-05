---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Последнее изменение: 21 февраля 2012 г.'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392090"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="2dd7f-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="2dd7f-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="2dd7f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dd7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dd7f-105">Определяет, длина указанной строки Юникод, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="2dd7f-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="2dd7f-106">Рекомендуется использовать [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2dd7f-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="2dd7f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dd7f-107">Parameters</span></span>

 <span data-ttu-id="2dd7f-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="2dd7f-108">_lpsz_</span></span>
  
> <span data-ttu-id="2dd7f-109">[in] Символом null строка Юникод для проверки.</span><span class="sxs-lookup"><span data-stu-id="2dd7f-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2dd7f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dd7f-110">Return value</span></span>

<span data-ttu-id="2dd7f-111">Функция возвращает целое число в длину строки.</span><span class="sxs-lookup"><span data-stu-id="2dd7f-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="2dd7f-112">Это число знаков в строке, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="2dd7f-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="2dd7f-113">Если _lpsz_ имеет значение NULL, функция возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2dd7f-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2dd7f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2dd7f-114">Remarks</span></span>

<span data-ttu-id="2dd7f-115">Эта функция имеет функцию **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="2dd7f-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="2dd7f-116">Для получения дополнительных сведений см [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2dd7f-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dd7f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="2dd7f-117">See also</span></span>



[<span data-ttu-id="2dd7f-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="2dd7f-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="2dd7f-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="2dd7f-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

