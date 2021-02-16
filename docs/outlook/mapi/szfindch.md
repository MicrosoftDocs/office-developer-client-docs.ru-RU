---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421944"
---
# <a name="szfindch"></a><span data-ttu-id="a90c7-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="a90c7-103">SzFindCh</span></span>
 
<span data-ttu-id="a90c7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a90c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a90c7-105">Выполняет поиск первого вхождения символа в строке с нулью.</span><span class="sxs-lookup"><span data-stu-id="a90c7-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a90c7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a90c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="a90c7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a90c7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a90c7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a90c7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a90c7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a90c7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a90c7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a90c7-110">Called by:</span></span>  <br/> |<span data-ttu-id="a90c7-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a90c7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="a90c7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a90c7-112">Parameters</span></span>

<span data-ttu-id="a90c7-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a90c7-113">_lpsz_</span></span>
  
> <span data-ttu-id="a90c7-114">[in] Указатель на строку с завершенным нулом для поиска.</span><span class="sxs-lookup"><span data-stu-id="a90c7-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="a90c7-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="a90c7-115">_ch_</span></span>
  
> <span data-ttu-id="a90c7-116">[in] Ищите символ.</span><span class="sxs-lookup"><span data-stu-id="a90c7-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a90c7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a90c7-117">Return value</span></span>

<span data-ttu-id="a90c7-118">**SzFindCh** возвращает указатель на первый вхождение символа в строке.</span><span class="sxs-lookup"><span data-stu-id="a90c7-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="a90c7-119">Если символ не встречается ни в одной строке или если параметр  _lpsz_ имеет значение NULL, возвращается значение NULL.</span><span class="sxs-lookup"><span data-stu-id="a90c7-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a90c7-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="a90c7-120">Remarks</span></span>

<span data-ttu-id="a90c7-121">Функция **SzFindCh** ищет только точное совпадение; он чувствителен к различиям в диакритических и диакритических диакритах.</span><span class="sxs-lookup"><span data-stu-id="a90c7-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="a90c7-122">Поиск в форматах Юникод и DBCS поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a90c7-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

