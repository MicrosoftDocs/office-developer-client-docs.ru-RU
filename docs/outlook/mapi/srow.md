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
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336520"
---
# <a name="srow"></a><span data-ttu-id="d0f4e-103">SRow</span><span class="sxs-lookup"><span data-stu-id="d0f4e-103">SRow</span></span>

<span data-ttu-id="d0f4e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0f4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0f4e-105">Описывает строку из таблицы, которая содержит выбранные свойства для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0f4e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d0f4e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d0f4e-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d0f4e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="d0f4e-108">Members</span><span class="sxs-lookup"><span data-stu-id="d0f4e-108">Members</span></span>

<span data-ttu-id="d0f4e-109">**Уладрентрипад**</span><span class="sxs-lookup"><span data-stu-id="d0f4e-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="d0f4e-110">Заполнение байтов для правильного выравнивания значений свойств, на которые указывает элемент **лппропс** .</span><span class="sxs-lookup"><span data-stu-id="d0f4e-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="d0f4e-111">**Квалуес**</span><span class="sxs-lookup"><span data-stu-id="d0f4e-111">**cValues**</span></span>
  
> <span data-ttu-id="d0f4e-112">Количество значений свойств, на которые указывает **лппропс**.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="d0f4e-113">**Лппропс**</span><span class="sxs-lookup"><span data-stu-id="d0f4e-113">**lpProps**</span></span>
  
> <span data-ttu-id="d0f4e-114">Указатель на массив структур [спропвалуе](spropvalue.md) , описывающих значения свойств для столбцов в строке.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d0f4e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0f4e-115">Remarks</span></span>

<span data-ttu-id="d0f4e-116">Структура **сров** описывает строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="d0f4e-117">Он включен в структуру [табле_нотификатион](table_notification.md) , сопровождающую табличное уведомление.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="d0f4e-118">Структуры **сров** используются в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="d0f4e-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="d0f4e-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="d0f4e-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="d0f4e-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="d0f4e-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="d0f4e-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d0f4e-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="d0f4e-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="d0f4e-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="d0f4e-123">[Итабледата: IUnknown](itabledataiunknown.md) (многие методы)</span><span class="sxs-lookup"><span data-stu-id="d0f4e-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="d0f4e-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="d0f4e-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="d0f4e-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="d0f4e-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="d0f4e-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="d0f4e-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="d0f4e-127">Если необходимо описать более одной строки, используется структура [SRowSet](srowset.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f4e-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="d0f4e-128">Структура **SRowSet** содержит массив структур **сров** и число структур в массиве.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="d0f4e-129">На следующем рисунке показана связь между **сров** и структурой данных **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="d0f4e-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="d0f4e-130">**Отношение между SRow и SRowSet**</span><span class="sxs-lookup"><span data-stu-id="d0f4e-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="d0f4e-131">![Отношение между сров и SRowSet] (media/amapi_17.gif "Отношение между сров и SRowSet")</span><span class="sxs-lookup"><span data-stu-id="d0f4e-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="d0f4e-132">Структуры **сров** определяются так же, как структуры [адрентри](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f4e-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="d0f4e-133">Таким образом, строка таблицы получателей и запись в списке адресов могут рассматриваться как один и тот же.</span><span class="sxs-lookup"><span data-stu-id="d0f4e-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="d0f4e-134">Сведения о том, как следует выделить память для структур **сров** , можно узнать в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="d0f4e-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0f4e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="d0f4e-135">See also</span></span>

- [<span data-ttu-id="d0f4e-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="d0f4e-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="d0f4e-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="d0f4e-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="d0f4e-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="d0f4e-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="d0f4e-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d0f4e-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="d0f4e-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="d0f4e-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="d0f4e-141">Управление памятью для структур ADRLIST и SRowSet</span><span class="sxs-lookup"><span data-stu-id="d0f4e-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

