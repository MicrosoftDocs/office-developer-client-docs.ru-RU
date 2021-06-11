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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435224"
---
# <a name="szfindsz"></a><span data-ttu-id="9ebf9-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="9ebf9-103">SzFindSz</span></span>

  
  
<span data-ttu-id="9ebf9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ebf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ebf9-105">Находит первое возникновение подстройки null-terminated в строке null-terminated.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ebf9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9ebf9-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ebf9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9ebf9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9ebf9-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9ebf9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9ebf9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9ebf9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9ebf9-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9ebf9-110">Called by:</span></span>  <br/> |<span data-ttu-id="9ebf9-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="9ebf9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="9ebf9-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="9ebf9-112">Parameters</span></span>

 <span data-ttu-id="9ebf9-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="9ebf9-113">_lpsz_</span></span>
  
> <span data-ttu-id="9ebf9-114">[in] Указатель на строку null-terminated, которая будет искаться.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="9ebf9-115">Параметр  _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="9ebf9-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="9ebf9-116">_lpszKey_</span></span>
  
> <span data-ttu-id="9ebf9-117">[in] Указатель на подстройку с недействимой, для поиска.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="9ebf9-118">Параметр  _lpszKey_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ebf9-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ebf9-119">Return value</span></span>

 <span data-ttu-id="9ebf9-120">**SzFindSz** возвращает указатель на первый символ первого появления подстройки в строке.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="9ebf9-121">Если подстройка не возникает нигде в строке, если  _размер lpszKey_ превышает  _lpsz,_ или если любой параметр NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9ebf9-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ebf9-122">Remarks</span></span>

<span data-ttu-id="9ebf9-123">Функция **SzFindSz** ищет только точный совпадение; он чувствителен к различиям в случае и диакритических различиях.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="9ebf9-124">Поддерживаются поиски в форматах Unicode и DBCS.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="9ebf9-125">Ограничение длины для обоих параметров имеется в символах, а не обязательно в bytes.</span><span class="sxs-lookup"><span data-stu-id="9ebf9-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

