---
title: Каноническое свойство PidTagSearchFolderTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b7a88387-72ff-49e5-b73a-8bafab635658
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a4ad72c147abebfe9863d19690bc9f27f00544a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282322"
---
# <a name="pidtagsearchfoldertag-canonical-property"></a><span data-ttu-id="f2cb9-103">Каноническое свойство PidTagSearchFolderTag</span><span class="sxs-lookup"><span data-stu-id="f2cb9-103">PidTagSearchFolderTag Canonical Property</span></span>

  
  
<span data-ttu-id="f2cb9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2cb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2cb9-105">Содержит значение, используемое для синхронизации этого сообщения определения с подходящим контейнером папок поиска.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-105">Contains the value used to synchronize this definition message with the matching search folder container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2cb9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f2cb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2cb9-107">PR_WB_SF_TAG</span><span class="sxs-lookup"><span data-stu-id="f2cb9-107">PR_WB_SF_TAG</span></span>  <br/> |
|<span data-ttu-id="f2cb9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f2cb9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2cb9-109">0x6847</span><span class="sxs-lookup"><span data-stu-id="f2cb9-109">0x6847</span></span>  <br/> |
|<span data-ttu-id="f2cb9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f2cb9-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2cb9-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f2cb9-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f2cb9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f2cb9-112">Area:</span></span>  <br/> |<span data-ttu-id="f2cb9-113">Поиск</span><span class="sxs-lookup"><span data-stu-id="f2cb9-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2cb9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2cb9-114">Remarks</span></span>

<span data-ttu-id="f2cb9-115">Это свойство изменяется при изменении сообщения определения.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-115">This property is changed when the definition message is changed.</span></span> <span data-ttu-id="f2cb9-116">Он должен изменить каждую итерацию, но может быть не уникальным.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-116">It must change each iteration, but it may not be unique.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2cb9-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f2cb9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2cb9-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f2cb9-118">Protocol specifications</span></span>

<span data-ttu-id="f2cb9-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2cb9-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2cb9-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2cb9-121">[[MS — ОКСОСРЧ]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2cb9-121">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2cb9-122">Задает свойства и операции для управления конфигурацией списка папок поиска.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-122">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2cb9-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f2cb9-123">Header files</span></span>

<span data-ttu-id="f2cb9-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f2cb9-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2cb9-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2cb9-126">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f2cb9-126">Mapitags.h</span></span>
  
> <span data-ttu-id="f2cb9-127">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="f2cb9-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2cb9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f2cb9-128">See also</span></span>



[<span data-ttu-id="f2cb9-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f2cb9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2cb9-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f2cb9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2cb9-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f2cb9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2cb9-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f2cb9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

