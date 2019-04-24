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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357500"
---
# <a name="scbinfromhexbounded"></a><span data-ttu-id="178a8-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="178a8-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="178a8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="178a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="178a8-105">Преобразует заданную часть строкового представления шестнадцатеричного числа в двоичное число.</span><span class="sxs-lookup"><span data-stu-id="178a8-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="178a8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="178a8-106">Header file:</span></span>  <br/> |<span data-ttu-id="178a8-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="178a8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="178a8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="178a8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="178a8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="178a8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="178a8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="178a8-110">Called by:</span></span>  <br/> |<span data-ttu-id="178a8-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="178a8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="178a8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="178a8-112">Parameters</span></span>

 <span data-ttu-id="178a8-113">_СЗ_</span><span class="sxs-lookup"><span data-stu-id="178a8-113">_sz_</span></span>
  
> <span data-ttu-id="178a8-114">возврата Указатель на преобразуемую строку, заканчивающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="178a8-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="178a8-115">Допустимыми символами являются шестнадцатеричные символы от 0 до 9, а как прописные, так и строчные буквы от a до f.</span><span class="sxs-lookup"><span data-stu-id="178a8-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="178a8-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="178a8-116">_pb_</span></span>
  
> <span data-ttu-id="178a8-117">вышли Указатель на возвращаемое двоичное число.</span><span class="sxs-lookup"><span data-stu-id="178a8-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="178a8-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="178a8-118">_cb_</span></span>
  
> <span data-ttu-id="178a8-119">возврата Размер (в байтах) параметра _Pb_ .</span><span class="sxs-lookup"><span data-stu-id="178a8-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="178a8-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="178a8-120">Return value</span></span>

<span data-ttu-id="178a8-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="178a8-121">S_OK</span></span>
  
> <span data-ttu-id="178a8-122">Преобразование выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="178a8-122">Conversion was successful.</span></span>
    
<span data-ttu-id="178a8-123">МАПИ_Е_КАЛЛ_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="178a8-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="178a8-124">Обнаружены неДопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="178a8-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="178a8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="178a8-125">See also</span></span>



[<span data-ttu-id="178a8-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="178a8-126">FBinFromHex</span></span>](fbinfromhex.md)

