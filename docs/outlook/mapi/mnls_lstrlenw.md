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
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810051"
---
# <a name="mnlslstrlenw"></a><span data-ttu-id="8acbd-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="8acbd-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="8acbd-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8acbd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8acbd-105">Определяет, длина указанной строки Юникод, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="8acbd-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="8acbd-106">Рекомендуется использовать [StringCchLength](http://msdn.microsoft.com/ru-ru/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8acbd-106">Consider using [StringCchLength](http://msdn.microsoft.com/ru-ru/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="8acbd-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8acbd-107">Parameters</span></span>

 <span data-ttu-id="8acbd-108">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="8acbd-108">_lpsz_</span></span>
  
> <span data-ttu-id="8acbd-109">[in] Символом null строка Юникод для проверки.</span><span class="sxs-lookup"><span data-stu-id="8acbd-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8acbd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="8acbd-111">Функция возвращает целое число в длину строки.</span><span class="sxs-lookup"><span data-stu-id="8acbd-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="8acbd-112">Это число знаков в строке, за исключением конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="8acbd-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="8acbd-113">Если _lpsz_ имеет значение NULL, функция возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="8acbd-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8acbd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8acbd-114">Remarks</span></span>

<span data-ttu-id="8acbd-115">Эта функция имеет функцию **lstrlen** .</span><span class="sxs-lookup"><span data-stu-id="8acbd-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="8acbd-116">Для получения дополнительных сведений см [lstrlen](http://msdn.microsoft.com/ru-ru/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8acbd-116">For more information, see [lstrlen](http://msdn.microsoft.com/ru-ru/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8acbd-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8acbd-117">See also</span></span>



[<span data-ttu-id="8acbd-118">lstrlen</span><span class="sxs-lookup"><span data-stu-id="8acbd-118">lstrlen</span></span>](http://msdn.microsoft.com/ru-ru/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="8acbd-119">StringCchLength</span><span class="sxs-lookup"><span data-stu-id="8acbd-119">StringCchLength</span></span>](http://msdn.microsoft.com/ru-ru/library/ms647539%28VS.85%29.aspx)

