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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358513"
---
# <a name="pidtaginstancekey-canonical-property"></a><span data-ttu-id="13b89-103">Каноническое свойство PidTagInstanceKey</span><span class="sxs-lookup"><span data-stu-id="13b89-103">PidTagInstanceKey Canonical Property</span></span>

  
  
<span data-ttu-id="13b89-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13b89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13b89-105">Содержит значение, однозначно идентифицирующее строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="13b89-105">Contains a value that uniquely identifies a row in a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13b89-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="13b89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13b89-107">ПР_ИНСТАНЦЕ_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="13b89-107">PR_INSTANCE_KEY</span></span>  <br/> |
|<span data-ttu-id="13b89-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="13b89-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13b89-109">0x0FF6</span><span class="sxs-lookup"><span data-stu-id="13b89-109">0x0FF6</span></span>  <br/> |
|<span data-ttu-id="13b89-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="13b89-110">Data type:</span></span>  <br/> |<span data-ttu-id="13b89-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="13b89-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="13b89-112">Область:</span><span class="sxs-lookup"><span data-stu-id="13b89-112">Area:</span></span>  <br/> |<span data-ttu-id="13b89-113">Table</span><span class="sxs-lookup"><span data-stu-id="13b89-113">Table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13b89-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="13b89-114">Remarks</span></span>

<span data-ttu-id="13b89-115">Это свойство является двоичным значением, уникальным образом идентифицирующее строку в представлении таблицы.</span><span class="sxs-lookup"><span data-stu-id="13b89-115">This property is a binary value that uniquely identifies a row in a table view.</span></span> <span data-ttu-id="13b89-116">Это обязательный столбец в большинстве таблиц.</span><span class="sxs-lookup"><span data-stu-id="13b89-116">It is a required column in most tables.</span></span> <span data-ttu-id="13b89-117">Если строка включена в два представления, существует два разных ключа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="13b89-117">If a row is included in two views, there are two different instance keys.</span></span> <span data-ttu-id="13b89-118">Ключ экземпляра строки может различаться при каждом открытии таблицы, но остается неизменным при открытии таблицы.</span><span class="sxs-lookup"><span data-stu-id="13b89-118">The instance key of a row may differ each time the table is opened, but remains constant while the table is open.</span></span> <span data-ttu-id="13b89-119">Строки, добавленные во время использования таблицы, не повторно используют ключ экземпляра, который использовался ранее.</span><span class="sxs-lookup"><span data-stu-id="13b89-119">Rows added while a table is in use do not reuse an instance key that was previously used.</span></span> 
  
<span data-ttu-id="13b89-120">Используйте свойства **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или **пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), чтобы сопоставить все строки расширения.</span><span class="sxs-lookup"><span data-stu-id="13b89-120">Use the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) or **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) properties to correlate all the rows of an expansion.</span></span> <span data-ttu-id="13b89-121">Используйте **пр_инстанце_кэй** для обнаружения определенного экземпляра в развертывании.</span><span class="sxs-lookup"><span data-stu-id="13b89-121">Use **PR_INSTANCE_KEY** to locate a particular instance within the expansion.</span></span> 
  
<span data-ttu-id="13b89-122">Когда многозначное свойство разворачивается в таблице, создается строка для каждого экземпляра расширения, то есть для каждого значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="13b89-122">When a multivalued property is expanded in a table, a row is created for each instance of the expansion, that is, for each value of that property.</span></span> <span data-ttu-id="13b89-123">Каждая строка имеет уникальное значение для свойства **пр_инстанце_кэй** , а все остальные столбцы сохраняют их исходные значения во время расширения.</span><span class="sxs-lookup"><span data-stu-id="13b89-123">Each row has a unique value for the **PR_INSTANCE_KEY** property, while all the other columns retain their original values throughout the expansion.</span></span> 
  
<span data-ttu-id="13b89-124">При сортировке по категории таблицы строки, не соответствующие реальным данным, можно добавлять к результату сортировки.</span><span class="sxs-lookup"><span data-stu-id="13b89-124">In a categorized sort of a table, rows not corresponding to actual data can be added to the result of the sort.</span></span> <span data-ttu-id="13b89-125">Каждая такая строка, как и все строки во всех таблицах, имеет собственный уникальный ключ экземпляра.</span><span class="sxs-lookup"><span data-stu-id="13b89-125">Each such row, like all rows in all tables, has its own unique instance key.</span></span> 
  
 <span data-ttu-id="13b89-126">**Пр_инстанце_кэй** также используется в уведомлениях о событии в табличном виде.</span><span class="sxs-lookup"><span data-stu-id="13b89-126">**PR_INSTANCE_KEY** is also used in table event notifications.</span></span> <span data-ttu-id="13b89-127">Члены **пропиндекс** и **пропприор** структуры [табле_нотификатион](table_notification.md) — [спропвалуе](spropvalue.md) структуры, содержащие **пр_инстанце_кэй** значений.</span><span class="sxs-lookup"><span data-stu-id="13b89-127">The **propIndex** and **propPrior** members of the [TABLE_NOTIFICATION](table_notification.md) structure are [SPropValue](spropvalue.md) structures holding **PR_INSTANCE_KEY** values.</span></span> <span data-ttu-id="13b89-128">Элемент **пропиндекс** указывает строку, которая была добавлена или изменена.</span><span class="sxs-lookup"><span data-stu-id="13b89-128">The **propIndex** member indicates the row that was added or changed.</span></span> <span data-ttu-id="13b89-129">Элемент **пропприор** указывает строку перед добавлением или изменением строки (**пр_нулл** означает изменение первой строки).</span><span class="sxs-lookup"><span data-stu-id="13b89-129">The **propPrior** member indicates the row before the added or changed row (**PR_NULL** indicates a change to the first row).</span></span> 
  
<span data-ttu-id="13b89-130">Это значение не копируется в состав таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="13b89-130">This value is not copied as part of the display table.</span></span> 
  
 <span data-ttu-id="13b89-131">**Пр_инстанце_кэй** — это структура [мапиуид](mapiuid.md) .</span><span class="sxs-lookup"><span data-stu-id="13b89-131">**PR_INSTANCE_KEY** is a [MAPIUID](mapiuid.md) structure.</span></span> <span data-ttu-id="13b89-132">Все ключи экземпляра можно напрямую сравнить с двоичными значениями.</span><span class="sxs-lookup"><span data-stu-id="13b89-132">All instance keys can be directly compared as binary values.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13b89-133">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13b89-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13b89-134">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="13b89-134">Protocol specifications</span></span>

<span data-ttu-id="13b89-135">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b89-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b89-136">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="13b89-136">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13b89-137">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13b89-137">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13b89-138">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13b89-138">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13b89-139">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="13b89-139">Header files</span></span>

<span data-ttu-id="13b89-140">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="13b89-140">Mapidefs.h</span></span>
  
> <span data-ttu-id="13b89-141">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="13b89-141">Provides data type definitions.</span></span>
    
<span data-ttu-id="13b89-142">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="13b89-142">Mapitags.h</span></span>
  
> <span data-ttu-id="13b89-143">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="13b89-143">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13b89-144">См. также</span><span class="sxs-lookup"><span data-stu-id="13b89-144">See also</span></span>



[<span data-ttu-id="13b89-145">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="13b89-145">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13b89-146">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="13b89-146">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13b89-147">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="13b89-147">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13b89-148">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="13b89-148">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

