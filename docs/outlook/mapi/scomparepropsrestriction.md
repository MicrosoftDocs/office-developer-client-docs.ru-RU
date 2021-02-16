---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440005"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="e887d-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="e887d-103">SComparePropsRestriction</span></span>

<span data-ttu-id="e887d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e887d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e887d-105">Описывает ограничение сравнения свойств, которое тестирует два свойства с помощью реляционного оператора.</span><span class="sxs-lookup"><span data-stu-id="e887d-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e887d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e887d-106">Header file:</span></span>  <br/> |<span data-ttu-id="e887d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e887d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="e887d-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="e887d-108">Members</span></span>

<span data-ttu-id="e887d-109">**relop**</span><span class="sxs-lookup"><span data-stu-id="e887d-109">**relop**</span></span>
  
> <span data-ttu-id="e887d-110">Реляционный оператор для сравнения двух свойств.</span><span class="sxs-lookup"><span data-stu-id="e887d-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="e887d-111">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="e887d-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="e887d-112">RELOP_GE: сравнение основано на большем или равном первом значении.</span><span class="sxs-lookup"><span data-stu-id="e887d-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="e887d-113">RELOP_GT: сравнение основано на большем первом значении.</span><span class="sxs-lookup"><span data-stu-id="e887d-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="e887d-114">RELOP_LE: сравнение основано на меньшем или равном первом значении.</span><span class="sxs-lookup"><span data-stu-id="e887d-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="e887d-115">RELOP_LT: сравнение основано на меньшем первом значении.</span><span class="sxs-lookup"><span data-stu-id="e887d-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="e887d-116">RELOP_NE: сравнение основано на значениях значений значений.</span><span class="sxs-lookup"><span data-stu-id="e887d-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="e887d-117">RELOP_RE: сравнение основано на значениях LIKE (регулярного выражения).</span><span class="sxs-lookup"><span data-stu-id="e887d-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="e887d-118">RELOP_EQ: сравнение основано на одинаковых значениях.</span><span class="sxs-lookup"><span data-stu-id="e887d-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="e887d-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="e887d-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="e887d-120">Тег свойства первого сравниваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="e887d-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="e887d-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="e887d-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="e887d-122">Тег свойства второго свойства, который необходимо сравнить.</span><span class="sxs-lookup"><span data-stu-id="e887d-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e887d-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="e887d-123">Remarks</span></span>

<span data-ttu-id="e887d-124">Порядок сравнения : _(тег свойства 1) (реляционный оператор) (тег свойства 2)._</span><span class="sxs-lookup"><span data-stu-id="e887d-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="e887d-125">Сравниваемые свойства должны иметь одинаковый тип.</span><span class="sxs-lookup"><span data-stu-id="e887d-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="e887d-126">При попытке сравнить свойства различных типов MAPI или поставщик услуг возвращает значение ошибки MAPI_E_TOO_COMPLEX из метода [IMAPITable,](imapitableiunknown.md) в который структура передается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="e887d-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="e887d-127">Результат ограничения значения свойства сравнения не задается, если одно или оба свойства не существуют.</span><span class="sxs-lookup"><span data-stu-id="e887d-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="e887d-128">Если клиент требует четкого поведения для такого ограничения и не уверен, существует ли свойство (например, это не обязательное столбец таблицы), он должен создать ограничение **AND,** чтобы присоединиться к ограничению сравнения свойств с ограничением на существование.</span><span class="sxs-lookup"><span data-stu-id="e887d-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="e887d-129">Используйте [структуру SExistRestriction](sexistrestriction.md) для определения ограничений на существование и [структуру SAndRestriction](sandrestriction.md) для определения **ограничения AND.**</span><span class="sxs-lookup"><span data-stu-id="e887d-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="e887d-130">Свойства, указанные в членах **ulPropTag1** и **ulPropTag2,** могут иметь несколько значений, если поставщик услуг поддерживает их.</span><span class="sxs-lookup"><span data-stu-id="e887d-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="e887d-131">Дополнительные сведения о структуре **и ограничениях SComparePropsRestriction** в целом см. в сведениях [об ограничениях.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="e887d-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e887d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e887d-132">See also</span></span>

- [<span data-ttu-id="e887d-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="e887d-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="e887d-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="e887d-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="e887d-135">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e887d-135">MAPI Structures</span></span>](mapi-structures.md)

