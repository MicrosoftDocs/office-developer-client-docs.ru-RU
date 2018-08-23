---
title: Каноническое свойство PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d376a5219125866f467be01709a6a611ed8d47f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576423"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="9d925-103">Каноническое свойство PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="9d925-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="9d925-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d925-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d925-105">Содержит значение TRUE, если запись в таблице одноразовых можно выбирать.</span><span class="sxs-lookup"><span data-stu-id="9d925-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d925-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9d925-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d925-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="9d925-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="9d925-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9d925-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d925-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="9d925-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="9d925-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9d925-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d925-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9d925-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9d925-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9d925-112">Area:</span></span>  <br/> |<span data-ttu-id="9d925-113">Контейнер адресной книги</span><span class="sxs-lookup"><span data-stu-id="9d925-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d925-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9d925-114">Remarks</span></span>

<span data-ttu-id="9d925-115">Это свойство используется в основном для визуального форматирования одноразовых таблицы.</span><span class="sxs-lookup"><span data-stu-id="9d925-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="9d925-116">Шаблоны могут быть сгруппированы, создав запись, указывающую заголовка для группы.</span><span class="sxs-lookup"><span data-stu-id="9d925-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="9d925-117">Назначить этому свойству значение FALSE для заголовка гарантирует, что пользователь может выбрать только фактическая шаблонов в группе, а не в этой записи заголовка.</span><span class="sxs-lookup"><span data-stu-id="9d925-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="9d925-118">Это свойство применяется только к одноразовых таблицы, не для таблицы иерархии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9d925-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="9d925-119">MAPI позволяет поставщика адресных книг для группировки визуально с двумя способами.</span><span class="sxs-lookup"><span data-stu-id="9d925-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="9d925-120">Во-первых определенные строки могут работать в качестве заголовков, не упустив ни одного.</span><span class="sxs-lookup"><span data-stu-id="9d925-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="9d925-121">Во-вторых доступно для выбора элементов можно отступ относительно их заголовки с помощью свойства **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9d925-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="9d925-122">Это свойство используется в таких группировки для указания ли этот элемент можно выбрать из списка для создания указывает адрес.</span><span class="sxs-lookup"><span data-stu-id="9d925-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="9d925-123">Например если клиент имеет несколько шаблонов для создания адресов факсов, его можно они отображаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9d925-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="9d925-124">Шаблоны ФАКСОВ (глубина 0, не выбирается)</span><span class="sxs-lookup"><span data-stu-id="9d925-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="9d925-125">Локальный (глубина 1, доступно для выбора)</span><span class="sxs-lookup"><span data-stu-id="9d925-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="9d925-126">Звонок из США (глубина 1, доступно для выбора)</span><span class="sxs-lookup"><span data-stu-id="9d925-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9d925-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9d925-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d925-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9d925-128">Protocol specifications</span></span>

<span data-ttu-id="9d925-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d925-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d925-130">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9d925-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d925-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d925-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d925-132">Задает свойства и операции, допустимые для шаблонов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="9d925-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d925-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9d925-133">Header files</span></span>

<span data-ttu-id="9d925-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9d925-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d925-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9d925-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d925-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9d925-136">Mapitags.h</span></span>
  
> <span data-ttu-id="9d925-137">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="9d925-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d925-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9d925-138">See also</span></span>



[<span data-ttu-id="9d925-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="9d925-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="9d925-140">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="9d925-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="9d925-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9d925-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d925-142">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9d925-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d925-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9d925-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d925-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9d925-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

