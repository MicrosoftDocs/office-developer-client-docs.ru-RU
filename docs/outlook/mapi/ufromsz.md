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
# <a name="ufromsz"></a><span data-ttu-id="9d0e4-103">UFromSz</span><span class="sxs-lookup"><span data-stu-id="9d0e4-103">UFromSz</span></span>

  
  
<span data-ttu-id="9d0e4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d0e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d0e4-105">Преобразует строку десятичных цифр с завершающим нулем в целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-105">Converts a null-terminated string of decimal digits into an unsigned integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d0e4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9d0e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d0e4-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9d0e4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9d0e4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9d0e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d0e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d0e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d0e4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9d0e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="9d0e4-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9d0e4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a><span data-ttu-id="9d0e4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d0e4-112">Parameters</span></span>

 <span data-ttu-id="9d0e4-113">_лпсз_</span><span class="sxs-lookup"><span data-stu-id="9d0e4-113">_lpsz_</span></span>
  
> <span data-ttu-id="9d0e4-114">возврата Указатель на преобразуемую строку, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="9d0e4-115">Значение параметра _лпсз_ не должно превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d0e4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d0e4-116">Return value</span></span>

 <span data-ttu-id="9d0e4-117">**Уфромсз** возвращает целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-117">**UFromSz** returns an unsigned integer.</span></span> <span data-ttu-id="9d0e4-118">Если строка не начинается по крайней мере с одной десятичной цифрой, возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-118">If the string does not begin with at least one decimal digit, zero is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9d0e4-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d0e4-119">Remarks</span></span>

<span data-ttu-id="9d0e4-120">Функция **уфромсз** завершает преобразование при достижении первого символа в строке, не являющийся десятичной цифрой.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-120">The **UFromSz** function stops converting when it reaches the first character in the string that is not a decimal digit.</span></span> <span data-ttu-id="9d0e4-121">Например, если задается строка "55", **уфромсз** возвращает целое значение 55.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-121">For example, given the string "55", **UFromSz** returns the integer value 55.</span></span> <span data-ttu-id="9d0e4-122">При наличии строки "5a5b" функция возвращает целое значение 5.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-122">Given the string "5a5b", the function returns the integer value 5.</span></span> <span data-ttu-id="9d0e4-123">При наличии строки "a5b5" **уфромсз** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-123">Given the string "a5b5", **UFromSz** returns zero.</span></span> 
  
 <span data-ttu-id="9d0e4-124">**Уфромсз** учитывает диакритические различия.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-124">**UFromSz** is sensitive to diacritical differences.</span></span> <span data-ttu-id="9d0e4-125">Поддерживаются строки в форматах Юникод и DBCS.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-125">Strings in the Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="9d0e4-126">Предельная длина в _лпсз_ — символы, не обязательно — байты.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-126">The length limit on  _lpsz_ is in characters, not necessarily bytes.</span></span> 
  

