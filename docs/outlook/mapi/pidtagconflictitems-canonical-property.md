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
ms.openlocfilehash: 61176ec6f9ff00fa5a38a2b385cb5281fa40961e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810920"
---
# <a name="pidtagconflictitems-canonical-property"></a><span data-ttu-id="17702-103">Каноническое свойство PidTagConflictItems</span><span class="sxs-lookup"><span data-stu-id="17702-103">PidTagConflictItems Canonical Property</span></span>

  
  
<span data-ttu-id="17702-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="17702-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="17702-105">Содержит запись один или несколько идентификаторов элементов, участвовавших в автоматического разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="17702-105">Contains one or more entry IDs of items that have been involved in an automatic conflict resolution.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="17702-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="17702-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17702-107">PR_CONFLICT_ITEMS</span><span class="sxs-lookup"><span data-stu-id="17702-107">PR_CONFLICT_ITEMS</span></span>  <br/> |
|<span data-ttu-id="17702-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="17702-108">Identifier:</span></span>  <br/> |<span data-ttu-id="17702-109">0x1098</span><span class="sxs-lookup"><span data-stu-id="17702-109">0x1098</span></span>  <br/> |
|<span data-ttu-id="17702-110">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="17702-110">Property type:</span></span>  <br/> |<span data-ttu-id="17702-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="17702-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="17702-112">Область:</span><span class="sxs-lookup"><span data-stu-id="17702-112">Area:</span></span>  <br/> |<span data-ttu-id="17702-113">ICS</span><span class="sxs-lookup"><span data-stu-id="17702-113">ICS</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17702-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="17702-114">Remarks</span></span>

<span data-ttu-id="17702-115">Типы стандартных элементов Microsoft Outlook, которые поддерживают автоматического разрешения конфликтов включают следующие типы стандартных элементов: элементы встреч, элементов контактов, элементы дневника, почтовых элементов, элементы приглашения, записки элементы и элементы задачи.</span><span class="sxs-lookup"><span data-stu-id="17702-115">The types of standard Microsoft Outlook items that support automatic conflict resolution include the following standard item types: appointment items, contact items, journal items, mail items, meeting items, sticky note items, and task items.</span></span> <span data-ttu-id="17702-116">Элемент, относящегося к класс сообщений, который также является производным от одного из следующих типов стандартных элементов поддерживает автоматического разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="17702-116">An item belonging to a message class that derives from one of these standard item types also supports automatic conflict resolution.</span></span> <span data-ttu-id="17702-117">В Microsoft Outlook 2003 и Microsoft Office Outlook 2007 когда Outlook синхронизирует элементов и считает, что есть вероятность, что результирующее копии не может содержать все необходимые данные Outlook хранятся конфликтующие копий в **конфликтов** Папка, в папке **Ошибки синхронизации** .</span><span class="sxs-lookup"><span data-stu-id="17702-117">In Microsoft Outlook 2003 and Microsoft Office Outlook 2007, when Outlook synchronizes items and considers that there is a possibility that the resultant copy may not contain all essential data, Outlook stores the conflicting copies in the **Conflicts** folder, under the **Sync Issues** folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="17702-118">**Ошибки синхронизации** и вложенные в нее папки скрыты до выберите **Список папок** в меню **Перейти** .</span><span class="sxs-lookup"><span data-stu-id="17702-118">**Sync Issues** and its subfolders are hidden until you click **Folder List** on the **Go** menu.</span></span> 
  
<span data-ttu-id="17702-119">Элемент предоставляет свойство **PR_CONFLICT_ITEMS** , если — это один из типов элементов, которые поддерживают автоматического разрешения конфликтов, Вона разрешения конфликтов или помещен в папку **конфликтов** из-за разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="17702-119">An item exposes the **PR_CONFLICT_ITEMS** property if it is one of the item types that support automatic conflict resolution, has won in a conflict resolution, or was placed in the **Conflicts** folder because of a conflict resolution.</span></span> <span data-ttu-id="17702-120">Папка, в которой размещен элемент определяет содержимое **PR_CONFLICT_ITEMS**.</span><span class="sxs-lookup"><span data-stu-id="17702-120">The folder in which the item is placed determines the content of **PR_CONFLICT_ITEMS**.</span></span> <span data-ttu-id="17702-121">Если элемент находится в некоторые папки кроме папки " **конфликты** " и элемент предоставляет свойство **PR_CONFLICT_ITEMS** , элемент должен Вона разрешения конфликтов и **PR_CONFLICT_ITEMS** будет содержать один или несколько идентификаторов запись из элементы, которые утеряны разрешения конфликтов.</span><span class="sxs-lookup"><span data-stu-id="17702-121">If the item is located in some folder other than the **Conflicts** folder, and the item exposes the **PR_CONFLICT_ITEMS** property, the item must have won the conflict resolution, and **PR_CONFLICT_ITEMS** would contain one or more entry IDs of those items that lost in the conflict resolution.</span></span> <span data-ttu-id="17702-122">Если элемент находится в папке **конфликтов** и элемент предоставляет свойство **PR_CONFLICT_ITEMS** , этот элемент должен утеряны разрешения конфликтов и **PR_CONFLICT_ITEMS** будет содержать идентификатор записи элемента, который Вона в конфликт решение.</span><span class="sxs-lookup"><span data-stu-id="17702-122">If the item is located in the **Conflicts** folder and the item exposes the **PR_CONFLICT_ITEMS** property, this item must have lost the conflict resolution, and **PR_CONFLICT_ITEMS** would contain the entry ID of the item that won in the conflict resolution.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="17702-123">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="17702-123">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17702-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="17702-124">Protocol specifications</span></span>

<span data-ttu-id="17702-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17702-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17702-126">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="17702-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17702-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17702-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17702-128">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="17702-128">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17702-129">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="17702-129">Header files</span></span>

<span data-ttu-id="17702-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17702-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="17702-131">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="17702-131">Provides data type definitions.</span></span>
    
<span data-ttu-id="17702-132">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="17702-132">Mapitags.h</span></span>
  
> <span data-ttu-id="17702-133">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="17702-133">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17702-134">См. также</span><span class="sxs-lookup"><span data-stu-id="17702-134">See also</span></span>



[<span data-ttu-id="17702-135">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="17702-135">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="17702-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="17702-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17702-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="17702-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17702-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="17702-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17702-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="17702-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

