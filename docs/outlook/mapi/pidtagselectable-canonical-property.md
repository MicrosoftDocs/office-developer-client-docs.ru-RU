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
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="3d0fb-103">Каноническое свойство PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="3d0fb-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="3d0fb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d0fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d0fb-105">Содержит TRUE, если можно выбрать запись в разовой таблице.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d0fb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3d0fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d0fb-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="3d0fb-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="3d0fb-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3d0fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d0fb-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="3d0fb-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="3d0fb-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3d0fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d0fb-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="3d0fb-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="3d0fb-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3d0fb-112">Area:</span></span>  <br/> |<span data-ttu-id="3d0fb-113">Контейнер адресной книги</span><span class="sxs-lookup"><span data-stu-id="3d0fb-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d0fb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d0fb-114">Remarks</span></span>

<span data-ttu-id="3d0fb-115">Это свойство используется в основном для визуального форматирования разовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="3d0fb-116">Шаблоны можно сгруппить, создав запись, которая указывает заголовок для группы.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="3d0fb-117">Настройка этого свойства false для заголовка гарантирует, что пользователь может выбрать только фактические шаблоны в группе, а не эту запись заголовка.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="3d0fb-118">Это свойство применяется только к разовой таблице, а не к таблице иерархии адресных книг.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="3d0fb-119">MAPI позволяет поставщику адресных книг визуально группировать элементы двумя средствами.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="3d0fb-120">Во-первых, некоторые строки могут функционировать в качестве заголовков, будучи неизбираемыми.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="3d0fb-121">Во-вторых, выбранные элементы могут быть отступлены по отношению к их заголовкам с помощью **свойства PR_DEPTH** [(PidTagDepth).](pidtagdepth-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="3d0fb-122">Это свойство используется в такой группировке, чтобы указать, можно ли выбрать этот элемент из списка для создания разового адреса.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="3d0fb-123">Например, если клиент имеет несколько шаблонов для создания факсимили, он может отображать их следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3d0fb-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="3d0fb-124">Шаблоны ФАКС (глубина 0, не выбрана)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="3d0fb-125">Локальный (глубина 1, выбор)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="3d0fb-126">Междугородние (глубина 1, выборка)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d0fb-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d0fb-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d0fb-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3d0fb-128">Protocol specifications</span></span>

<span data-ttu-id="3d0fb-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0fb-130">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d0fb-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d0fb-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d0fb-132">Указывает свойства и операции, допустимые для шаблонов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d0fb-133">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="3d0fb-133">Header files</span></span>

<span data-ttu-id="3d0fb-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d0fb-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d0fb-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d0fb-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d0fb-136">Mapitags.h</span></span>
  
> <span data-ttu-id="3d0fb-137">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="3d0fb-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d0fb-138">См. также</span><span class="sxs-lookup"><span data-stu-id="3d0fb-138">See also</span></span>



[<span data-ttu-id="3d0fb-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="3d0fb-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="3d0fb-140">Каноническое свойство PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="3d0fb-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="3d0fb-141">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d0fb-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d0fb-142">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d0fb-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d0fb-143">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3d0fb-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d0fb-144">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="3d0fb-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

