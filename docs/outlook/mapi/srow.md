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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410436"
---
# <a name="srow"></a><span data-ttu-id="bfef1-103">SRow</span><span class="sxs-lookup"><span data-stu-id="bfef1-103">SRow</span></span>

<span data-ttu-id="bfef1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfef1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfef1-105">Описывает строку из таблицы, которая содержит выбранные свойства для конкретного объекта.</span><span class="sxs-lookup"><span data-stu-id="bfef1-105">Describes a row from a table that contains selected properties for a specific object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bfef1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="bfef1-106">Header file:</span></span>  <br/> |<span data-ttu-id="bfef1-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bfef1-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a><span data-ttu-id="bfef1-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="bfef1-108">Members</span></span>

<span data-ttu-id="bfef1-109">**ulAdrEntryPad**</span><span class="sxs-lookup"><span data-stu-id="bfef1-109">**ulAdrEntryPad**</span></span>
  
> <span data-ttu-id="bfef1-110">Байты заполнения для правильного выравнивания значений свойств, на которые указывает **член lpProps.**</span><span class="sxs-lookup"><span data-stu-id="bfef1-110">Padding bytes to properly align the property values pointed to by the **lpProps** member.</span></span> 
    
<span data-ttu-id="bfef1-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="bfef1-111">**cValues**</span></span>
  
> <span data-ttu-id="bfef1-112">Количество значений свойств, на которые указывает **lpProps.**</span><span class="sxs-lookup"><span data-stu-id="bfef1-112">Count of property values pointed to by **lpProps**.</span></span> 
    
<span data-ttu-id="bfef1-113">**lpProps**</span><span class="sxs-lookup"><span data-stu-id="bfef1-113">**lpProps**</span></span>
  
> <span data-ttu-id="bfef1-114">Указатель на массив структур [SPropValue,](spropvalue.md) которые описывают значения свойств столбцов в строке.</span><span class="sxs-lookup"><span data-stu-id="bfef1-114">Pointer to an array of [SPropValue](spropvalue.md) structures that describe the property values for the columns in the row.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="bfef1-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="bfef1-115">Remarks</span></span>

<span data-ttu-id="bfef1-116">Структура **SRow** описывает строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="bfef1-116">An **SRow** structure describes a row in a table.</span></span> <span data-ttu-id="bfef1-117">Он включен в [структуру](table_notification.md) TABLE_NOTIFICATION, которая сопровождает уведомление таблицы.</span><span class="sxs-lookup"><span data-stu-id="bfef1-117">It is included in the [TABLE_NOTIFICATION](table_notification.md) structure that accompanies a table notification.</span></span> 
  
<span data-ttu-id="bfef1-118">**Структуры SRow** используются в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="bfef1-118">**SRow** structures are used in the following methods:</span></span> 
  
- [<span data-ttu-id="bfef1-119">IAddrBook::GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bfef1-119">IAddrBook::GetSearchPath</span></span>](iaddrbook-getsearchpath.md)
    
- [<span data-ttu-id="bfef1-120">IAddrBook::SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="bfef1-120">IAddrBook::SetSearchPath</span></span>](iaddrbook-setsearchpath.md)
    
- [<span data-ttu-id="bfef1-121">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="bfef1-121">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
    
- [<span data-ttu-id="bfef1-122">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="bfef1-122">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
    
- <span data-ttu-id="bfef1-123">[ITableData : IUnknown](itabledataiunknown.md) (много методов)</span><span class="sxs-lookup"><span data-stu-id="bfef1-123">[ITableData : IUnknown](itabledataiunknown.md) (many methods)</span></span> 
    
- [<span data-ttu-id="bfef1-124">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="bfef1-124">FBadRowSet</span></span>](fbadrowset.md)
    
- [<span data-ttu-id="bfef1-125">FreeProws</span><span class="sxs-lookup"><span data-stu-id="bfef1-125">FreeProws</span></span>](freeprows.md)
    
- [<span data-ttu-id="bfef1-126">HrQueryAllRows</span><span class="sxs-lookup"><span data-stu-id="bfef1-126">HrQueryAllRows</span></span>](hrqueryallrows.md)
    
<span data-ttu-id="bfef1-127">Если требуется описать несколько строк, используется структура [SRowSet.](srowset.md)</span><span class="sxs-lookup"><span data-stu-id="bfef1-127">When more than one row needs to be described, an [SRowSet](srowset.md) structure is used.</span></span> <span data-ttu-id="bfef1-128">Структура **SRowSet** содержит массив структур **SRow** и количество структур в массиве.</span><span class="sxs-lookup"><span data-stu-id="bfef1-128">An **SRowSet** structure contains an array of **SRow** structures and a count of structures in the array.</span></span> 
  
<span data-ttu-id="bfef1-129">На следующем рисунке показана связь **между структурой данных SRow и** **SRowSet.**</span><span class="sxs-lookup"><span data-stu-id="bfef1-129">The following illustration shows the relationship between an **SRow** and an **SRowSet** data structure.</span></span> 
  
<span data-ttu-id="bfef1-130">**Отношение между SRow и SRowSet**</span><span class="sxs-lookup"><span data-stu-id="bfef1-130">**Relationship between SRow and SRowSet**</span></span>
  
<span data-ttu-id="bfef1-131">![Связь между SRow и SRowSet](media/amapi_17.gif "между SRow и SRowSet")</span><span class="sxs-lookup"><span data-stu-id="bfef1-131">![Relationship between SRow and SRowSet](media/amapi_17.gif "Relationship between SRow and SRowSet")</span></span>
  
<span data-ttu-id="bfef1-132">**Структуры SRow** определяются так же, как структуры [ADRENTRY.](adrentry.md)</span><span class="sxs-lookup"><span data-stu-id="bfef1-132">**SRow** structures are defined the same as [ADRENTRY](adrentry.md) structures.</span></span> <span data-ttu-id="bfef1-133">Таким образом, строка таблицы получателей и запись в списке адресов могут быть обработаны одинаково.</span><span class="sxs-lookup"><span data-stu-id="bfef1-133">Therefore, a row of a recipient table and an entry in an address list can be treated the same.</span></span> 
  
<span data-ttu-id="bfef1-134">Сведения о выделении памяти для структур **SRow** см. в подсети "Управление памятью для [структур ADRLIST и SRowSet".](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="bfef1-134">For information about how the memory for **SRow** structures should be allocated, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bfef1-135">См. также</span><span class="sxs-lookup"><span data-stu-id="bfef1-135">See also</span></span>

- [<span data-ttu-id="bfef1-136">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="bfef1-136">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="bfef1-137">SPropValue</span><span class="sxs-lookup"><span data-stu-id="bfef1-137">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="bfef1-138">SRowSet</span><span class="sxs-lookup"><span data-stu-id="bfef1-138">SRowSet</span></span>](srowset.md)
- [<span data-ttu-id="bfef1-139">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bfef1-139">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="bfef1-140">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="bfef1-140">MAPI Structures</span></span>](mapi-structures.md)
- [<span data-ttu-id="bfef1-141">Управление памятью для структур ADRLIST и SRowSet</span><span class="sxs-lookup"><span data-stu-id="bfef1-141">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

