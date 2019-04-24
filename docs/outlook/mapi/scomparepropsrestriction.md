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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351291"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="9d4f9-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="9d4f9-103">SComparePropsRestriction</span></span>

<span data-ttu-id="9d4f9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d4f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d4f9-105">Описывает ограничение свойства Compare, которое проверяет два свойства с помощью оператора отношения.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d4f9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9d4f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d4f9-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9d4f9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="9d4f9-108">Members</span><span class="sxs-lookup"><span data-stu-id="9d4f9-108">Members</span></span>

<span data-ttu-id="9d4f9-109">**релоп**</span><span class="sxs-lookup"><span data-stu-id="9d4f9-109">**relop**</span></span>
  
> <span data-ttu-id="9d4f9-110">Оператор отношения, который используется для сравнения двух свойств.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="9d4f9-111">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9d4f9-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="9d4f9-112">РЕЛОП_ЖЕ: сравнение выполняется на основе более высокого или равного первого значения.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="9d4f9-113">РЕЛОП_ГТ: сравнение выполняется на основе большего первого значения.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="9d4f9-114">РЕЛОП_ЛЕ: сравнение выполняется на основе меньшего или равного первого значения.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="9d4f9-115">РЕЛОП_ЛТ: сравнение выполняется на основе меньшего первого значения.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="9d4f9-116">РЕЛОП_НЕ: сравнение выполняется на основе неодинаковых значений.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="9d4f9-117">РЕЛОП_РЕ: сравнение выполняется на основе значений LIKE (регулярное выражение).</span><span class="sxs-lookup"><span data-stu-id="9d4f9-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="9d4f9-118">РЕЛОП_ЕК: сравнение выполняется на основе равных значений.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="9d4f9-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="9d4f9-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="9d4f9-120">Тег свойства первого сравниваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="9d4f9-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="9d4f9-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="9d4f9-122">Тег свойства второго свойства, которое требуется сравнить.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d4f9-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d4f9-123">Remarks</span></span>

<span data-ttu-id="9d4f9-124">Порядок сравнения _(тег свойства 1) (оператор отношения) (тег свойства 2)_.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="9d4f9-125">Сравниваемые свойства должны относиться к одному и тому же типу.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="9d4f9-126">Попытка сравнить свойства различных типов приводит к тому, что MAPI или поставщик услуг возвращает значение ошибки МАПИ_Е_ТУ_КОМПЛЕКС из метода [IMAPITable](imapitableiunknown.md) , для которого структура передается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="9d4f9-127">Результат ограничения значения свойства Compare не определен, если одно или оба свойства не существуют.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="9d4f9-128">Когда клиенту требуется строго определенное поведение для такого ограничения и не гарантируется, существует ли свойство (например, это не обязательный столбец таблицы), необходимо создать ограничение **и** разрешить присоединение к ограничению свойства Compare с помощью EXISTS. лагать.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="9d4f9-129">Используйте структуру [сексистрестриктион](sexistrestriction.md) , чтобы определить ограничение exist и структуру [сандрестриктион](sandrestriction.md) для определения ограничения. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9d4f9-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="9d4f9-130">Свойства, указанные в членах **ulPropTag1** и **ulPropTag2** , могут быть многозначными, если поставщик услуг поддерживает ее.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="9d4f9-131">Для получения дополнительных сведений о структуре и ограничениях **скомпарепропсрестриктион** в целом ознакомьтесь [](about-restrictions.md)с ограничениями.</span><span class="sxs-lookup"><span data-stu-id="9d4f9-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d4f9-132">См. также</span><span class="sxs-lookup"><span data-stu-id="9d4f9-132">See also</span></span>

- [<span data-ttu-id="9d4f9-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="9d4f9-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="9d4f9-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9d4f9-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="9d4f9-135">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9d4f9-135">MAPI Structures</span></span>](mapi-structures.md)

