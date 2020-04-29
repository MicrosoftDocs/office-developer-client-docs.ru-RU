---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439760"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="3c2c4-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="3c2c4-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="3c2c4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c2c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c2c4-105">Преобразует заданную часть строкового представления шестнадцатеричного числа в двоичное число.</span><span class="sxs-lookup"><span data-stu-id="3c2c4-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3c2c4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3c2c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="3c2c4-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="3c2c4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3c2c4-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3c2c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3c2c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3c2c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3c2c4-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3c2c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="3c2c4-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3c2c4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="3c2c4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c2c4-112">Parameters</span></span>

 <span data-ttu-id="3c2c4-113">_сз_</span><span class="sxs-lookup"><span data-stu-id="3c2c4-113">_sz_</span></span>
  
> <span data-ttu-id="3c2c4-114">возврата Указатель на преобразуемую строку, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="3c2c4-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="3c2c4-115">Допустимыми символами являются шестнадцатеричные символы от 0 до 9, а как прописные, так и строчные буквы от a до f.</span><span class="sxs-lookup"><span data-stu-id="3c2c4-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="3c2c4-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="3c2c4-116">_pb_</span></span>
  
> <span data-ttu-id="3c2c4-117">вышли Указатель на возвращаемое двоичное число.</span><span class="sxs-lookup"><span data-stu-id="3c2c4-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="3c2c4-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="3c2c4-118">_cb_</span></span>
  
> <span data-ttu-id="3c2c4-119">возврата Размер (в байтах) параметра _Pb_ .</span><span class="sxs-lookup"><span data-stu-id="3c2c4-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3c2c4-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c2c4-120">Return value</span></span>

<span data-ttu-id="3c2c4-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c2c4-121">S_OK</span></span>
  
> <span data-ttu-id="3c2c4-122">Преобразование выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="3c2c4-122">Conversion was successful.</span></span>
    
<span data-ttu-id="3c2c4-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="3c2c4-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="3c2c4-124">Обнаружены недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="3c2c4-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c2c4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3c2c4-125">See also</span></span>



[<span data-ttu-id="3c2c4-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="3c2c4-126">FBinFromHex</span></span>](fbinfromhex.md)

