---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812455"
---
# <a name="szfindsz"></a><span data-ttu-id="90253-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="90253-103">SzFindSz</span></span>

  
  
<span data-ttu-id="90253-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90253-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90253-105">Поиск первого вхождения подстроки символом null в строку символом null.</span><span class="sxs-lookup"><span data-stu-id="90253-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="90253-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="90253-106">Header file:</span></span>  <br/> |<span data-ttu-id="90253-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="90253-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="90253-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="90253-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="90253-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="90253-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="90253-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="90253-110">Called by:</span></span>  <br/> |<span data-ttu-id="90253-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="90253-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="90253-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="90253-112">Parameters</span></span>

 <span data-ttu-id="90253-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="90253-113">_lpsz_</span></span>
  
> <span data-ttu-id="90253-114">[in] Указатель на строку символом null для поиска.</span><span class="sxs-lookup"><span data-stu-id="90253-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="90253-115">Параметр _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="90253-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="90253-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="90253-116">_lpszKey_</span></span>
  
> <span data-ttu-id="90253-117">[in] Указатель на подстроки символом null для поиска.</span><span class="sxs-lookup"><span data-stu-id="90253-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="90253-118">Параметр _lpszKey_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="90253-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="90253-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

 <span data-ttu-id="90253-120">**SzFindSz** возвращает указатель на первый символ первого вхождения подстроки в строке.</span><span class="sxs-lookup"><span data-stu-id="90253-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="90253-121">Если подстрока не происходит в строке, в любом месте, если _lpszKey_ больше, чем _lpsz_или один из параметров имеет значение NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="90253-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90253-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="90253-122">Remarks</span></span>

<span data-ttu-id="90253-123">Функция **SzFindSz** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия.</span><span class="sxs-lookup"><span data-stu-id="90253-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="90253-124">Поиск в форматах Юникод и DBCS поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="90253-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="90253-125">Ограничение длины на оба параметра — в символы, не обязательно в байтах.</span><span class="sxs-lookup"><span data-stu-id="90253-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

