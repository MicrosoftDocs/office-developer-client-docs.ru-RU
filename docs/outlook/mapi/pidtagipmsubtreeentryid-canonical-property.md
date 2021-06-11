---
title: Каноническое свойство PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412732"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="2f677-103">Каноническое свойство PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="2f677-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2f677-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f677-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f677-105">Содержит идентификатор входа корневого подтриба папки межличностного сообщения (IPM) в дереве папки магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f677-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2f677-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2f677-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2f677-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2f677-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2f677-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2f677-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2f677-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="2f677-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="2f677-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2f677-110">Data type:</span></span>  <br/> |<span data-ttu-id="2f677-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2f677-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2f677-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2f677-112">Area:</span></span>  <br/> |<span data-ttu-id="2f677-113">Folder</span><span class="sxs-lookup"><span data-stu-id="2f677-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2f677-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f677-114">Remarks</span></span>

<span data-ttu-id="2f677-115">Это свойство представляет корень иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="2f677-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="2f677-116">Клиенты IPM не должны отображать папки, не вложенные в папку, представленную этим свойством.</span><span class="sxs-lookup"><span data-stu-id="2f677-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2f677-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2f677-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2f677-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="2f677-118">Header files</span></span>

<span data-ttu-id="2f677-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2f677-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2f677-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2f677-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2f677-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2f677-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2f677-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="2f677-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2f677-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2f677-123">See also</span></span>



[<span data-ttu-id="2f677-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f677-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2f677-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2f677-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2f677-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2f677-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2f677-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="2f677-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

