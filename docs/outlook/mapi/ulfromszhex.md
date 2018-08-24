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
ms.openlocfilehash: e6de4be29811dafaf5288b2ccb39c0342a314bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584627"
---
# <a name="ulfromszhex"></a><span data-ttu-id="48a7b-103">UlFromSzHex</span><span class="sxs-lookup"><span data-stu-id="48a7b-103">UlFromSzHex</span></span>

  
  
<span data-ttu-id="48a7b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48a7b-105">Преобразует строку символом null шестнадцатеричных цифр в длинное целое без знака.</span><span class="sxs-lookup"><span data-stu-id="48a7b-105">Converts a null-terminated string of hexadecimal digits into an unsigned long integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48a7b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="48a7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="48a7b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48a7b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="48a7b-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="48a7b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48a7b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48a7b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48a7b-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="48a7b-110">Called by:</span></span>  <br/> |<span data-ttu-id="48a7b-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="48a7b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="48a7b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="48a7b-112">Parameters</span></span>

 <span data-ttu-id="48a7b-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="48a7b-113">_lpsz_</span></span>
  
> <span data-ttu-id="48a7b-114">[in] Указатель на строку символом null, которую нужно преобразовать.</span><span class="sxs-lookup"><span data-stu-id="48a7b-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="48a7b-115">Параметр _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="48a7b-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48a7b-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="48a7b-116">Return value</span></span>

 <span data-ttu-id="48a7b-117">**UlFromSzHex** Возвращает длинное целое.</span><span class="sxs-lookup"><span data-stu-id="48a7b-117">**UlFromSzHex** returns an unsigned long integer.</span></span> <span data-ttu-id="48a7b-118">Если строка не начинается с по крайней мере один шестнадцатеричных цифр, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="48a7b-118">If the string does not begin with at least one hexadecimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="48a7b-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="48a7b-119">Remarks</span></span>

<span data-ttu-id="48a7b-120">Функция **UlFromSzHex** прекращает преобразование при достижении первым символом в строке, которая не является шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="48a7b-120">The **UlFromSzHex** function stops converting when it reaches the first character in the string that is not a hexadecimal digit.</span></span> <span data-ttu-id="48a7b-121">Например **UlFromSzHex** данной строки «5a», возвращает целое значение 90.</span><span class="sxs-lookup"><span data-stu-id="48a7b-121">For example, given the string "5a", **UlFromSzHex** returns the integer value 90.</span></span> <span data-ttu-id="48a7b-122">Учитывая строка «5g5h», функция возвращает целое значение 5.</span><span class="sxs-lookup"><span data-stu-id="48a7b-122">Given the string "5g5h", the function returns the integer value 5.</span></span> <span data-ttu-id="48a7b-123">Учитывая строка «g5h5», **UlFromSzHex** возвращает нуль.</span><span class="sxs-lookup"><span data-stu-id="48a7b-123">Given the string "g5h5", **UlFromSzHex** returns zero.</span></span> 
  
 <span data-ttu-id="48a7b-124">**UlFromSzHex** учета диакритических различия, но обеспечивает как «» до «f» и «» до «F» для шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="48a7b-124">**UlFromSzHex** is sensitive to diacritical differences but allows both 'a' through 'f' and 'A' through 'F' for hexadecimal digits.</span></span> <span data-ttu-id="48a7b-125">Поддерживаются строки в формате Юникод и DBCS.</span><span class="sxs-lookup"><span data-stu-id="48a7b-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="48a7b-126">Ограничение длины на _lpsz_ находится в символы, не обязательно в байтах.</span><span class="sxs-lookup"><span data-stu-id="48a7b-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

