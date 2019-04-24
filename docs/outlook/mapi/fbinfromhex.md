---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341645"
---
# <a name="fbinfromhex"></a><span data-ttu-id="a29e8-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="a29e8-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="a29e8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a29e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a29e8-105">Преобразует строковое представление шестнадцатеричного числа в двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="a29e8-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a29e8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a29e8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a29e8-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="a29e8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a29e8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a29e8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a29e8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a29e8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a29e8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a29e8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a29e8-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a29e8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="a29e8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a29e8-112">Parameters</span></span>

 <span data-ttu-id="a29e8-113">_СЗ_</span><span class="sxs-lookup"><span data-stu-id="a29e8-113">_sz_</span></span>
  
> <span data-ttu-id="a29e8-114">возврата Указатель на строку ASCII с завершающим нулем для преобразования.</span><span class="sxs-lookup"><span data-stu-id="a29e8-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="a29e8-115">Он не является строкой Юникода.</span><span class="sxs-lookup"><span data-stu-id="a29e8-115">It is not a Unicode string.</span></span> <span data-ttu-id="a29e8-116">Допустимые символы включают в себя шестнадцатеричные символы от нуля до девяти, прописные и строчные буквы от A до F.</span><span class="sxs-lookup"><span data-stu-id="a29e8-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="a29e8-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="a29e8-117">_pb_</span></span>
  
> <span data-ttu-id="a29e8-118">вышли Указатель на возвращаемое двоичное число.</span><span class="sxs-lookup"><span data-stu-id="a29e8-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a29e8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a29e8-119">Return value</span></span>

<span data-ttu-id="a29e8-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="a29e8-120">TRUE</span></span> 
  
> <span data-ttu-id="a29e8-121">Строка успешно преобразована в двоичное число.</span><span class="sxs-lookup"><span data-stu-id="a29e8-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="a29e8-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="a29e8-122">FALSE</span></span> 
  
> <span data-ttu-id="a29e8-123">Входная строка содержит недопустимые шестнадцатеричные символы ASCII.</span><span class="sxs-lookup"><span data-stu-id="a29e8-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a29e8-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a29e8-124">See also</span></span>



[<span data-ttu-id="a29e8-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="a29e8-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

