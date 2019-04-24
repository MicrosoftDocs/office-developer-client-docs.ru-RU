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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327875"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="0a151-103">Каноническое свойство PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="0a151-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="0a151-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a151-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a151-105">Содержит идентификатор корня поддерева папки межконтактного сообщения (IPM) в дереве папок хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="0a151-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a151-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0a151-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0a151-107">ПР_ИПМ_СУБТРИ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="0a151-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="0a151-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0a151-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0a151-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="0a151-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="0a151-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0a151-110">Data type:</span></span>  <br/> |<span data-ttu-id="0a151-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0a151-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0a151-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0a151-112">Area:</span></span>  <br/> |<span data-ttu-id="0a151-113">Folder</span><span class="sxs-lookup"><span data-stu-id="0a151-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a151-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a151-114">Remarks</span></span>

<span data-ttu-id="0a151-115">Это свойство представляет корень иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="0a151-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="0a151-116">Клиенты IPM не должны отображать папки, которые не являются подпапками папки, представленной этим свойством.</span><span class="sxs-lookup"><span data-stu-id="0a151-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0a151-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0a151-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0a151-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="0a151-118">Header files</span></span>

<span data-ttu-id="0a151-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="0a151-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0a151-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0a151-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0a151-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="0a151-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0a151-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="0a151-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0a151-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0a151-123">See also</span></span>



[<span data-ttu-id="0a151-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0a151-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0a151-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="0a151-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0a151-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0a151-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0a151-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0a151-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

