---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388905"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="7b753-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="7b753-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="7b753-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b753-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b753-105">Проверяет, что вызывающий процесс имеет доступ на чтение для указанного диапазона памяти.</span><span class="sxs-lookup"><span data-stu-id="7b753-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b753-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7b753-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b753-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="7b753-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="7b753-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7b753-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b753-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b753-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b753-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7b753-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b753-111">Клиентские приложения и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="7b753-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="7b753-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b753-112">Parameters</span></span>

 <span data-ttu-id="7b753-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="7b753-113">_lpsz_</span></span>
  
> <span data-ttu-id="7b753-114">[in] Указатель на строку ASCII символом null.</span><span class="sxs-lookup"><span data-stu-id="7b753-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="7b753-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="7b753-115">_cchMax_</span></span>
  
> <span data-ttu-id="7b753-116">[in] Максимальный размер строки в символах.</span><span class="sxs-lookup"><span data-stu-id="7b753-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="7b753-117">Функция проверяет наличие доступ на чтение в все символы до выполнения определенного пустого строки или до числа символов, указанных в этом параметре, какое из значений меньше.</span><span class="sxs-lookup"><span data-stu-id="7b753-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="7b753-118">Если этот параметр равно нулю, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7b753-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7b753-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b753-119">Return value</span></span>

<span data-ttu-id="7b753-120">Возвращаемое значение равно нулю, когда процесс вызова имеет доступ на чтение к все символы до выполнения определенного пустого строки или доступ на чтение до числа знаков, указанное в _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="7b753-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="7b753-121">Значение, возвращаемое при ненулевое процесс вызова не имеет доступ на чтение к все символы до выполнения определенного пустого строки или доступ на чтение до числа знаков, указанное в _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="7b753-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b753-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="7b753-122">Remarks</span></span>

<span data-ttu-id="7b753-123">Функция **IsBadBoundedStringPtr** эквивалентно использованию **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="7b753-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7b753-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7b753-124">See also</span></span>



[<span data-ttu-id="7b753-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="7b753-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

