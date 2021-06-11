---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432634"
---
# <a name="fpropcontainsprop"></a><span data-ttu-id="ff9ad-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="ff9ad-103">FPropContainsProp</span></span>

<span data-ttu-id="ff9ad-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff9ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff9ad-105">Сравнивает два значения свойств, как правило, строки или двоичные массивы, чтобы узнать, содержит ли одно другое.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff9ad-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff9ad-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ff9ad-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ff9ad-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff9ad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff9ad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff9ad-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="ff9ad-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="ff9ad-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="ff9ad-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="ff9ad-112">Parameters</span></span>

<span data-ttu-id="ff9ad-113">_lpSPropValueDst_</span><span class="sxs-lookup"><span data-stu-id="ff9ad-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="ff9ad-114">[in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей значение свойства, которое может содержать строку поиска, указываемую параметром _lpSPropValueSrc._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="ff9ad-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="ff9ad-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="ff9ad-116">[in] Указатель на **структуру SPropValue,** определяющей строку поиска, которую **ищет FPropContainsProp,** в значении свойства, на которое указывает параметр _lpSPropValueDst._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="ff9ad-117">_ulFuzzyLevel_</span><span class="sxs-lookup"><span data-stu-id="ff9ad-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="ff9ad-118">[in] Параметры, определяющие уровень точности, который необходимо использовать в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="ff9ad-119">Нижние **16 битов** применяются к свойствам типа PT_BINARY и PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="ff9ad-120">Они должны быть назначены как раз к одному из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="ff9ad-121">FL_FULLSTRING. Строка поиска _lpSPropValueSrc_ должна быть равна значению свойства, установленного _lpSPropValueDst._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="ff9ad-122">FL_PREFIX. Строка поиска  _lpSPropValueSrc_ должна отображаться в начале значения свойства, установленного  _lpSPropValueDst_.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="ff9ad-123">Эти два значения следует сравнить только с длиной строки поиска, обозначенной _lpSPropValueSrc._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="ff9ad-124">FL_SUBSTRING. Строка поиска _lpSPropValueSrc_ должна содержаться в любом месте в значении свойства, идентифицированного _lpSPropValueDst._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="ff9ad-125">Верхние **16 битов** применяются только к свойствам типа PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="ff9ad-126">Они могут быть установлены к следующим значениям в любой комбинации:</span><span class="sxs-lookup"><span data-stu-id="ff9ad-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="ff9ad-127">FL_IGNORECASE. Сравнение должно быть выполнено без рассмотрения чувствительности к делу.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="ff9ad-128">FL_IGNORENONSPACE. Сравнение должно игнорировать неспаксированные символы, определенные Юникодом, такие как диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="ff9ad-129">FL_LOOSE. Сравнение должно указывать совпадение по мере возможности, игнорируя чувствительность к делу и неспаные символы.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff9ad-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff9ad-130">Return value</span></span>

<span data-ttu-id="ff9ad-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="ff9ad-131">TRUE</span></span> 
  
> <span data-ttu-id="ff9ad-132">Все параметры действительны, а строка поиска _lpSPropValueSrc_ содержится в значении _свойства lpSPropValueDst._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="ff9ad-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="ff9ad-133">FALSE</span></span> 
  
> <span data-ttu-id="ff9ad-134">Сравниваемые значения свойств не имеют типа PT_STRING8 или PT_BINARY, значения свойств имеют различные типы, или строка поиска _lpSPropValueSrc_ не содержится, как указано в значении свойства _lpSPropValueDst._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ff9ad-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff9ad-135">Remarks</span></span>

<span data-ttu-id="ff9ad-136">Метод сравнения зависит от типов свойств, указанных в определениях [свойств SPropValue,](spropvalue.md) и эвристичного уровня нечетких уровней, указанных в параметре _ulFuzzyLevel._</span><span class="sxs-lookup"><span data-stu-id="ff9ad-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="ff9ad-137">Функции [FPropCompareProp](fpropcompareprop.md) и **FPropContainsProp** можно использовать для подготовки ограничений для создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="ff9ad-138">Верхние 16  _битов ulFuzzyLevel_ игнорируются для типа PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="ff9ad-139">Если параметры  _в ulFuzzyLevel_ отсутствуют или недействительны, выполняется полное совпадение точных строк.</span><span class="sxs-lookup"><span data-stu-id="ff9ad-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="ff9ad-140">Дополнительные сведения о сдерживании свойств см. в структуре [SContentRestriction.](scontentrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="ff9ad-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

