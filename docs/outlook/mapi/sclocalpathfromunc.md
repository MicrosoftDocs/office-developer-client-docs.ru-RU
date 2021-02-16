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
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432235"
---
# <a name="sclocalpathfromunc"></a><span data-ttu-id="9f134-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="9f134-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="9f134-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f134-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f134-105">Находит локальный путь, аналог заданного UNC-пути.</span><span class="sxs-lookup"><span data-stu-id="9f134-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9f134-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9f134-106">Header file:</span></span>  <br/> |<span data-ttu-id="9f134-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9f134-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9f134-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9f134-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9f134-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9f134-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9f134-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9f134-110">Called by:</span></span>  <br/> |<span data-ttu-id="9f134-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9f134-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="9f134-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f134-112">Parameters</span></span>

 <span data-ttu-id="9f134-113">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="9f134-113">_szUNC_</span></span>
  
> <span data-ttu-id="9f134-114">[in] Путь в формате [ сервер ] путь ] файла \\  \[ или \[ каталога.</span><span class="sxs-lookup"><span data-stu-id="9f134-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="9f134-115">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="9f134-115">_szLocal_</span></span>
  
> <span data-ttu-id="9f134-116">[out] Путь в формате [ _диск:_ путь ] того же файла или каталога, что и для параметра \[  _szUNC._</span><span class="sxs-lookup"><span data-stu-id="9f134-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="9f134-117">_cchLocal_</span><span class="sxs-lookup"><span data-stu-id="9f134-117">_cchLocal_</span></span>
  
> <span data-ttu-id="9f134-118">[in] Размер буфера для строки вывода.</span><span class="sxs-lookup"><span data-stu-id="9f134-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9f134-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f134-119">Return value</span></span>

<span data-ttu-id="9f134-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f134-120">S_OK</span></span>
  
> <span data-ttu-id="9f134-121">Локальный путь успешно расположен.</span><span class="sxs-lookup"><span data-stu-id="9f134-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="9f134-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="9f134-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="9f134-123">_szLocal_ не был достаточно большим для удержания результата.</span><span class="sxs-lookup"><span data-stu-id="9f134-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="9f134-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="9f134-124">S_FALSE</span></span>
  
> <span data-ttu-id="9f134-125">Строка UNC уже была локальным путем.</span><span class="sxs-lookup"><span data-stu-id="9f134-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="9f134-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9f134-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="9f134-127">Локальный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="9f134-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f134-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9f134-128">See also</span></span>



[<span data-ttu-id="9f134-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="9f134-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

