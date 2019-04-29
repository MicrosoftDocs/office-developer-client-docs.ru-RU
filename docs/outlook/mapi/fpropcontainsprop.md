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
# <a name="fpropcontainsprop"></a><span data-ttu-id="2cc95-103">FPropContainsProp</span><span class="sxs-lookup"><span data-stu-id="2cc95-103">FPropContainsProp</span></span>

<span data-ttu-id="2cc95-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cc95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cc95-105">Сравнивает два значения свойств, обычно строки или двоичные массивы, чтобы проверить, содержит ли один из них другой.</span><span class="sxs-lookup"><span data-stu-id="2cc95-105">Compares two property values, generally strings or binary arrays, to see if one contains the other.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cc95-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2cc95-106">Header file:</span></span>  <br/> |<span data-ttu-id="2cc95-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="2cc95-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2cc95-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2cc95-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2cc95-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2cc95-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2cc95-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2cc95-110">Called by:</span></span>  <br/> |<span data-ttu-id="2cc95-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="2cc95-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a><span data-ttu-id="2cc95-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cc95-112">Parameters</span></span>

<span data-ttu-id="2cc95-113">_Лпспропвалуедст_</span><span class="sxs-lookup"><span data-stu-id="2cc95-113">_lpSPropValueDst_</span></span>
  
> <span data-ttu-id="2cc95-114">возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую значение свойства, которое может содержать строку поиска, на которую указывает параметр _лпспропвалуесрк_ .</span><span class="sxs-lookup"><span data-stu-id="2cc95-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the property value that might contain the search string pointed to by the  _lpSPropValueSrc_ parameter.</span></span> 
    
<span data-ttu-id="2cc95-115">_Лпспропвалуесрк_</span><span class="sxs-lookup"><span data-stu-id="2cc95-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="2cc95-116">возврата Указатель на структуру **спропвалуе** , определяющую строку поиска, которую **фпропконтаинспроп** ищет в значении свойства, на которое указывает параметр _лпспропвалуедст_ .</span><span class="sxs-lookup"><span data-stu-id="2cc95-116">[in] Pointer to an **SPropValue** structure defining the search string that **FPropContainsProp** is seeking in the property value pointed to by the  _lpSPropValueDst_ parameter.</span></span> 
    
<span data-ttu-id="2cc95-117">_Улфуззилевел_</span><span class="sxs-lookup"><span data-stu-id="2cc95-117">_ulFuzzyLevel_</span></span>
  
> <span data-ttu-id="2cc95-118">возврата Параметры параметров, определяющие степень точности, используемую в сравнении.</span><span class="sxs-lookup"><span data-stu-id="2cc95-118">[in] Option settings defining the level of preciseness to use in the comparison.</span></span> 

  - <span data-ttu-id="2cc95-119">**Младшие 16 битов** применяются к свойствам типа ПТ_БИНАРИ и PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="2cc95-119">The **lower 16 bits** apply to properties of type PT_BINARY and PT_STRING8.</span></span> <span data-ttu-id="2cc95-120">Для них должно быть задано значение, равное одному из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2cc95-120">They must be set to exactly one of the following values:</span></span>
      
    - <span data-ttu-id="2cc95-121">ФЛ_ФУЛЛСТРИНГ: строка поиска _лпспропвалуесрк_ должна быть равна значению свойства, определенному с помощью _лпспропвалуедст_.</span><span class="sxs-lookup"><span data-stu-id="2cc95-121">FL_FULLSTRING: The  _lpSPropValueSrc_ search string must be equal to the property value identified by  _lpSPropValueDst_.</span></span>
        
    - <span data-ttu-id="2cc95-122">ФЛ_ПРЕФИКС: строка поиска _лпспропвалуесрк_ должна находиться в начале значения свойства, идентифицируемого _лпспропвалуедст_.</span><span class="sxs-lookup"><span data-stu-id="2cc95-122">FL_PREFIX: The  _lpSPropValueSrc_ search string must appear at the beginning of the property value identified by  _lpSPropValueDst_.</span></span> <span data-ttu-id="2cc95-123">Эти два значения должны сравниваться только с длиной строки поиска, указанной в _лпспропвалуесрк_.</span><span class="sxs-lookup"><span data-stu-id="2cc95-123">The two values should be compared only up to the length of the search string indicated by  _lpSPropValueSrc_.</span></span> 
        
    - <span data-ttu-id="2cc95-124">ФЛ_СУБСТРИНГ: строка поиска _лпспропвалуесрк_ должна содержаться в любом месте в значении свойства, определенном с помощью _лпспропвалуедст_.</span><span class="sxs-lookup"><span data-stu-id="2cc95-124">FL_SUBSTRING: The  _lpSPropValueSrc_ search string must be contained anywhere in the property value identified by  _lpSPropValueDst_.</span></span> 
      
  - <span data-ttu-id="2cc95-125">**Верхние 16 битов** применяются только к свойствам типа PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="2cc95-125">The **upper 16 bits** apply only to properties of type PT_STRING8.</span></span> <span data-ttu-id="2cc95-126">Можно задать следующие значения в любой комбинации:</span><span class="sxs-lookup"><span data-stu-id="2cc95-126">They can be set to the following values in any combination:</span></span>
    
    - <span data-ttu-id="2cc95-127">ФЛ_ИГНОРЕКАСЕ: сравнение следует производить без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="2cc95-127">FL_IGNORECASE: The comparison should be made without considering case sensitivity.</span></span> 
        
    - <span data-ttu-id="2cc95-128">ФЛ_ИГНОРЕНОНСПАЦЕ: сравнение должно игнорировать заданные Юникод несамостоятельные символы, такие как диакритические знаки.</span><span class="sxs-lookup"><span data-stu-id="2cc95-128">FL_IGNORENONSPACE: The comparison should ignore Unicode-defined nonspacing characters such as diacritical marks.</span></span> 
        
    - <span data-ttu-id="2cc95-129">ФЛ_ЛУСЕ: сравнение должно указывать на сопоставление, если это возможно, без учета регистра символов и несамостоятельных символов.</span><span class="sxs-lookup"><span data-stu-id="2cc95-129">FL_LOOSE: The comparison should indicate a match whenever possible, ignoring case sensitivity and nonspacing characters.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2cc95-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2cc95-130">Return value</span></span>

