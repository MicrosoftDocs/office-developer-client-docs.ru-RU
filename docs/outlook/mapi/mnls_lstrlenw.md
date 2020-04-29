---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Дата последнего изменения: 21 февраля 2012 г.'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338467"
---
# <a name="mnls_lstrlenw"></a><span data-ttu-id="295cb-103">MNLS_lstrlenW</span><span class="sxs-lookup"><span data-stu-id="295cb-103">MNLS_lstrlenW</span></span>

  
  
<span data-ttu-id="295cb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="295cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="295cb-105">Определяет длину указанной строки Юникода, за исключением завершающего знака null.</span><span class="sxs-lookup"><span data-stu-id="295cb-105">Determines the length of the specified Unicode string, excluding the terminating null character.</span></span>
  
> [!TIP]
> <span data-ttu-id="295cb-106">Вместо этого рекомендуется использовать [стрингкчленгс](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="295cb-106">Consider using [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) instead.</span></span> 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a><span data-ttu-id="295cb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="295cb-107">Parameters</span></span>

 <span data-ttu-id="295cb-108">_лпсз_</span><span class="sxs-lookup"><span data-stu-id="295cb-108">_lpsz_</span></span>
  
> <span data-ttu-id="295cb-109">возврата Строка Юникода с завершающим нулем для проверки.</span><span class="sxs-lookup"><span data-stu-id="295cb-109">[in] The null-terminated Unicode string to be checked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="295cb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="295cb-110">Return value</span></span>

<span data-ttu-id="295cb-111">Функция возвращает целое число с длиной строки.</span><span class="sxs-lookup"><span data-stu-id="295cb-111">The function returns an integer with the length of the string.</span></span> <span data-ttu-id="295cb-112">Это количество символов в строке, за исключением завершающего знака null.</span><span class="sxs-lookup"><span data-stu-id="295cb-112">It is a count of characters in the string, excluding the terminating null character.</span></span> <span data-ttu-id="295cb-113">Если _лпсз_ имеет значение null, функция возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="295cb-113">If  _lpsz_ is NULL, the function returns zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="295cb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="295cb-114">Remarks</span></span>

<span data-ttu-id="295cb-115">Эта функция заключает в оболочку функцию **лстрлен** .</span><span class="sxs-lookup"><span data-stu-id="295cb-115">This function wraps the **lstrlen** function.</span></span> <span data-ttu-id="295cb-116">Дополнительные сведения см. в разделе [лстрлен](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="295cb-116">For more information, see [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="295cb-117">См. также</span><span class="sxs-lookup"><span data-stu-id="295cb-117">See also</span></span>



[<span data-ttu-id="295cb-118">лстрлен</span><span class="sxs-lookup"><span data-stu-id="295cb-118">lstrlen</span></span>](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[<span data-ttu-id="295cb-119">стрингкчленгс</span><span class="sxs-lookup"><span data-stu-id="295cb-119">StringCchLength</span></span>](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

