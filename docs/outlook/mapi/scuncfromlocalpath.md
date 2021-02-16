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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414538"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="26778-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="26778-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="26778-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26778-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26778-105">Находит аналог UNC-пути для данного локального пути.</span><span class="sxs-lookup"><span data-stu-id="26778-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="26778-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="26778-106">Header file:</span></span>  <br/> |<span data-ttu-id="26778-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="26778-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="26778-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="26778-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="26778-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="26778-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="26778-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="26778-110">Called by:</span></span>  <br/> |<span data-ttu-id="26778-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="26778-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="26778-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="26778-112">Parameters</span></span>

 <span data-ttu-id="26778-113">_szLocal_</span><span class="sxs-lookup"><span data-stu-id="26778-113">_szLocal_</span></span>
  
> <span data-ttu-id="26778-114">[in] Путь в формате [ _диск:_ путь ] файла \[ или каталога.</span><span class="sxs-lookup"><span data-stu-id="26778-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="26778-115">_szUNC_</span><span class="sxs-lookup"><span data-stu-id="26778-115">_szUNC_</span></span>
  
> <span data-ttu-id="26778-116">[out] Путь в формате [ сервер ] путь ] того же файла или каталога, что и для \\  \[  \[  _параметра szLocal._</span><span class="sxs-lookup"><span data-stu-id="26778-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="26778-117">_cchUNC_</span><span class="sxs-lookup"><span data-stu-id="26778-117">_cchUNC_</span></span>
  
> <span data-ttu-id="26778-118">[in] Размер буфера для строки вывода.</span><span class="sxs-lookup"><span data-stu-id="26778-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26778-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26778-119">Return value</span></span>

<span data-ttu-id="26778-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="26778-120">S_OK</span></span>
  
> <span data-ttu-id="26778-121">Аналог UNC-пути успешно расположен.</span><span class="sxs-lookup"><span data-stu-id="26778-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="26778-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="26778-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="26778-123">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="26778-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="26778-124">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="26778-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="26778-125">_SzUNC_ не был достаточно большим для удержания результата.</span><span class="sxs-lookup"><span data-stu-id="26778-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="26778-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="26778-126">S_FALSE</span></span>
  
> <span data-ttu-id="26778-127">Локальный путь уже был строкой UNC.</span><span class="sxs-lookup"><span data-stu-id="26778-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26778-128">См. также</span><span class="sxs-lookup"><span data-stu-id="26778-128">See also</span></span>



[<span data-ttu-id="26778-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="26778-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

