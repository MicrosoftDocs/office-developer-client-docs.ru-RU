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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810034"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="2589f-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="2589f-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="2589f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2589f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2589f-105">Копирует строки в буфер.</span><span class="sxs-lookup"><span data-stu-id="2589f-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="2589f-106">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="2589f-106">Do not use.</span></span> <span data-ttu-id="2589f-107">Рекомендуется использовать [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2589f-107">Consider using [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="2589f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2589f-108">Parameters</span></span>

<span data-ttu-id="2589f-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="2589f-109">lpString1</span></span>
  
> <span data-ttu-id="2589f-110">[out] Буфер для получения содержимого строки, на который указывает параметр lpString2.</span><span class="sxs-lookup"><span data-stu-id="2589f-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="2589f-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="2589f-111">lpString2</span></span>
  
> <span data-ttu-id="2589f-112">[in] Строка для копирования символом null.</span><span class="sxs-lookup"><span data-stu-id="2589f-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2589f-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2589f-113">Return value</span></span>

<span data-ttu-id="2589f-114">Если функция успешно выполнена, возвращается указатель на буфер.</span><span class="sxs-lookup"><span data-stu-id="2589f-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="2589f-115">В случае сбоя функция возвращает значение NULL, и lpString1 могут быть символом null.</span><span class="sxs-lookup"><span data-stu-id="2589f-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2589f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="2589f-116">Remarks</span></span>

<span data-ttu-id="2589f-117">Эта функция имеет функцию **lstrcpy** .</span><span class="sxs-lookup"><span data-stu-id="2589f-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="2589f-118">Для получения дополнительных сведений см [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2589f-118">For more information, see [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2589f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2589f-119">See also</span></span>



[<span data-ttu-id="2589f-120">lstrcpy</span><span class="sxs-lookup"><span data-stu-id="2589f-120">lstrcpy</span></span>](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

