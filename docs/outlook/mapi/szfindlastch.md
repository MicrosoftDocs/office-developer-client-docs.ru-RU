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
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812453"
---
# <a name="szfindlastch"></a><span data-ttu-id="2a222-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="2a222-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="2a222-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a222-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a222-105">Выполняет поиск последнего вхождения знака в string символом null.</span><span class="sxs-lookup"><span data-stu-id="2a222-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a222-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2a222-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a222-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2a222-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2a222-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="2a222-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a222-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a222-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a222-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="2a222-110">Called by:</span></span>  <br/> |<span data-ttu-id="2a222-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="2a222-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="2a222-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a222-112">Parameters</span></span>

 <span data-ttu-id="2a222-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="2a222-113">_lpsz_</span></span>
  
> <span data-ttu-id="2a222-114">[in] Указатель на строку символом null для поиска.</span><span class="sxs-lookup"><span data-stu-id="2a222-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="2a222-115">_Кан_</span><span class="sxs-lookup"><span data-stu-id="2a222-115">_ch_</span></span>
  
> <span data-ttu-id="2a222-116">[in] Знак для поиска.</span><span class="sxs-lookup"><span data-stu-id="2a222-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2a222-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

 <span data-ttu-id="2a222-118">**SzFindLastCh** возвращает указатель на последнего вхождения знаков в строке.</span><span class="sxs-lookup"><span data-stu-id="2a222-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="2a222-119">Если кодировка не происходит в любом месте в строке или параметр _lpsz_ имеет значение NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="2a222-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2a222-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="2a222-120">Remarks</span></span>

<span data-ttu-id="2a222-121">Функция **SzFindLastCh** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия.</span><span class="sxs-lookup"><span data-stu-id="2a222-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="2a222-122">Поиск в формате Юникод и DBCS поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2a222-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

