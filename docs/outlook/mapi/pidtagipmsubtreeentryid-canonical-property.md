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
# <a name="pidtagipmsubtreeentryid-canonical-property"></a><span data-ttu-id="82866-103">Каноническое свойство PidTagIpmSubtreeEntryId</span><span class="sxs-lookup"><span data-stu-id="82866-103">PidTagIpmSubtreeEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="82866-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82866-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82866-105">Содержит идентификатор корня поддерева папки межконтактного сообщения (IPM) в дереве папок хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="82866-105">Contains the entry identifier of the root of the interpersonal message (IPM) folder subtree in the message store's folder tree.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82866-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="82866-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82866-107">ПР_ИПМ_СУБТРИ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="82866-107">PR_IPM_SUBTREE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="82866-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="82866-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82866-109">0x35E0</span><span class="sxs-lookup"><span data-stu-id="82866-109">0x35E0</span></span>  <br/> |
|<span data-ttu-id="82866-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="82866-110">Data type:</span></span>  <br/> |<span data-ttu-id="82866-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="82866-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="82866-112">Область:</span><span class="sxs-lookup"><span data-stu-id="82866-112">Area:</span></span>  <br/> |<span data-ttu-id="82866-113">Folder</span><span class="sxs-lookup"><span data-stu-id="82866-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82866-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="82866-114">Remarks</span></span>

<span data-ttu-id="82866-115">Это свойство представляет корень иерархии IPM.</span><span class="sxs-lookup"><span data-stu-id="82866-115">This property represents the root of the IPM hierarchy.</span></span> <span data-ttu-id="82866-116">Клиенты IPM не должны отображать папки, которые не являются подпапками папки, представленной этим свойством.</span><span class="sxs-lookup"><span data-stu-id="82866-116">IPM clients should not display any folders that are not subfolders of the folder represented by this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="82866-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82866-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="82866-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="82866-118">Header files</span></span>

<span data-ttu-id="82866-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="82866-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="82866-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="82866-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="82866-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="82866-121">Mapitags.h</span></span>
  
> <span data-ttu-id="82866-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="82866-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82866-123">См. также</span><span class="sxs-lookup"><span data-stu-id="82866-123">See also</span></span>



[<span data-ttu-id="82866-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="82866-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82866-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="82866-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82866-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="82866-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82866-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="82866-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

