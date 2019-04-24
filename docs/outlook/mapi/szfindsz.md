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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345747"
---
# <a name="szfindsz"></a><span data-ttu-id="c53ca-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="c53ca-103">SzFindSz</span></span>

  
  
<span data-ttu-id="c53ca-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c53ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c53ca-105">Ищет первое вхождение подстроки с завершающим нулем в строке с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="c53ca-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c53ca-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c53ca-106">Header file:</span></span>  <br/> |<span data-ttu-id="c53ca-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="c53ca-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c53ca-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c53ca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c53ca-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c53ca-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c53ca-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c53ca-110">Called by:</span></span>  <br/> |<span data-ttu-id="c53ca-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c53ca-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="c53ca-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c53ca-112">Parameters</span></span>

 <span data-ttu-id="c53ca-113">_лпсз_</span><span class="sxs-lookup"><span data-stu-id="c53ca-113">_lpsz_</span></span>
  
> <span data-ttu-id="c53ca-114">возврата Указатель на строку с завершающим нулем для поиска.</span><span class="sxs-lookup"><span data-stu-id="c53ca-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="c53ca-115">Значение параметра _лпсз_ не должно превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="c53ca-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="c53ca-116">_Лпсзкэй_</span><span class="sxs-lookup"><span data-stu-id="c53ca-116">_lpszKey_</span></span>
  
> <span data-ttu-id="c53ca-117">возврата Указатель на подстроку, заканчивающуюся нулем, для поиска.</span><span class="sxs-lookup"><span data-stu-id="c53ca-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="c53ca-118">Значение параметра _лпсзкэй_ не должно превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="c53ca-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c53ca-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c53ca-119">Return value</span></span>

 <span data-ttu-id="c53ca-120">**Сзфиндсз** возвращает указатель на первый символ первого вхождения подстроки в строке.</span><span class="sxs-lookup"><span data-stu-id="c53ca-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="c53ca-121">Если подстрока нет в любом месте строки, если _лпсзкэй_ больше, чем _лпсз_, или если любой из этих параметров равен NULL, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="c53ca-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c53ca-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c53ca-122">Remarks</span></span>

<span data-ttu-id="c53ca-123">Функция **сзфиндсз** выполняет поиск только точного совпадения; Это зависит от регистра и диакритических различий.</span><span class="sxs-lookup"><span data-stu-id="c53ca-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="c53ca-124">Поисковые запросы поддерживаются в форматах Юникод и DBCS.</span><span class="sxs-lookup"><span data-stu-id="c53ca-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="c53ca-125">Длина обоих параметров ограничена символами, а не обязательно байтами.</span><span class="sxs-lookup"><span data-stu-id="c53ca-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

