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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414937"
---
# <a name="fbinfromhex"></a><span data-ttu-id="1a43c-103">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="1a43c-103">FBinFromHex</span></span>

  
  
<span data-ttu-id="1a43c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a43c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a43c-105">Преобразует строковое представление шестнадцатеричного числа в двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="1a43c-105">Converts a string representation of a hexadecimal number to binary data.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a43c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1a43c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1a43c-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="1a43c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1a43c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="1a43c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1a43c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1a43c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1a43c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="1a43c-110">Called by:</span></span>  <br/> |<span data-ttu-id="1a43c-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="1a43c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a><span data-ttu-id="1a43c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a43c-112">Parameters</span></span>

 <span data-ttu-id="1a43c-113">_СЗ_</span><span class="sxs-lookup"><span data-stu-id="1a43c-113">_sz_</span></span>
  
> <span data-ttu-id="1a43c-114">возврата Указатель на строку ASCII с завершающим нулем для преобразования.</span><span class="sxs-lookup"><span data-stu-id="1a43c-114">[in] Pointer to the null-terminated ASCII string to be converted.</span></span> <span data-ttu-id="1a43c-115">Он не является строкой Юникода.</span><span class="sxs-lookup"><span data-stu-id="1a43c-115">It is not a Unicode string.</span></span> <span data-ttu-id="1a43c-116">Допустимые символы включают в себя шестнадцатеричные символы от нуля до девяти, прописные и строчные буквы от A до F.</span><span class="sxs-lookup"><span data-stu-id="1a43c-116">Valid characters include the hexadecimal characters zero through nine and both uppercase and lowercase characters A through F.</span></span>
    
 <span data-ttu-id="1a43c-117">_pb_</span><span class="sxs-lookup"><span data-stu-id="1a43c-117">_pb_</span></span>
  
> <span data-ttu-id="1a43c-118">вышли Указатель на возвращаемое двоичное число.</span><span class="sxs-lookup"><span data-stu-id="1a43c-118">[out] Pointer to the returned binary number.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a43c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a43c-119">Return value</span></span>

<span data-ttu-id="1a43c-120">TRUE</span><span class="sxs-lookup"><span data-stu-id="1a43c-120">TRUE</span></span> 
  
> <span data-ttu-id="1a43c-121">Строка успешно преобразована в двоичное число.</span><span class="sxs-lookup"><span data-stu-id="1a43c-121">The string was successfully converted into a binary number.</span></span> 
    
<span data-ttu-id="1a43c-122">FALSE</span><span class="sxs-lookup"><span data-stu-id="1a43c-122">FALSE</span></span> 
  
> <span data-ttu-id="1a43c-123">Входная строка содержит недопустимые шестнадцатеричные символы ASCII.</span><span class="sxs-lookup"><span data-stu-id="1a43c-123">The input string contains invalid ASCII hexadecimal characters.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a43c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="1a43c-124">See also</span></span>



[<span data-ttu-id="1a43c-125">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="1a43c-125">ScBinFromHexBounded</span></span>](scbinfromhexbounded.md)

