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
# <a name="sclocalpathfromunc"></a><span data-ttu-id="e2cbf-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="e2cbf-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="e2cbf-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2cbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2cbf-105">Находит аналог локальный путь для указанного универсальных имен пути (UNC).</span><span class="sxs-lookup"><span data-stu-id="e2cbf-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2cbf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e2cbf-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2cbf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e2cbf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e2cbf-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e2cbf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2cbf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2cbf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2cbf-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e2cbf-110">Called by:</span></span>  <br/> |<span data-ttu-id="e2cbf-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="e2cbf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="e2cbf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2cbf-112">Parameters</span></span>

 <span data-ttu-id="e2cbf-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="e2cbf-113">_szUNC_</span></span>
  
> <span data-ttu-id="e2cbf-114">[in] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] файла или папки.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="e2cbf-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="e2cbf-115">_szLocal_</span></span>
  
> <span data-ttu-id="e2cbf-116">[out] Путь в формате [ _диск:_]\[ _путь_] одного файла или папки и для параметра _szUNC_ .</span><span class="sxs-lookup"><span data-stu-id="e2cbf-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="e2cbf-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="e2cbf-117">_cchLocal_</span></span>
  
> <span data-ttu-id="e2cbf-118">[in] Размер буфера для вывода строки.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2cbf-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="e2cbf-119">Return value</span></span>

<span data-ttu-id="e2cbf-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="e2cbf-120">S_OK</span></span>
  
> <span data-ttu-id="e2cbf-121">Локальный путь был найден.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="e2cbf-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="e2cbf-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="e2cbf-123">_szLocal_ не достаточно для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="e2cbf-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e2cbf-124">S_FALSE</span></span>
  
> <span data-ttu-id="e2cbf-125">Строка UNC уже локальный путь.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="e2cbf-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="e2cbf-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="e2cbf-127">Локальный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="e2cbf-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2cbf-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e2cbf-128">See also</span></span>



[<span data-ttu-id="e2cbf-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="e2cbf-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

