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
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="2d328-103">Каноническое свойство PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="2d328-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="2d328-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d328-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d328-105">Содержит один или несколько идентификаторов записей элементов, которые участвовали в автоматическом разрешении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="2d328-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="2d328-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2d328-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2d328-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="2d328-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="2d328-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2d328-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2d328-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="2d328-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="2d328-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="2d328-110">Property type:</span></span>  <br/> |<span data-ttu-id="2d328-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d328-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="2d328-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2d328-112">Area:</span></span>  <br/> |<span data-ttu-id="2d328-113">ICS</span><span class="sxs-lookup"><span data-stu-id="2d328-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d328-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d328-114">Remarks</span></span>

<span data-ttu-id="2d328-115">Типы стандартных элементов Microsoft Outlook, поддерживающих автоматическое разрешение конфликтов, включают следующие стандартные типы элементов: элементы встреч, элементы контактов, элементы дневника, элементы почты, элементы собраний, элементы клейких заметок и элементы задач.</span><span class="sxs-lookup"><span data-stu-id="2d328-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="2d328-116">Элемент, принадлежащий классу сообщения, который является производным от одного из этих стандартных типов элементов, также поддерживает автоматическое разрешение конфликтов.</span><span class="sxs-lookup"><span data-stu-id="2d328-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="2d328-117">В Microsoft Outlook 2003 и Microsoft Office Outlook 2007, когда Outlook синхронизирует элементы и считает, что итоговая копия может не содержать все важные данные, Outlook сохраняет конфликтующие копии в папке " **конфликты** " в папке " **ошибки синхронизации** ".</span><span class="sxs-lookup"><span data-stu-id="2d328-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2d328-118">**Проблемы синхронизации** и вложенные папки скрываются до тех пор, пока не будет выбран пункт **список папок** в меню **Перейти** .</span><span class="sxs-lookup"><span data-stu-id="2d328-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="2d328-119">Элемент предоставляет свойство **PR_CONFLICT_ITEMS** , если это один из типов элементов, поддерживающих автоматическое разрешение конфликтов, выиграл разрешение конфликтов или размещается в папке **конфликтов** из-за разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="2d328-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="2d328-120">Содержимое **PR_CONFLICT_ITEMS**определяется папкой, в которой размещается элемент.</span><span class="sxs-lookup"><span data-stu-id="2d328-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="2d328-121">Если элемент находится в папке, отличной от папки **конфликтов** , а элемент предоставляет свойство **PR_CONFLICT_ITEMS** , то элемент должен иметь разрешение конфликтов, а **PR_CONFLICT_ITEMS** будет содержать один или несколько идентификаторов записей этих элементов, потерянных при разрешении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="2d328-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="2d328-122">Если элемент находится в папке **конфликтов** , а элемент предоставляет свойство **PR_CONFLICT_ITEMS** , этот элемент должен потерял разрешение конфликтов, а **PR_CONFLICT_ITEMS** будет содержать идентификатор элемента, который выиграл при разрешении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="2d328-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2d328-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2d328-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2d328-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2d328-124">Protocol specifications</span></span>

<span data-ttu-id="2d328-125">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d328-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d328-126">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2d328-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2d328-127">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2d328-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2d328-128">Обрабатывает синхронизацию данных объекта обмена данными между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="2d328-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2d328-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2d328-129">Header files</span></span>

<span data-ttu-id="2d328-130">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2d328-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="2d328-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2d328-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="2d328-132">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="2d328-132">Mapitags.h</span></span>
  
> <span data-ttu-id="2d328-133">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="2d328-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2d328-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2d328-134">See also</span></span>



[<span data-ttu-id="2d328-135">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="2d328-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="2d328-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2d328-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2d328-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2d328-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2d328-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2d328-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2d328-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2d328-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

