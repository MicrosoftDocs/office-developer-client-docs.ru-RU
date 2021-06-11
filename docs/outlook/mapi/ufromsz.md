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
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439011"
---
# <a name="ufromsz"></a><span data-ttu-id="9d653-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="9d653-103">UFromSz</span></span>

  
  
<span data-ttu-id="9d653-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d653-105">Преобразует строку десятичных цифр с null-terminated в неподписавую цепочку.</span><span class="sxs-lookup"><span data-stu-id="9d653-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d653-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9d653-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d653-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d653-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9d653-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9d653-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d653-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d653-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d653-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9d653-110">Called by:</span></span>  <br/> |<span data-ttu-id="9d653-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9d653-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="9d653-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="9d653-112">Parameters</span></span>

 <span data-ttu-id="9d653-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="9d653-113">_lpsz_</span></span>
  
> <span data-ttu-id="9d653-114">[in] Указатель на завершаемую строку null, которая должна быть преобразована.</span><span class="sxs-lookup"><span data-stu-id="9d653-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="9d653-115">Параметр  _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="9d653-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d653-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d653-116">Return value</span></span>

 <span data-ttu-id="9d653-117">**UFromSz** возвращает незаверяемую ставку.</span><span class="sxs-lookup"><span data-stu-id="9d653-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="9d653-118">Если строка не начинается с хотя бы одной десятичной цифры, возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="9d653-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9d653-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d653-119">Remarks</span></span>

<span data-ttu-id="9d653-120">Функция **UFromSz** прекращает преобразование, когда достигает первого символа в строке, которая не является десятичной цифрой.</span><span class="sxs-lookup"><span data-stu-id="9d653-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="9d653-121">Например, с учетом строки "55", **UFromSz** возвращает значение 55.</span><span class="sxs-lookup"><span data-stu-id="9d653-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="9d653-122">С учетом строки "5a5b" функция возвращает значение 5.</span><span class="sxs-lookup"><span data-stu-id="9d653-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="9d653-123">Учитывая строку "a5b5", **UFromSz** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="9d653-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="9d653-124">**UFromSz чувствителен** к диакритичным различиям.</span><span class="sxs-lookup"><span data-stu-id="9d653-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="9d653-125">Поддерживаются строки в форматах Unicode и DBCS.</span><span class="sxs-lookup"><span data-stu-id="9d653-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="9d653-126">Ограничение длины  _lpsz имеет_ символы, а не обязательно bytes.</span><span class="sxs-lookup"><span data-stu-id="9d653-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

