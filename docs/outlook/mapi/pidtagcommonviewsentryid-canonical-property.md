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
ms.openlocfilehash: 7449e59227b147d34c2329175d0251dbb9c427b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581344"
---
# <a name="pidtagcommonviewsentryid-canonical-property"></a><span data-ttu-id="4cf30-103">Каноническое свойство PidTagCommonViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="4cf30-103">PidTagCommonViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="4cf30-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cf30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cf30-105">Содержит идентификатор записи предварительно определенные общие папки представления.</span><span class="sxs-lookup"><span data-stu-id="4cf30-105">Contains the entry identifier of the predefined common view folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cf30-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4cf30-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4cf30-107">PR_COMMON_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="4cf30-107">PR_COMMON_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="4cf30-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4cf30-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4cf30-109">0x35E6</span><span class="sxs-lookup"><span data-stu-id="4cf30-109">0x35E6</span></span>  <br/> |
|<span data-ttu-id="4cf30-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4cf30-110">Data type:</span></span>  <br/> |<span data-ttu-id="4cf30-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4cf30-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4cf30-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4cf30-112">Area:</span></span>  <br/> |<span data-ttu-id="4cf30-113">Приложения Outlook</span><span class="sxs-lookup"><span data-stu-id="4cf30-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cf30-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4cf30-114">Remarks</span></span>

<span data-ttu-id="4cf30-115">Общие папки представление содержит с предопределенным набором описатели стандартного представления, а представление папки описатели, определенные пользователем, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4cf30-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="4cf30-116">Эти папки, которые не отображаются в иерархии электронной почты — это сообщение (IPM), может содержать множество спецификаторы представления, каждая из которых хранятся в виде сообщения.</span><span class="sxs-lookup"><span data-stu-id="4cf30-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="4cf30-117">Клиентское приложение можно выбрать объединение двух наборов указателей и сделать их оба доступными.</span><span class="sxs-lookup"><span data-stu-id="4cf30-117">A client application can choose to merge the two sets of specifiers and make them both available.</span></span> 
  
<span data-ttu-id="4cf30-118">Дополнительные сведения о представлениях содержатся [Представления папок](mapi-view-folders.md).</span><span class="sxs-lookup"><span data-stu-id="4cf30-118">For more information on views, see [View Folders](mapi-view-folders.md).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4cf30-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4cf30-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4cf30-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4cf30-120">Header files</span></span>

<span data-ttu-id="4cf30-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4cf30-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4cf30-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4cf30-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4cf30-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4cf30-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4cf30-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="4cf30-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4cf30-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4cf30-125">See also</span></span>



[<span data-ttu-id="4cf30-126">Каноническое свойство PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="4cf30-126">PidTagDefaultViewEntryId Canonical Property</span></span>](pidtagdefaultviewentryid-canonical-property.md)
  
[<span data-ttu-id="4cf30-127">Каноническое свойство PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="4cf30-127">PidTagViewsEntryId Canonical Property</span></span>](pidtagviewsentryid-canonical-property.md)


[<span data-ttu-id="4cf30-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4cf30-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4cf30-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4cf30-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4cf30-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4cf30-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4cf30-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4cf30-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

