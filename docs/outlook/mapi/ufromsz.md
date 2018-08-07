---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812550"
---
# <a name="ufromsz"></a><span data-ttu-id="dc1b3-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="dc1b3-103">UFromSz</span></span>

  
  
<span data-ttu-id="dc1b3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dc1b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dc1b3-105">Преобразует строку символом null из десятичных цифр в целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dc1b3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="dc1b3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dc1b3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="dc1b3-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dc1b3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dc1b3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dc1b3-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-110">Called by:</span></span>  <br/> |<span data-ttu-id="dc1b3-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="dc1b3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="dc1b3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc1b3-112">Parameters</span></span>

 <span data-ttu-id="dc1b3-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="dc1b3-113">_lpsz_</span></span>
  
> <span data-ttu-id="dc1b3-114">[in] Указатель на строку символом null, которую нужно преобразовать.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="dc1b3-115">Параметр _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc1b3-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="dc1b3-116">Return value</span></span>

 <span data-ttu-id="dc1b3-117">**UFromSz** возвращает целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="dc1b3-118">Если строка не начинается с по крайней мере один десятичное число, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dc1b3-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc1b3-119">Remarks</span></span>

<span data-ttu-id="dc1b3-120">Функция **UFromSz** прекращает преобразование при достижении первым символом в строке, которая не является десятичных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="dc1b3-121">Например **UFromSz** данной строки «55», возвращает целое значение 55.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="dc1b3-122">Учитывая строка «5a5b», функция возвращает целое значение 5.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="dc1b3-123">Учитывая строка «a5b5», **UFromSz** возвращает нуль.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="dc1b3-124">**UFromSz** учета диакритических различия.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="dc1b3-125">Поддерживаются строки в формате Юникод и DBCS.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="dc1b3-126">Ограничение длины на _lpsz_ находится в символы, не обязательно в байтах.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

