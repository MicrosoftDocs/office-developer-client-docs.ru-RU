---
title: Каноническое свойство PidTagConflictItems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConflictItems
api_type:
- HeaderDef
ms.assetid: 0d147827-f0e2-dcc1-4427-c4a2f48ca801
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 83940d9239bc172d5fab76232f6644f0e89033b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338019"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="4d685-103">Каноническое свойство PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="4d685-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="4d685-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d685-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d685-105">Содержит один или несколько входных ИД элементов, которые были вовлечены в автоматическое разрешение конфликтов.</span><span class="sxs-lookup"><span data-stu-id="4d685-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="4d685-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4d685-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d685-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="4d685-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="4d685-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4d685-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d685-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="4d685-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="4d685-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="4d685-110">Property type:</span></span>  <br/> |<span data-ttu-id="4d685-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4d685-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="4d685-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4d685-112">Area:</span></span>  <br/> |<span data-ttu-id="4d685-113">ICS</span><span class="sxs-lookup"><span data-stu-id="4d685-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d685-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d685-114">Remarks</span></span>

<span data-ttu-id="4d685-115">Типы стандартных элементов Microsoft Outlook, которые поддерживают автоматическое разрешение конфликтов, включают следующие стандартные типы элементов: пункты назначения, контактные элементы, элементы журнала, элементы почты, элементы собраний, липкие элементы заметки и элементы задач.</span><span class="sxs-lookup"><span data-stu-id="4d685-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="4d685-116">Элемент, принадлежащий классу сообщений, который происходит из одного из этих стандартных типов элементов, также поддерживает автоматическое разрешение конфликтов.</span><span class="sxs-lookup"><span data-stu-id="4d685-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="4d685-117">В Microsoft Outlook 2003 и Microsoft Office Outlook 2007 г., когда Outlook синхронизирует элементы и считает, что существует вероятность того, что результатовая копия может содержать не все необходимые данные, Outlook хранит конфликтующие копии в папке **Conflicts,** в папке **Sync Issues.**</span><span class="sxs-lookup"><span data-stu-id="4d685-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4d685-118">**Проблемы синхронизации и** его подмостки скрыты до тех пор, пока вы не нажмете список папок **в** меню **Go.**</span><span class="sxs-lookup"><span data-stu-id="4d685-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="4d685-119">Элемент предоставляет свойство **PR_CONFLICT_ITEMS,** если это один из типов элементов, которые поддерживают автоматическое разрешение конфликтов, выиграли в разрешении конфликтов или были помещены в папку **Conflicts** из-за разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="4d685-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="4d685-120">Папка, в которой размещен элемент, определяет содержимое **PR_CONFLICT_ITEMS.**</span><span class="sxs-lookup"><span data-stu-id="4d685-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="4d685-121">Если элемент находится в какой-либо папке, кроме папки **Conflicts,** и элемент предоставляет свойство **PR_CONFLICT_ITEMS,** элемент должен  был выиграть разрешение конфликтов, а PR_CONFLICT_ITEMS будет содержать один или несколько входных ИД тех элементов, которые были потеряны в разрешении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="4d685-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="4d685-122">Если элемент находится в папке **Conflict** и элемент предоставляет свойство **PR_CONFLICT_ITEMS,** этот элемент должен был потерять  разрешение конфликта, и PR_CONFLICT_ITEMS будет содержать входной ID элемента, выигранного в разрешении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="4d685-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4d685-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4d685-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4d685-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4d685-124">Protocol specifications</span></span>

<span data-ttu-id="4d685-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d685-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d685-126">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="4d685-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4d685-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d685-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4d685-128">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="4d685-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4d685-129">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4d685-129">Header files</span></span>

<span data-ttu-id="4d685-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d685-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d685-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4d685-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d685-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d685-132">Mapitags.h</span></span>
  
> <span data-ttu-id="4d685-133">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4d685-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d685-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4d685-134">See also</span></span>



[<span data-ttu-id="4d685-135">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="4d685-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="4d685-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4d685-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d685-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4d685-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d685-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4d685-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d685-139">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4d685-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

