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
ms.openlocfilehash: 7177b2f0f709939b7580fa7abb87490073bb00c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588813"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="89052-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="89052-103">SComparePropsRestriction</span></span>

<span data-ttu-id="89052-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89052-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89052-105">Описывается ограничение свойства сравнения, предназначенный для тестирования два свойства, используя оператор сравнения.</span><span class="sxs-lookup"><span data-stu-id="89052-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89052-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="89052-106">Header file:</span></span>  <br/> |<span data-ttu-id="89052-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89052-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="89052-108">Members</span><span class="sxs-lookup"><span data-stu-id="89052-108">Members</span></span>

<span data-ttu-id="89052-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="89052-109">**relop**</span></span>
  
> <span data-ttu-id="89052-110">Оператор сравнения можно использовать для сравнения двух свойств.</span><span class="sxs-lookup"><span data-stu-id="89052-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="89052-111">Ниже приведены возможные значения:</span><span class="sxs-lookup"><span data-stu-id="89052-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="89052-112">RELOP_GE: Сравнение выполняется на основе на больше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="89052-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="89052-113">RELOP_GT: Сравнение выполняется на основе на более высокой версии первое значение.</span><span class="sxs-lookup"><span data-stu-id="89052-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="89052-114">RELOP_LE: Сравнение выполняется на основе на меньше или равно первого значения.</span><span class="sxs-lookup"><span data-stu-id="89052-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="89052-115">RELOP_LT: Сравнение выполняется на основе на меньшим первое значение.</span><span class="sxs-lookup"><span data-stu-id="89052-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="89052-116">RELOP_NE: Сравнение выполняется на основе на разные значения.</span><span class="sxs-lookup"><span data-stu-id="89052-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="89052-117">RELOP_RE: Сравнение выполняется на основе как значения (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="89052-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="89052-118">RELOP_EQ: Сравнение выполняется на основе на равные значения.</span><span class="sxs-lookup"><span data-stu-id="89052-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="89052-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="89052-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="89052-120">Свойство tag первого свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="89052-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="89052-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="89052-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="89052-122">Свойство tag второго свойства для сравнения.</span><span class="sxs-lookup"><span data-stu-id="89052-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="89052-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="89052-123">Remarks</span></span>

<span data-ttu-id="89052-124">Порядок сравнения _(тег свойства (1) (оператор сравнения) (тег свойства 2)_.</span><span class="sxs-lookup"><span data-stu-id="89052-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="89052-125">Свойства для сравнения значения одного типа.</span><span class="sxs-lookup"><span data-stu-id="89052-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="89052-126">Попытка сравнить свойства различных типов приводит MAPI или поставщик услуг для возврата значения ошибка MAPI_E_TOO_COMPLEX из метода [IMAPITable](imapitableiunknown.md) , к которому структура передается как параметр.</span><span class="sxs-lookup"><span data-stu-id="89052-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="89052-127">В результате ограничение значение свойства сравнения не определен, когда один или оба свойства не существуют.</span><span class="sxs-lookup"><span data-stu-id="89052-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="89052-128">Когда клиент требует некорректно для подобных ограничений и не проверьте, существует ли свойство, (например, это не обязательный столбец таблицы) его необходимо создать **и** ограничения для присоединения к ограничений свойств сравнение с exist ограничение.</span><span class="sxs-lookup"><span data-stu-id="89052-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="89052-129">Используйте структуру [SExistRestriction](sexistrestriction.md) , чтобы определить ограничение exist и структуру [SAndRestriction](sandrestriction.md) для определения **и** ограничение.</span><span class="sxs-lookup"><span data-stu-id="89052-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="89052-130">Свойства, указанные в разделе участники **ulPropTag1** и **ulPropTag2** может быть поддерживающий несколько значений, если поставщик услуг поддерживает его.</span><span class="sxs-lookup"><span data-stu-id="89052-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="89052-131">Дополнительные сведения о структуре **SComparePropsRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="89052-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89052-132">См. также</span><span class="sxs-lookup"><span data-stu-id="89052-132">See also</span></span>

- [<span data-ttu-id="89052-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="89052-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="89052-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="89052-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="89052-135">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="89052-135">MAPI Structures</span></span>](mapi-structures.md)

