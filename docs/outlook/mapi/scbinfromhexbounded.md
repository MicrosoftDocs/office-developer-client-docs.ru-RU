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
ms.openlocfilehash: 135db8d690d4d4bd610bd15893c358fedddb4605
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589282"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="7ebb5-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="7ebb5-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="7ebb5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ebb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ebb5-105">Преобразует указанную часть строковое представление шестнадцатеричное число в двоичное.</span><span class="sxs-lookup"><span data-stu-id="7ebb5-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7ebb5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7ebb5-106">Header file:</span></span>  <br/> |<span data-ttu-id="7ebb5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7ebb5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7ebb5-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7ebb5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7ebb5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7ebb5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7ebb5-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7ebb5-110">Called by:</span></span>  <br/> |<span data-ttu-id="7ebb5-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="7ebb5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="7ebb5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ebb5-112">Parameters</span></span>

 <span data-ttu-id="7ebb5-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="7ebb5-113">_sz_</span></span>
  
> <span data-ttu-id="7ebb5-114">[in] Указатель на строку символом null, которую нужно преобразовать.</span><span class="sxs-lookup"><span data-stu-id="7ebb5-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="7ebb5-115">Допустимые знаки включают шестнадцатеричных знаков 0 до 9 и прописные и строчные буквы по f.</span><span class="sxs-lookup"><span data-stu-id="7ebb5-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="7ebb5-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="7ebb5-116">_pb_</span></span>
  
> <span data-ttu-id="7ebb5-117">[out] Указатель на возвращаемый двоичное число.</span><span class="sxs-lookup"><span data-stu-id="7ebb5-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="7ebb5-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="7ebb5-118">_cb_</span></span>
  
> <span data-ttu-id="7ebb5-119">[in] Размер, в байтах, параметр _pb_ .</span><span class="sxs-lookup"><span data-stu-id="7ebb5-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7ebb5-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ebb5-120">Return value</span></span>

<span data-ttu-id="7ebb5-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="7ebb5-121">S_OK</span></span>
  
> <span data-ttu-id="7ebb5-122">Преобразование прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="7ebb5-122">Conversion was successful.</span></span>
    
<span data-ttu-id="7ebb5-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="7ebb5-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="7ebb5-124">Обнаружены недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="7ebb5-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ebb5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7ebb5-125">See also</span></span>



[<span data-ttu-id="7ebb5-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="7ebb5-126">FBinFromHex</span></span>](fbinfromhex.md)

