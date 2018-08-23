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
ms.openlocfilehash: 39b4474bcc6bd71993fb5dc42bb2bfc1bf9f5f48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573406"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="e5f43-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="e5f43-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="e5f43-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5f43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5f43-105">Проверяет, что вызывающий процесс имеет доступ на чтение для указанного диапазона памяти.</span><span class="sxs-lookup"><span data-stu-id="e5f43-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5f43-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e5f43-106">Header file:</span></span>  <br/> |<span data-ttu-id="e5f43-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="e5f43-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="e5f43-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e5f43-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5f43-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e5f43-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e5f43-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e5f43-110">Called by:</span></span>  <br/> |<span data-ttu-id="e5f43-111">Клиентские приложения и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e5f43-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="e5f43-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5f43-112">Parameters</span></span>

 <span data-ttu-id="e5f43-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="e5f43-113">_lpsz_</span></span>
  
> <span data-ttu-id="e5f43-114">[in] Указатель на строку ASCII символом null.</span><span class="sxs-lookup"><span data-stu-id="e5f43-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="e5f43-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="e5f43-115">_cchMax_</span></span>
  
> <span data-ttu-id="e5f43-116">[in] Максимальный размер строки в символах.</span><span class="sxs-lookup"><span data-stu-id="e5f43-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="e5f43-117">Функция проверяет наличие доступ на чтение в все символы до выполнения определенного пустого строки или до числа символов, указанных в этом параметре, какое из значений меньше.</span><span class="sxs-lookup"><span data-stu-id="e5f43-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="e5f43-118">Если этот параметр равно нулю, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e5f43-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5f43-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e5f43-119">Return value</span></span>

<span data-ttu-id="e5f43-120">Возвращаемое значение равно нулю, когда процесс вызова имеет доступ на чтение к все символы до выполнения определенного пустого строки или доступ на чтение до числа знаков, указанное в _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="e5f43-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="e5f43-121">Значение, возвращаемое при ненулевое процесс вызова не имеет доступ на чтение к все символы до выполнения определенного пустого строки или доступ на чтение до числа знаков, указанное в _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="e5f43-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5f43-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="e5f43-122">Remarks</span></span>

<span data-ttu-id="e5f43-123">Функция **IsBadBoundedStringPtr** эквивалентно использованию **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="e5f43-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5f43-124">См. также</span><span class="sxs-lookup"><span data-stu-id="e5f43-124">See also</span></span>



[<span data-ttu-id="e5f43-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="e5f43-125">IsBadStringPtr</span></span>](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

