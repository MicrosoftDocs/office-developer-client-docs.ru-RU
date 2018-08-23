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
ms.openlocfilehash: 7513e361f4c1c1bcc93cc420f3a1987e0d817c54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580504"
---
# <a name="ufromsz"></a><span data-ttu-id="709ea-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="709ea-103">UFromSz</span></span>

  
  
<span data-ttu-id="709ea-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="709ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="709ea-105">Преобразует строку символом null из десятичных цифр в целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="709ea-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="709ea-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="709ea-106">Header file:</span></span>  <br/> |<span data-ttu-id="709ea-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="709ea-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="709ea-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="709ea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="709ea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="709ea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="709ea-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="709ea-110">Called by:</span></span>  <br/> |<span data-ttu-id="709ea-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="709ea-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="709ea-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="709ea-112">Parameters</span></span>

 <span data-ttu-id="709ea-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="709ea-113">_lpsz_</span></span>
  
> <span data-ttu-id="709ea-114">[in] Указатель на строку символом null, которую нужно преобразовать.</span><span class="sxs-lookup"><span data-stu-id="709ea-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="709ea-115">Параметр _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="709ea-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="709ea-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="709ea-116">Return value</span></span>

 <span data-ttu-id="709ea-117">**UFromSz** возвращает целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="709ea-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="709ea-118">Если строка не начинается с по крайней мере один десятичное число, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="709ea-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="709ea-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="709ea-119">Remarks</span></span>

<span data-ttu-id="709ea-120">Функция **UFromSz** прекращает преобразование при достижении первым символом в строке, которая не является десятичных цифр.</span><span class="sxs-lookup"><span data-stu-id="709ea-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="709ea-121">Например **UFromSz** данной строки «55», возвращает целое значение 55.</span><span class="sxs-lookup"><span data-stu-id="709ea-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="709ea-122">Учитывая строка «5a5b», функция возвращает целое значение 5.</span><span class="sxs-lookup"><span data-stu-id="709ea-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="709ea-123">Учитывая строка «a5b5», **UFromSz** возвращает нуль.</span><span class="sxs-lookup"><span data-stu-id="709ea-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="709ea-124">**UFromSz** учета диакритических различия.</span><span class="sxs-lookup"><span data-stu-id="709ea-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="709ea-125">Поддерживаются строки в формате Юникод и DBCS.</span><span class="sxs-lookup"><span data-stu-id="709ea-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="709ea-126">Ограничение длины на _lpsz_ находится в символы, не обязательно в байтах.</span><span class="sxs-lookup"><span data-stu-id="709ea-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

