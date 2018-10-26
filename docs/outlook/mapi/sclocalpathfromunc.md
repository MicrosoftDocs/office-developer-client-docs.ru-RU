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
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594420"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="9f910-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="9f910-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="9f910-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f910-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f910-105">Находит аналог локальный путь для указанного универсальных имен пути (UNC).</span><span class="sxs-lookup"><span data-stu-id="9f910-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f910-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9f910-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f910-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9f910-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9f910-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9f910-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f910-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f910-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f910-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9f910-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f910-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="9f910-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="9f910-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f910-112">Parameters</span></span>

 <span data-ttu-id="9f910-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="9f910-113">_szUNC_</span></span>
  
> <span data-ttu-id="9f910-114">[in] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] файла или папки.</span><span class="sxs-lookup"><span data-stu-id="9f910-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="9f910-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="9f910-115">_szLocal_</span></span>
  
> <span data-ttu-id="9f910-116">[out] Путь в формате [ _диск:_]\[ _путь_] одного файла или папки и для параметра _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="9f910-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="9f910-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="9f910-117">_cchLocal_</span></span>
  
> <span data-ttu-id="9f910-118">[in] Размер буфера для вывода строки.</span><span class="sxs-lookup"><span data-stu-id="9f910-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f910-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f910-119">Return value</span></span>

<span data-ttu-id="9f910-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f910-120">S_OK</span></span>
  
> <span data-ttu-id="9f910-121">Локальный путь был найден.</span><span class="sxs-lookup"><span data-stu-id="9f910-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="9f910-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="9f910-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="9f910-123">_szLocal_ не достаточно для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="9f910-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="9f910-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9f910-124">S_FALSE</span></span>
  
> <span data-ttu-id="9f910-125">Строка UNC уже локальный путь.</span><span class="sxs-lookup"><span data-stu-id="9f910-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="9f910-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9f910-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="9f910-127">Локальный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="9f910-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f910-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9f910-128">See also</span></span>



[<span data-ttu-id="9f910-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="9f910-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

