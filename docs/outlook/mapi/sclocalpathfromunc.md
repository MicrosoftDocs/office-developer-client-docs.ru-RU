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
# <a name="sclocalpathfromunc"></a><span data-ttu-id="4747a-103">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="4747a-103">ScLocalPathFromUNC</span></span>

  
  
<span data-ttu-id="4747a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4747a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4747a-105">Определяет путь к локальному пути к указанному UNC-пути.</span><span class="sxs-lookup"><span data-stu-id="4747a-105">Locates a local path counterpart to the given universal naming convention (UNC) path.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4747a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4747a-106">Header file:</span></span>  <br/> |<span data-ttu-id="4747a-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="4747a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4747a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4747a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4747a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4747a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4747a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4747a-110">Called by:</span></span>  <br/> |<span data-ttu-id="4747a-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="4747a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a><span data-ttu-id="4747a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4747a-112">Parameters</span></span>

 <span data-ttu-id="4747a-113">_сзунк_</span><span class="sxs-lookup"><span data-stu-id="4747a-113">_szUNC_</span></span>
  
> <span data-ttu-id="4747a-114">возврата Путь в \\формате [ _Server_]\[ _Share_\[ ] _путь_] файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="4747a-114">[in] A path in the format \\[ _server_]\[ _share_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="4747a-115">_сзлокал_</span><span class="sxs-lookup"><span data-stu-id="4747a-115">_szLocal_</span></span>
  
> <span data-ttu-id="4747a-116">вышли Путь в формате [ _диск:_]\[ _путь_] того же файла или каталога, что и для параметра _сзунк_ .</span><span class="sxs-lookup"><span data-stu-id="4747a-116">[out] A path in the format [ _drive:_]\[ _path_] of the same file or directory as for the  _szUNC_ parameter.</span></span> 
    
 <span data-ttu-id="4747a-117">_кчлокал_</span><span class="sxs-lookup"><span data-stu-id="4747a-117">_cchLocal_</span></span>
  
> <span data-ttu-id="4747a-118">возврата Размер буфера для выходной строки.</span><span class="sxs-lookup"><span data-stu-id="4747a-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4747a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4747a-119">Return value</span></span>

<span data-ttu-id="4747a-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="4747a-120">S_OK</span></span>
  
> <span data-ttu-id="4747a-121">Локальный путь успешно найден.</span><span class="sxs-lookup"><span data-stu-id="4747a-121">A local path was successfully located.</span></span>
    
<span data-ttu-id="4747a-122">MAPI_E_TOO_BIG</span><span class="sxs-lookup"><span data-stu-id="4747a-122">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="4747a-123">_сзлокал_ недостаточно велик для хранения результата.</span><span class="sxs-lookup"><span data-stu-id="4747a-123">_szLocal_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="4747a-124">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="4747a-124">S_FALSE</span></span>
  
> <span data-ttu-id="4747a-125">Строка UNC уже является локальным путем.</span><span class="sxs-lookup"><span data-stu-id="4747a-125">The UNC string was already a local path.</span></span>
    
<span data-ttu-id="4747a-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="4747a-126">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="4747a-127">Локальный путь не найден.</span><span class="sxs-lookup"><span data-stu-id="4747a-127">A local path was not found.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4747a-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4747a-128">See also</span></span>



[<span data-ttu-id="4747a-129">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="4747a-129">ScUNCFromLocalPath</span></span>](scuncfromlocalpath.md)

