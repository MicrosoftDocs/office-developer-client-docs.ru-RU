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
ms.openlocfilehash: a00a9b2200f76dfd600f72bf387467b5792599c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812184"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="c937a-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="c937a-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="c937a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c937a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c937a-105">Преобразует указанную часть строковое представление шестнадцатеричное число в двоичное.</span><span class="sxs-lookup"><span data-stu-id="c937a-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c937a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c937a-106">Header file:</span></span>  <br/> |<span data-ttu-id="c937a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c937a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c937a-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c937a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c937a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c937a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c937a-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c937a-110">Called by:</span></span>  <br/> |<span data-ttu-id="c937a-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="c937a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="c937a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c937a-112">Parameters</span></span>

 <span data-ttu-id="c937a-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="c937a-113">_sz_</span></span>
  
> <span data-ttu-id="c937a-114">[in] Указатель на строку символом null, которую нужно преобразовать.</span><span class="sxs-lookup"><span data-stu-id="c937a-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="c937a-115">Допустимые знаки включают шестнадцатеричных знаков 0 до 9 и прописные и строчные буквы по f.</span><span class="sxs-lookup"><span data-stu-id="c937a-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="c937a-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="c937a-116">_pb_</span></span>
  
> <span data-ttu-id="c937a-117">[out] Указатель на возвращаемый двоичное число.</span><span class="sxs-lookup"><span data-stu-id="c937a-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="c937a-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="c937a-118">_cb_</span></span>
  
> <span data-ttu-id="c937a-119">[in] Размер, в байтах, параметр _pb_ .</span><span class="sxs-lookup"><span data-stu-id="c937a-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c937a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="c937a-121">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c937a-121">S_OK</span></span>
  
> <span data-ttu-id="c937a-122">Преобразование прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="c937a-122">Conversion was successful.</span></span>
    
<span data-ttu-id="c937a-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="c937a-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="c937a-124">Обнаружены недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="c937a-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c937a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c937a-125">See also</span></span>



[<span data-ttu-id="c937a-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="c937a-126">FBinFromHex</span></span>](fbinfromhex.md)

