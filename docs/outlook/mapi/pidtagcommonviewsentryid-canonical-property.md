---
title: Каноническое свойство PidTagCommonViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCommonViewsEntryId
api_type:
- HeaderDef
ms.assetid: cd9e6a46-2112-4663-891e-5e57b22c0950
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e22b8905901f16606614ac918896f3afe0093752
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437345"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="4ed7c-103">Каноническое свойство PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="4ed7c-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4ed7c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ed7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ed7c-105">Содержит идентификатор предварительно определенной папки общего представления.</span><span class="sxs-lookup"><span data-stu-id="4ed7c-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ed7c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4ed7c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4ed7c-107">ПР_КОММОН_ВИЕВС_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="4ed7c-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4ed7c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4ed7c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4ed7c-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="4ed7c-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="4ed7c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4ed7c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4ed7c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4ed7c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4ed7c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4ed7c-112">Area:</span></span>  <br/> |<span data-ttu-id="4ed7c-113">Приложение Outlook</span><span class="sxs-lookup"><span data-stu-id="4ed7c-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ed7c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4ed7c-114">Remarks</span></span>

<span data-ttu-id="4ed7c-115">Папка общего представления содержит предопределенный набор стандартных описателей представлений, в то время как папка представления содержит описатели, определенные пользователем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4ed7c-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="4ed7c-116">Эти папки, которые не отображаются в иерархии взаимосвязанных сообщений (IPM), могут содержать множество описателей представлений, каждый из которых хранится в виде сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ed7c-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="4ed7c-117">Клиентское приложение может объединить два набора описателей и сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="4ed7c-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="4ed7c-118">Дополнительные сведения о представлениях приведены в статье [Просмотр папок](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="4ed7c-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4ed7c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4ed7c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4ed7c-120">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="4ed7c-120">Header files</span></span>

<span data-ttu-id="4ed7c-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="4ed7c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4ed7c-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4ed7c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4ed7c-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="4ed7c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4ed7c-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="4ed7c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ed7c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4ed7c-125">See also</span></span>



[<span data-ttu-id="4ed7c-126">Каноническое свойство PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="4ed7c-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="4ed7c-127">Каноническое свойство PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="4ed7c-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="4ed7c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4ed7c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4ed7c-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="4ed7c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4ed7c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4ed7c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4ed7c-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4ed7c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

