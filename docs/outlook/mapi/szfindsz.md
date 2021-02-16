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
# <a name="szfindsz"></a><span data-ttu-id="2159a-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="2159a-103">SzFindSz</span></span>

  
  
<span data-ttu-id="2159a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2159a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2159a-105">Находит первый вхождение подстроки с завершенным нулом в строке с нулью.</span><span class="sxs-lookup"><span data-stu-id="2159a-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2159a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2159a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2159a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2159a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2159a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2159a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2159a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2159a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2159a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2159a-110">Called by:</span></span>  <br/> |<span data-ttu-id="2159a-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2159a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="2159a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2159a-112">Parameters</span></span>

 <span data-ttu-id="2159a-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="2159a-113">_lpsz_</span></span>
  
> <span data-ttu-id="2159a-114">[in] Указатель на строку, о конце null для поиска.</span><span class="sxs-lookup"><span data-stu-id="2159a-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="2159a-115">Параметр  _lpsz_ не должен превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="2159a-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="2159a-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="2159a-116">_lpszKey_</span></span>
  
> <span data-ttu-id="2159a-117">[in] Указатель на подстроку, одернутую нулом, для поиска.</span><span class="sxs-lookup"><span data-stu-id="2159a-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="2159a-118">Параметр  _lpszKey не должен_ превышать 65536 символов.</span><span class="sxs-lookup"><span data-stu-id="2159a-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2159a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2159a-119">Return value</span></span>

 <span data-ttu-id="2159a-120">**SzFindSz** возвращает указатель на первый символ первого вхождения подстроки в строке.</span><span class="sxs-lookup"><span data-stu-id="2159a-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="2159a-121">Если подстрока не возникает ни в одной строке, если  _lpszKey_ больше  _lpsz,_ или если любой из параметров имеет значение NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="2159a-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2159a-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="2159a-122">Remarks</span></span>

<span data-ttu-id="2159a-123">Функция **SzFindSz** ищет только точное совпадение; он чувствителен к различиям в диакритических и диакритических диакритах.</span><span class="sxs-lookup"><span data-stu-id="2159a-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="2159a-124">Поиск в форматах Юникод и DBCS поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2159a-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="2159a-125">Ограничение длины для обоих параметров — в символах, а не вбайтах.</span><span class="sxs-lookup"><span data-stu-id="2159a-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

