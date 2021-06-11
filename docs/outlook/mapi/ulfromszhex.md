---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433054"
---
# <a name="ulfromszhex"></a><span data-ttu-id="5fe4f-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="5fe4f-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="5fe4f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fe4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fe4f-105">Преобразует строку из гексадецимальных цифр null-terminated в незавернутую длинную цепочку.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5fe4f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5fe4f-106">Header file:</span></span>  <br/> |<span data-ttu-id="5fe4f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5fe4f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5fe4f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5fe4f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5fe4f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5fe4f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5fe4f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5fe4f-110">Called by:</span></span>  <br/> |<span data-ttu-id="5fe4f-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="5fe4f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="5fe4f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="5fe4f-112">Parameters</span></span>

 <span data-ttu-id="5fe4f-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="5fe4f-113">_lpsz_</span></span>
  
> <span data-ttu-id="5fe4f-114">[in] Указатель на завершаемую строку null, которая должна быть преобразована.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="5fe4f-115">Параметр  _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5fe4f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fe4f-116">Return value</span></span>

 <span data-ttu-id="5fe4f-117">**UlFromSzHex** возвращает незаверяемую длинную вставку.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="5fe4f-118">Если строка не начинается с хотя бы одной гексадецимальной цифры, возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5fe4f-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="5fe4f-119">Remarks</span></span>

<span data-ttu-id="5fe4f-120">Функция **UlFromSzHex** перестает преобразовываться, когда достигает первого символа в строке, которая не является гексадецимальной цифрой.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="5fe4f-121">Например, с учетом строки "5a" **UlFromSzHex** возвращает значение 90.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="5fe4f-122">С учетом строки "5g5h" функция возвращает значение 5.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="5fe4f-123">Учитывая строку "g5h5", **UlFromSzHex** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="5fe4f-124">**UlFromSzHex** чувствителен к диакритичным различиям, но позволяет как "a" через "f", так и "A" через "F" для гексадецимальных цифр.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="5fe4f-125">Поддерживаются строки в форматах Unicode и DBCS.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="5fe4f-126">Ограничение длины  _lpsz имеет_ символы, а не обязательно bytes.</span><span class="sxs-lookup"><span data-stu-id="5fe4f-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

