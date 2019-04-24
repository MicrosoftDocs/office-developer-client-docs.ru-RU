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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358774"
---
# <a name="scuncfromlocalpath"></a><span data-ttu-id="b0d57-103">ScUNCFromLocalPath</span><span class="sxs-lookup"><span data-stu-id="b0d57-103">ScUNCFromLocalPath</span></span>

  
  
<span data-ttu-id="b0d57-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0d57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0d57-105">Определяет путь в формате UNC к заданному локальному пути.</span><span class="sxs-lookup"><span data-stu-id="b0d57-105">Locates a universal naming convention (UNC) path counterpart to the given local path.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0d57-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b0d57-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0d57-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="b0d57-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b0d57-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b0d57-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0d57-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d57-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b0d57-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b0d57-110">Called by:</span></span>  <br/> |<span data-ttu-id="b0d57-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b0d57-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a><span data-ttu-id="b0d57-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0d57-112">Parameters</span></span>

 <span data-ttu-id="b0d57-113">_Сзлокал_</span><span class="sxs-lookup"><span data-stu-id="b0d57-113">_szLocal_</span></span>
  
> <span data-ttu-id="b0d57-114">возврата Путь в формате [ _диск:_]\[ _путь_] файла или каталога.</span><span class="sxs-lookup"><span data-stu-id="b0d57-114">[in] A path in the format [ _drive:_]\[ _path_] of a file or directory.</span></span>
    
 <span data-ttu-id="b0d57-115">_Сзунк_</span><span class="sxs-lookup"><span data-stu-id="b0d57-115">_szUNC_</span></span>
  
> <span data-ttu-id="b0d57-116">вышли \\Путь в формате [ _Server_]\[ _Общий_\[ _путь] к_тому же файлу или каталогу, что и для параметра _сзлокал_ .</span><span class="sxs-lookup"><span data-stu-id="b0d57-116">[out] A path in the format \\[ _server_]\[ _share_]\[ _path_] of the same file or directory as for the  _szLocal_ parameter.</span></span> 
    
 <span data-ttu-id="b0d57-117">_Кчунк_</span><span class="sxs-lookup"><span data-stu-id="b0d57-117">_cchUNC_</span></span>
  
> <span data-ttu-id="b0d57-118">возврата Размер буфера для выходной строки.</span><span class="sxs-lookup"><span data-stu-id="b0d57-118">[in] Size of the buffer for the output string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b0d57-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0d57-119">Return value</span></span>

<span data-ttu-id="b0d57-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0d57-120">S_OK</span></span>
  
> <span data-ttu-id="b0d57-121">Аналогичный UNC-путь был успешно найден.</span><span class="sxs-lookup"><span data-stu-id="b0d57-121">The UNC path counterpart was successfully located.</span></span>
    
<span data-ttu-id="b0d57-122">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="b0d57-122">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="b0d57-123">Один или несколько параметров являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="b0d57-123">One or more parameters are invalid.</span></span>
    
<span data-ttu-id="b0d57-124">МАПИ_Е_ТУ_БИГ</span><span class="sxs-lookup"><span data-stu-id="b0d57-124">MAPI_E_TOO_BIG</span></span>
  
>  <span data-ttu-id="b0d57-125">_сзунк_ недостаточно велик для хранения результата.</span><span class="sxs-lookup"><span data-stu-id="b0d57-125">_szUNC_ was not large enough to hold the result.</span></span> 
    
<span data-ttu-id="b0d57-126">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b0d57-126">S_FALSE</span></span>
  
> <span data-ttu-id="b0d57-127">Локальный путь уже является строкой UNC.</span><span class="sxs-lookup"><span data-stu-id="b0d57-127">The local path was already a UNC string.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0d57-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b0d57-128">See also</span></span>



[<span data-ttu-id="b0d57-129">ScLocalPathFromUNC</span><span class="sxs-lookup"><span data-stu-id="b0d57-129">ScLocalPathFromUNC</span></span>](sclocalpathfromunc.md)

