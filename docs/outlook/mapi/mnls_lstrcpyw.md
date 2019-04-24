---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Дата последнего изменения: 18 июня 2012 г.'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341729"
---
# <a name="mnlslstrcpyw"></a><span data-ttu-id="0286e-103">MNLS_lstrcpyW</span><span class="sxs-lookup"><span data-stu-id="0286e-103">MNLS_lstrcpyW</span></span>

 
  
<span data-ttu-id="0286e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0286e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0286e-105">Копирует строку в буфер.</span><span class="sxs-lookup"><span data-stu-id="0286e-105">Copies a string to a buffer.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="0286e-106">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="0286e-106">Do not use.</span></span> <span data-ttu-id="0286e-107">Вместо этого рекомендуется использовать [стрингкчкопи](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0286e-107">Consider using [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a><span data-ttu-id="0286e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0286e-108">Parameters</span></span>

<span data-ttu-id="0286e-109">lpString1</span><span class="sxs-lookup"><span data-stu-id="0286e-109">lpString1</span></span>
  
> <span data-ttu-id="0286e-110">вышли Буфер для получения содержимого строки, на которую указывает параметр lpString2.</span><span class="sxs-lookup"><span data-stu-id="0286e-110">[out] A buffer to receive the contents of the string pointed to by the lpString2 parameter.</span></span>
    
<span data-ttu-id="0286e-111">lpString2</span><span class="sxs-lookup"><span data-stu-id="0286e-111">lpString2</span></span>
  
> <span data-ttu-id="0286e-112">возврата Копируемая строка, заканчивающаяся нулем.</span><span class="sxs-lookup"><span data-stu-id="0286e-112">[in] The null-terminated string to be copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0286e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0286e-113">Return value</span></span>

<span data-ttu-id="0286e-114">Если функция выполнена успешно, возвращаемое значение является указателем на буфер.</span><span class="sxs-lookup"><span data-stu-id="0286e-114">If the function succeeds, the return value is a pointer to the buffer.</span></span>
  
<span data-ttu-id="0286e-115">Если функция завершается с ошибкой, возвращается значение NULL, а lpString1 не может оканчиваться нулем.</span><span class="sxs-lookup"><span data-stu-id="0286e-115">If the function fails, the return value is NULL and lpString1 may not be null-terminated.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0286e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0286e-116">Remarks</span></span>

<span data-ttu-id="0286e-117">Эта функция заключает в оболочку функцию **лстркпи** .</span><span class="sxs-lookup"><span data-stu-id="0286e-117">This function wraps the **lstrcpy** function.</span></span> <span data-ttu-id="0286e-118">Дополнительные сведения см. в разделе [лстркпи](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0286e-118">For more information, see [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0286e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0286e-119">See also</span></span>



[<span data-ttu-id="0286e-120">лстркпи</span><span class="sxs-lookup"><span data-stu-id="0286e-120">lstrcpy</span></span>](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

