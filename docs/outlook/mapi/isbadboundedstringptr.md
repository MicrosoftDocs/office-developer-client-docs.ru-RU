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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278836"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="a5a31-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="a5a31-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="a5a31-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5a31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5a31-105">Проверяет, есть ли у вызываемого процесса доступ на чтение к указанному диапазону памяти.</span><span class="sxs-lookup"><span data-stu-id="a5a31-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5a31-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a5a31-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5a31-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="a5a31-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="a5a31-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a5a31-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a5a31-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a5a31-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a5a31-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a5a31-110">Called by:</span></span>  <br/> |<span data-ttu-id="a5a31-111">Клиентские приложения и поставщики услуг.</span><span class="sxs-lookup"><span data-stu-id="a5a31-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="a5a31-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5a31-112">Parameters</span></span>

 <span data-ttu-id="a5a31-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a5a31-113">_lpsz_</span></span>
  
> <span data-ttu-id="a5a31-114">[in] Указатель на строку ASCII, одернутую нулью.</span><span class="sxs-lookup"><span data-stu-id="a5a31-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="a5a31-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="a5a31-115">_cchMax_</span></span>
  
> <span data-ttu-id="a5a31-116">[in] Максимальный размер строки в chars.</span><span class="sxs-lookup"><span data-stu-id="a5a31-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="a5a31-117">Функция проверяет доступ на чтение во всех символах до символа null строки или до числа символов, указанных этим параметром, в зависимости от того, какой символ меньше.</span><span class="sxs-lookup"><span data-stu-id="a5a31-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="a5a31-118">Если этот параметр имеет нулевое значение, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a5a31-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5a31-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5a31-119">Return value</span></span>

<span data-ttu-id="a5a31-120">Возвращаемая величина — нуль, если вызывающий процесс имеет доступ на чтение ко всем символам до символа null строки или доступу на чтение до количества символов, указанных _cchMax._</span><span class="sxs-lookup"><span data-stu-id="a5a31-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="a5a31-121">Возвращаемая величина не является нулем, если вызывающий процесс не имеет доступа на чтение ко всем символам до символа нулевых терминов строки или доступу на чтение до количества символов, указанных _cchMax._</span><span class="sxs-lookup"><span data-stu-id="a5a31-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5a31-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5a31-122">Remarks</span></span>

<span data-ttu-id="a5a31-123">Функция **IsBadBoundedStringPtr** эквивалентна использованию **IsBadStringPtr.**</span><span class="sxs-lookup"><span data-stu-id="a5a31-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5a31-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a5a31-124">See also</span></span>



[<span data-ttu-id="a5a31-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="a5a31-125">IsBadStringPtr</span></span>](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

