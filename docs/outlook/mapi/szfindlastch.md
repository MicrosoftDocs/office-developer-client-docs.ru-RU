---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345138"
---
# <a name="szfindlastch"></a><span data-ttu-id="0c314-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="0c314-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="0c314-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c314-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c314-105">Ищет последнее вхождение символа в строке с завершающим нулем.</span><span class="sxs-lookup"><span data-stu-id="0c314-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c314-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0c314-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c314-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0c314-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0c314-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0c314-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c314-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0c314-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0c314-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0c314-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c314-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="0c314-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="0c314-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c314-112">Parameters</span></span>

 <span data-ttu-id="0c314-113">_лпсз_</span><span class="sxs-lookup"><span data-stu-id="0c314-113">_lpsz_</span></span>
  
> <span data-ttu-id="0c314-114">возврата Указатель на строку с завершающим нулем для поиска.</span><span class="sxs-lookup"><span data-stu-id="0c314-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="0c314-115">_CH_</span><span class="sxs-lookup"><span data-stu-id="0c314-115">_ch_</span></span>
  
> <span data-ttu-id="0c314-116">возврата Символ, для которого необходимо выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="0c314-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c314-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c314-117">Return value</span></span>

 <span data-ttu-id="0c314-118">**Сзфиндластч** возвращает указатель на последнее вхождение символа в строке.</span><span class="sxs-lookup"><span data-stu-id="0c314-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="0c314-119">Если символ не встречается в строке или параметр _лпсз_ имеет значение null, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="0c314-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0c314-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c314-120">Remarks</span></span>

<span data-ttu-id="0c314-121">Функция **сзфиндластч** выполняет поиск только точного совпадения; Это зависит от регистра и диакритических различий.</span><span class="sxs-lookup"><span data-stu-id="0c314-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="0c314-122">Поисковые запросы поддерживаются в форматах Юникод и DBCS.</span><span class="sxs-lookup"><span data-stu-id="0c314-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

