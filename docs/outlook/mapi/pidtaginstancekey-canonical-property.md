---
title: Каноническое свойство PidTagInstanceKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInstanceKey
api_type:
- HeaderDef
ms.assetid: 14fc5571-acc0-4d75-8598-964aee5ba01c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c237149c305a80012d1f06ea4373b892d25daec1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396991"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="e7222-103">Каноническое свойство PidTagInstanceKey</span><span class="sxs-lookup"><span data-stu-id="e7222-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="e7222-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7222-105">Содержит значение, уникальным образом определяет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="e7222-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7222-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e7222-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7222-107">PR_INSTANCE_KEY</span><span class="sxs-lookup"><span data-stu-id="e7222-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="e7222-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e7222-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7222-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="e7222-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="e7222-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e7222-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7222-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e7222-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e7222-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e7222-112">Area:</span></span>  <br/> |<span data-ttu-id="e7222-113">Таблица</span><span class="sxs-lookup"><span data-stu-id="e7222-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7222-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e7222-114">Remarks</span></span>

<span data-ttu-id="e7222-115">Это свойство соответствует двоичное значение, которое однозначно определяет строку в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="e7222-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="e7222-116">Это обязательный столбец в большинстве таблиц.</span><span class="sxs-lookup"><span data-stu-id="e7222-116">It is a required column in most tables.</span></span> <span data-ttu-id="e7222-117">Если строка входит в два представления, есть два ключевых другой экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e7222-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="e7222-118">Ключ экземпляра строки, могут отличаться каждый раз при открытии таблицы, но остаются постоянными при таблице open.</span><span class="sxs-lookup"><span data-stu-id="e7222-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="e7222-119">Строки, добавленные во время таблицы не повторного использования ключа экземпляра, который использовался ранее.</span><span class="sxs-lookup"><span data-stu-id="e7222-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="e7222-120">Чтобы сопоставить все строки расширение с помощью **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или свойства **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e7222-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="e7222-121">Используйте **PR_INSTANCE_KEY** для указания конкретного экземпляра в развертывание.</span><span class="sxs-lookup"><span data-stu-id="e7222-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="e7222-122">При развертывании свойством в таблице строка создается для каждого экземпляра расширения, то есть, для каждого значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="e7222-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="e7222-123">Каждая строка имеет уникальное значение для свойства **PR_INSTANCE_KEY** , а все остальные столбцы сохранить исходные значения во всей расширения.</span><span class="sxs-lookup"><span data-stu-id="e7222-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="e7222-124">В по категориям Сортировка таблицы строки, не соответствующие фактические данные можно добавить в результаты сортировки.</span><span class="sxs-lookup"><span data-stu-id="e7222-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="e7222-125">Как и все строки во всех таблицах каждую строку, имеет свой собственный ключ уникальный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e7222-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="e7222-126">**PR_INSTANCE_KEY** также используется в таблице уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="e7222-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="e7222-127">**PropIndex** и **propPrior** элементы структуры [TABLE_NOTIFICATION](table_notification.md) — это [SPropValue](spropvalue.md) структуры, содержащие **PR_INSTANCE_KEY** значения.</span><span class="sxs-lookup"><span data-stu-id="e7222-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="e7222-128">Элемент **propIndex** указывает строку, в которой были добавлены или изменены.</span><span class="sxs-lookup"><span data-stu-id="e7222-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="e7222-129">Элемент **propPrior** указывает строку перед строкой добавленного или измененного (**PR_NULL** указывает на изменение в первую строку).</span><span class="sxs-lookup"><span data-stu-id="e7222-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="e7222-130">Это значение не копируется как часть в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="e7222-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="e7222-131">**PR_INSTANCE_KEY** — это структура [MAPIUID](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="e7222-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="e7222-132">Все экземпляр непосредственно сравнения ключей как двоичные значения.</span><span class="sxs-lookup"><span data-stu-id="e7222-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e7222-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e7222-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7222-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="e7222-134">Protocol specifications</span></span>

<span data-ttu-id="e7222-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7222-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7222-136">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e7222-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7222-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7222-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7222-138">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7222-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7222-139">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="e7222-139">Header files</span></span>

<span data-ttu-id="e7222-140">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7222-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7222-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e7222-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7222-142">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7222-142">Mapitags.h</span></span>
  
> <span data-ttu-id="e7222-143">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="e7222-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7222-144">См. также</span><span class="sxs-lookup"><span data-stu-id="e7222-144">See also</span></span>



[<span data-ttu-id="e7222-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7222-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7222-146">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e7222-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7222-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e7222-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7222-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="e7222-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

