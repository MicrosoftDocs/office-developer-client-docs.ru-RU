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
# <a name="scbinfromhexbounded"></a><span data-ttu-id="21a2f-103">ScBinFromHexBounded</span><span class="sxs-lookup"><span data-stu-id="21a2f-103">ScBinFromHexBounded</span></span>

  
  
<span data-ttu-id="21a2f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21a2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21a2f-105">Преобразует указанную часть строки представления гексадецимального номера в двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="21a2f-105">Converts the specified portion of a string representation of a hexadecimal number into a binary number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="21a2f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="21a2f-106">Header file:</span></span>  <br/> |<span data-ttu-id="21a2f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="21a2f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="21a2f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="21a2f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="21a2f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="21a2f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="21a2f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="21a2f-110">Called by:</span></span>  <br/> |<span data-ttu-id="21a2f-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="21a2f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a><span data-ttu-id="21a2f-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="21a2f-112">Parameters</span></span>

 <span data-ttu-id="21a2f-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="21a2f-113">_sz_</span></span>
  
> <span data-ttu-id="21a2f-114">[in] Указатель на завершаемую строку null, которая должна быть преобразована.</span><span class="sxs-lookup"><span data-stu-id="21a2f-114">[in] Pointer to the null-terminated string to be converted.</span></span> <span data-ttu-id="21a2f-115">Допустимые символы включают гексадецимальные символы от 0 до 9, а также символы верхнего и нижнего регистра с помощью f.</span><span class="sxs-lookup"><span data-stu-id="21a2f-115">Valid characters include the hexadecimal characters 0 through 9 and both uppercase and lowercase characters a through f.</span></span>
    
 <span data-ttu-id="21a2f-116">_pb_</span><span class="sxs-lookup"><span data-stu-id="21a2f-116">_pb_</span></span>
  
> <span data-ttu-id="21a2f-117">[вышел] Указатель на возвращенный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="21a2f-117">[out] Pointer to the returned binary number.</span></span>
    
 <span data-ttu-id="21a2f-118">_cb_</span><span class="sxs-lookup"><span data-stu-id="21a2f-118">_cb_</span></span>
  
> <span data-ttu-id="21a2f-119">[in] Размер в bytes _параметра pb._</span><span class="sxs-lookup"><span data-stu-id="21a2f-119">[in] Size, in bytes, of the  _pb_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="21a2f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21a2f-120">Return value</span></span>

<span data-ttu-id="21a2f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="21a2f-121">S_OK</span></span>
  
> <span data-ttu-id="21a2f-122">Преобразование было успешным.</span><span class="sxs-lookup"><span data-stu-id="21a2f-122">Conversion was successful.</span></span>
    
<span data-ttu-id="21a2f-123">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="21a2f-123">MAPI_E_CALL_FAILED</span></span>
  
> <span data-ttu-id="21a2f-124">Были встречены недействительные символы.</span><span class="sxs-lookup"><span data-stu-id="21a2f-124">Invalid characters were encountered.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21a2f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="21a2f-125">See also</span></span>



[<span data-ttu-id="21a2f-126">FBinFromHex</span><span class="sxs-lookup"><span data-stu-id="21a2f-126">FBinFromHex</span></span>](fbinfromhex.md)

