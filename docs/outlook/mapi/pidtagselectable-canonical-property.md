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
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359019"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="f1fa7-103">Каноническое свойство PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="f1fa7-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="f1fa7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1fa7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1fa7-105">Содержит значение TRUE, если можно выбрать запись в таблице "одноразовый".</span><span class="sxs-lookup"><span data-stu-id="f1fa7-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1fa7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f1fa7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1fa7-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="f1fa7-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="f1fa7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f1fa7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1fa7-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="f1fa7-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="f1fa7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f1fa7-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1fa7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f1fa7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f1fa7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f1fa7-112">Area:</span></span>  <br/> |<span data-ttu-id="f1fa7-113">Контейнер адресной книги</span><span class="sxs-lookup"><span data-stu-id="f1fa7-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1fa7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1fa7-114">Remarks</span></span>

<span data-ttu-id="f1fa7-115">Это свойство используется в основном для визуального форматирования одноразовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="f1fa7-116">Шаблоны можно группировать, создавая запись, которая указывает заголовок для группы.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="f1fa7-117">Если задать для этого свойства значение FALSE для заголовка, пользователь сможет выбрать только шаблоны в группе, а не запись заголовка.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="f1fa7-118">Это свойство применяется только к одноразовой таблице, а не к таблице иерархий адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="f1fa7-119">MAPI позволяет поставщику адресных книг группировать элементы в визуальном виде с двумя способами.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="f1fa7-120">Во – первых, определенные строки могут работать в качестве заголовков, не выделять их.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="f1fa7-121">Во-вторых, доступные для выбора элементы могут относиться к своим заголовкам с помощью свойства **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f1fa7-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="f1fa7-122">Это свойство используется в такой группе, чтобы указать, можно ли выбрать этот элемент из списка для создания одноразового адреса.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="f1fa7-123">Например, если у клиента есть несколько шаблонов для создания адресов факса, они могут отображаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f1fa7-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="f1fa7-124">Шаблоны факсов (глубина 0, Невыбираемая)</span><span class="sxs-lookup"><span data-stu-id="f1fa7-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="f1fa7-125">Local (глубина 1, выбираемая)</span><span class="sxs-lookup"><span data-stu-id="f1fa7-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="f1fa7-126">Междугородный (глубина 1, выбираемая)</span><span class="sxs-lookup"><span data-stu-id="f1fa7-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f1fa7-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f1fa7-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1fa7-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f1fa7-128">Protocol specifications</span></span>

<span data-ttu-id="f1fa7-129">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fa7-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fa7-130">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1fa7-131">[[MS — ОКСОАБКТ]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1fa7-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1fa7-132">Задает свойства и операции, допустимые для шаблонов адресных книг.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1fa7-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f1fa7-133">Header files</span></span>

<span data-ttu-id="f1fa7-134">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f1fa7-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1fa7-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1fa7-136">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f1fa7-136">Mapitags.h</span></span>
  
> <span data-ttu-id="f1fa7-137">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="f1fa7-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1fa7-138">См. также</span><span class="sxs-lookup"><span data-stu-id="f1fa7-138">See also</span></span>



[<span data-ttu-id="f1fa7-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="f1fa7-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="f1fa7-140">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="f1fa7-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="f1fa7-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f1fa7-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1fa7-142">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f1fa7-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1fa7-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f1fa7-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1fa7-144">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f1fa7-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

