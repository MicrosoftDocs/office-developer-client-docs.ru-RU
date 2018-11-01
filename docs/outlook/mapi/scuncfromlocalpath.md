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
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590108"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="d575a-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="d575a-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="d575a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d575a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d575a-105">Находит универсальных имен соглашение (UNC) путь эквивалента данного локальный путь.</span><span class="sxs-lookup"><span data-stu-id="d575a-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d575a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d575a-106">Header file:</span></span>  <br/> |<span data-ttu-id="d575a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d575a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d575a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d575a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d575a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d575a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d575a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d575a-110">Called by:</span></span>  <br/> |<span data-ttu-id="d575a-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="d575a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="d575a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d575a-112">Parameters</span></span>

 <span data-ttu-id="d575a-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="d575a-113">_szLocal_</span></span>
  
> <span data-ttu-id="d575a-114">[in] Путь в формате [ _диск:_]\[ _путь_] файла или папки.</span><span class="sxs-lookup"><span data-stu-id="d575a-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="d575a-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="d575a-115">_szUNC_</span></span>
  
> <span data-ttu-id="d575a-116">[out] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] одного файла или папки и для параметра _szLocal_ .</span><span class="sxs-lookup"><span data-stu-id="d575a-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="d575a-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="d575a-117">_cchUNC_</span></span>
  
> <span data-ttu-id="d575a-118">[in] Размер буфера для вывода строки.</span><span class="sxs-lookup"><span data-stu-id="d575a-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d575a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d575a-119">Return value</span></span>

<span data-ttu-id="d575a-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d575a-120">S_OK</span></span>
  
> <span data-ttu-id="d575a-121">Аналог путь UNC был найден.</span><span class="sxs-lookup"><span data-stu-id="d575a-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="d575a-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d575a-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d575a-123">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="d575a-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="d575a-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="d575a-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="d575a-125">_szUNC_ не достаточно для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="d575a-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="d575a-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d575a-126">S_FALSE</span></span>
  
> <span data-ttu-id="d575a-127">Локальный путь уже была строка UNC.</span><span class="sxs-lookup"><span data-stu-id="d575a-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d575a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d575a-128">See also</span></span>



[<span data-ttu-id="d575a-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="d575a-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

