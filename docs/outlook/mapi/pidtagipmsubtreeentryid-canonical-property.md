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
ms.openlocfilehash: 9635c06ffa5638e370312e3b2b29e0c98161a766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811274"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="073e7-103">Каноническое свойство PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="073e7-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="073e7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="073e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="073e7-105">Содержит идентификатор записи корня поддерево папки электронной почты — это сообщение (IPM) в дереве папки хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="073e7-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="073e7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="073e7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="073e7-107">PR_IPM_SUBTREE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="073e7-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="073e7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="073e7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="073e7-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="073e7-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="073e7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="073e7-110">Data type:</span></span>  <br/> |<span data-ttu-id="073e7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="073e7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="073e7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="073e7-112">Area:</span></span>  <br/> |<span data-ttu-id="073e7-113">Folder</span><span class="sxs-lookup"><span data-stu-id="073e7-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="073e7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="073e7-114">Remarks</span></span>

<span data-ttu-id="073e7-115">Это свойство представляет корень иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="073e7-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="073e7-116">IPM клиенты не должны отображаться какие-либо папки, которые не являются вложенные папки, представленного в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="073e7-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="073e7-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="073e7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="073e7-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="073e7-118">Header files</span></span>

<span data-ttu-id="073e7-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="073e7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="073e7-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="073e7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="073e7-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="073e7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="073e7-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="073e7-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="073e7-123">См. также</span><span class="sxs-lookup"><span data-stu-id="073e7-123">See also</span></span>



[<span data-ttu-id="073e7-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="073e7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="073e7-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="073e7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="073e7-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="073e7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="073e7-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="073e7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

