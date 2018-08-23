---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579125"
---
# <a name="srow"></a><span data-ttu-id="20763-103">SRow</span><span class="sxs-lookup"><span data-stu-id="20763-103">SRow</span></span>

<span data-ttu-id="20763-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20763-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20763-105">Описывает строку из таблицы, содержащей выбранных свойств для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="20763-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20763-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="20763-106">Header file:</span></span>  <br/> |<span data-ttu-id="20763-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20763-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="20763-108">Members</span><span class="sxs-lookup"><span data-stu-id="20763-108">Members</span></span>

<span data-ttu-id="20763-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="20763-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="20763-110">Внутренние поля байт для правильного выравнивания значения свойств указывает член **lpProps** .</span><span class="sxs-lookup"><span data-stu-id="20763-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="20763-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="20763-111">**cValues**</span></span>
  
> <span data-ttu-id="20763-112">Количество значений свойств, на который указывает **lpProps**.</span><span class="sxs-lookup"><span data-stu-id="20763-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="20763-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="20763-113">**lpProps**</span></span>
  
> <span data-ttu-id="20763-114">Указатель на массив структур [SPropValue](spropvalue.md) , которые описывают значения свойств для столбцов в строке.</span><span class="sxs-lookup"><span data-stu-id="20763-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="20763-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="20763-115">Remarks</span></span>

<span data-ttu-id="20763-116">Структура с **SRow** Описание строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="20763-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="20763-117">Она включена в структуре [TABLE_NOTIFICATION](table_notification.md) , который описывается в таблице уведомлений.</span><span class="sxs-lookup"><span data-stu-id="20763-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="20763-118">**SRow** структуры используются следующие методы:</span><span class="sxs-lookup"><span data-stu-id="20763-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="20763-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="20763-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="20763-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="20763-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="20763-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="20763-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="20763-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="20763-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="20763-123">[ITableData: IUnknown](itabledataiunknown.md) (множество методов)</span><span class="sxs-lookup"><span data-stu-id="20763-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="20763-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="20763-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="20763-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="20763-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="20763-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="20763-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="20763-127">Если более одного ряда должен быть описано, используется структуру [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="20763-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="20763-128">Структура **SRowSet** содержит массив структур **SRow** и число структур в массиве.</span><span class="sxs-lookup"><span data-stu-id="20763-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="20763-129">На следующем рисунке показана связь между **SRow** и **SRowSet** структуру данных.</span><span class="sxs-lookup"><span data-stu-id="20763-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="20763-130">**Отношение между SRow и SRowSet**</span><span class="sxs-lookup"><span data-stu-id="20763-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="20763-131">![Отношение между SRow и SRowSet] (media/amapi_17.gif "Отношение между SRow и SRowSet")</span><span class="sxs-lookup"><span data-stu-id="20763-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="20763-132">Определения структур **SRow** то же, что [ADRENTRY](adrentry.md) структуры.</span><span class="sxs-lookup"><span data-stu-id="20763-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="20763-133">Таким образом, может быть строку таблице получателей и запись в список адресов обрабатывается так же.</span><span class="sxs-lookup"><span data-stu-id="20763-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="20763-134">Сведения о том, как следует выделить память для структуры **SRow** [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md)см.</span><span class="sxs-lookup"><span data-stu-id="20763-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20763-135">См. также</span><span class="sxs-lookup"><span data-stu-id="20763-135">See also</span></span>

- [<span data-ttu-id="20763-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="20763-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="20763-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="20763-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="20763-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="20763-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="20763-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="20763-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="20763-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="20763-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="20763-141">Управление памятью для структур ADRLIST и SRowSet</span><span class="sxs-lookup"><span data-stu-id="20763-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