<span data-ttu-id="2cc95-131">TRUE</span><span class="sxs-lookup"><span data-stu-id="2cc95-131">TRUE</span></span> 
  
> <span data-ttu-id="2cc95-132">Все параметры являются допустимыми, а строка поиска _лпспропвалуесрк_ указывается в значении свойства _лпспропвалуедст_ .</span><span class="sxs-lookup"><span data-stu-id="2cc95-132">The parameters are all valid and the  _lpSPropValueSrc_ search string is contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
<span data-ttu-id="2cc95-133">FALSE</span><span class="sxs-lookup"><span data-stu-id="2cc95-133">FALSE</span></span> 
  
> <span data-ttu-id="2cc95-134">Сравниваемые значения свойств не относятся к типу PT_STRING8 или ПТ_БИНАРИ, значения свойств относятся к разным типам, или строка поиска _лпспропвалуесрк_ не указана в значении свойства _лпспропвалуедст_ .</span><span class="sxs-lookup"><span data-stu-id="2cc95-134">The property values being compared are not of type PT_STRING8 or PT_BINARY, the property values are of different types, or the  _lpSPropValueSrc_ search string is not contained as specified in the  _lpSPropValueDst_ property value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2cc95-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="2cc95-135">Remarks</span></span>

<span data-ttu-id="2cc95-136">Метод сравнения зависит от типов свойств, указанных в определениях свойств [спропвалуе](spropvalue.md) , и эвристического алгоритма нечеткого уровня, указанного в параметре _улфуззилевел_ .</span><span class="sxs-lookup"><span data-stu-id="2cc95-136">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions and the fuzzy level heuristic provided in the  _ulFuzzyLevel_ parameter.</span></span> <span data-ttu-id="2cc95-137">Функции [фпропкомпарепроп](fpropcompareprop.md) и **фпропконтаинспроп** можно использовать для подготовки ограничений для создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="2cc95-137">The [FPropCompareProp](fpropcompareprop.md) and **FPropContainsProp** functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="2cc95-138">Верхние 16 разрядов _улфуззилевел_ игнорируются для свойства пт_бинари типа.</span><span class="sxs-lookup"><span data-stu-id="2cc95-138">The upper 16 bits of  _ulFuzzyLevel_ are ignored for property type PT_BINARY.</span></span> <span data-ttu-id="2cc95-139">Если параметры в _улфуззилевел_ отсутствуют или являются недопустимыми, выполняется точное точное совпадение.</span><span class="sxs-lookup"><span data-stu-id="2cc95-139">If the settings in  _ulFuzzyLevel_ are missing or invalid, a full-string exact match is performed.</span></span> <span data-ttu-id="2cc95-140">Дополнительные сведения о вложении свойств можно найти в разделе Структура [сконтентрестриктион](scontentrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="2cc95-140">For more information about property containment, see the [SContentRestriction](scontentrestriction.md) structure.</span></span> 
  

