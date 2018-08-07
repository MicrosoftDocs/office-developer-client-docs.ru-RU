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
ms.openlocfilehash: 64d205ee7f51c0ce6a6eb1e982659c6cda675f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808434"
---
# <a name="fbinfromhex"></a><span data-ttu-id="6a883-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="6a883-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="6a883-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6a883-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6a883-105">Преобразует строковое представление шестнадцатеричного числа в двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="6a883-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a883-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6a883-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a883-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6a883-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6a883-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="6a883-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a883-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a883-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a883-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="6a883-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a883-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="6a883-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="6a883-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a883-112">Parameters</span></span>

 <span data-ttu-id="6a883-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="6a883-113">_sz_</span></span>
  
> <span data-ttu-id="6a883-114">[in] Указатель на строку ASCII символом null, которую нужно преобразовать.</span><span class="sxs-lookup"><span data-stu-id="6a883-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="6a883-115">Не является строка Юникода.</span><span class="sxs-lookup"><span data-stu-id="6a883-115">It is not a Unicode string.</span></span> <span data-ttu-id="6a883-116">Допустимые знаки включают шестнадцатеричных знаков нулевой до девяти как, так и прописные и строчные буквы A до F.</span><span class="sxs-lookup"><span data-stu-id="6a883-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="6a883-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="6a883-117">_pb_</span></span>
  
> <span data-ttu-id="6a883-118">[out] Указатель на возвращаемый двоичное число.</span><span class="sxs-lookup"><span data-stu-id="6a883-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6a883-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6a883-119">Return value</span></span>

<span data-ttu-id="6a883-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="6a883-120">TRUE</span></span> 
  
> <span data-ttu-id="6a883-121">Строка была успешно преобразуется в двоичное.</span><span class="sxs-lookup"><span data-stu-id="6a883-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="6a883-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="6a883-122">FALSE</span></span> 
  
> <span data-ttu-id="6a883-123">Входная строка содержит недопустимый шестнадцатеричных знаков ASCII.</span><span class="sxs-lookup"><span data-stu-id="6a883-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a883-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6a883-124">See also</span></span>



[<span data-ttu-id="6a883-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="6a883-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

