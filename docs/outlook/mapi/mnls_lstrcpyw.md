---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Последнее изменение: 18 июня 2012 г.'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382710"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="0dc1f-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="0dc1f-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="0dc1f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dc1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dc1f-105">Копирует строки в буфер.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="0dc1f-106">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-106">Do not use.</span></span> <span data-ttu-id="0dc1f-107">Рекомендуется использовать [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0dc1f-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="0dc1f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dc1f-108">Parameters</span></span>

<span data-ttu-id="0dc1f-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="0dc1f-109">lpString1</span></span>
  
> <span data-ttu-id="0dc1f-110">[out] Буфер для получения содержимого строки, на который указывает параметр lpString2.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="0dc1f-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="0dc1f-111">lpString2</span></span>
  
> <span data-ttu-id="0dc1f-112">[in] Строка для копирования символом null.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0dc1f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dc1f-113">Return value</span></span>

<span data-ttu-id="0dc1f-114">Если функция успешно выполнена, возвращается указатель на буфер.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="0dc1f-115">В случае сбоя функция возвращает значение NULL, и lpString1 могут быть символом null.</span><span class="sxs-lookup"><span data-stu-id="0dc1f-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0dc1f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="0dc1f-116">Remarks</span></span>

<span data-ttu-id="0dc1f-117">Эта функция имеет функцию **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="0dc1f-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="0dc1f-118">Для получения дополнительных сведений см [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0dc1f-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0dc1f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0dc1f-119">See also</span></span>



[<span data-ttu-id="0dc1f-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="0dc1f-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

