---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812226"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="aa97d-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="aa97d-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="aa97d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa97d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa97d-105">Находит универсальных имен соглашение (UNC) путь эквивалента данного локальный путь.</span><span class="sxs-lookup"><span data-stu-id="aa97d-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa97d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="aa97d-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa97d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa97d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="aa97d-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="aa97d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa97d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="aa97d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="aa97d-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="aa97d-110">Called by:</span></span>  <br/> |<span data-ttu-id="aa97d-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="aa97d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="aa97d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa97d-112">Parameters</span></span>

 <span data-ttu-id="aa97d-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="aa97d-113">_szLocal_</span></span>
  
> <span data-ttu-id="aa97d-114">[in] Путь в формате [ _диск:_]\[ _путь_] файла или папки.</span><span class="sxs-lookup"><span data-stu-id="aa97d-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="aa97d-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="aa97d-115">_szUNC_</span></span>
  
> <span data-ttu-id="aa97d-116">[out] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] одного файла или папки и для параметра _szLocal_ .</span><span class="sxs-lookup"><span data-stu-id="aa97d-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="aa97d-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="aa97d-117">_cchUNC_</span></span>
  
> <span data-ttu-id="aa97d-118">[in] Размер буфера для вывода строки.</span><span class="sxs-lookup"><span data-stu-id="aa97d-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aa97d-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="aa97d-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="aa97d-120">S_OK</span></span>
  
> <span data-ttu-id="aa97d-121">Аналог путь UNC был найден.</span><span class="sxs-lookup"><span data-stu-id="aa97d-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="aa97d-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa97d-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="aa97d-123">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="aa97d-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="aa97d-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="aa97d-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="aa97d-125">_szUNC_ не достаточно для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="aa97d-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="aa97d-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="aa97d-126">S_FALSE</span></span>
  
> <span data-ttu-id="aa97d-127">Локальный путь уже была строка UNC.</span><span class="sxs-lookup"><span data-stu-id="aa97d-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa97d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="aa97d-128">See also</span></span>



[<span data-ttu-id="aa97d-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="aa97d-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

