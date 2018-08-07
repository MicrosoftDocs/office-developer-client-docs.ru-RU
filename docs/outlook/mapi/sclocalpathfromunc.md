---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812210"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="01c49-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="01c49-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="01c49-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01c49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01c49-105">Находит аналог локальный путь для указанного универсальных имен пути (UNC).</span><span class="sxs-lookup"><span data-stu-id="01c49-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01c49-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="01c49-106">Header file:</span></span>  <br/> |<span data-ttu-id="01c49-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01c49-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01c49-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="01c49-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01c49-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01c49-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01c49-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="01c49-110">Called by:</span></span>  <br/> |<span data-ttu-id="01c49-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="01c49-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="01c49-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="01c49-112">Parameters</span></span>

 <span data-ttu-id="01c49-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="01c49-113">_szUNC_</span></span>
  
> <span data-ttu-id="01c49-114">[in] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] файла или папки.</span><span class="sxs-lookup"><span data-stu-id="01c49-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="01c49-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="01c49-115">_szLocal_</span></span>
  
> <span data-ttu-id="01c49-116">[out] Путь в формате [ _диск:_]\[ _путь_] одного файла или папки и для параметра _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="01c49-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="01c49-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="01c49-117">_cchLocal_</span></span>
  
> <span data-ttu-id="01c49-118">[in] Размер буфера для вывода строки.</span><span class="sxs-lookup"><span data-stu-id="01c49-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="01c49-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="01c49-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="01c49-120">S_OK</span></span>
  
> <span data-ttu-id="01c49-121">Локальный путь был найден.</span><span class="sxs-lookup"><span data-stu-id="01c49-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="01c49-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="01c49-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="01c49-123">_szLocal_ не достаточно для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="01c49-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="01c49-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="01c49-124">S_FALSE</span></span>
  
> <span data-ttu-id="01c49-125">Строка UNC уже локальный путь.</span><span class="sxs-lookup"><span data-stu-id="01c49-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="01c49-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="01c49-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="01c49-127">Локальный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="01c49-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01c49-128">См. также</span><span class="sxs-lookup"><span data-stu-id="01c49-128">See also</span></span>



[<span data-ttu-id="01c49-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="01c49-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

