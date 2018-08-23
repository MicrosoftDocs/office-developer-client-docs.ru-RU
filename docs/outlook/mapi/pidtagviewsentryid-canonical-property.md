---
title: Каноническое свойство PidTagViewsEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 73ed7213ea2bd5079458ccc237b65590f06e8d53
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586265"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="97aae-103">Каноническое свойство PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="97aae-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="97aae-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97aae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97aae-105">Содержит идентификатор записи папки пользовательских представлений.</span><span class="sxs-lookup"><span data-stu-id="97aae-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="97aae-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="97aae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="97aae-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="97aae-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="97aae-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="97aae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="97aae-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="97aae-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="97aae-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="97aae-110">Data type:</span></span>  <br/> |<span data-ttu-id="97aae-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="97aae-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="97aae-112">Область:</span><span class="sxs-lookup"><span data-stu-id="97aae-112">Area:</span></span>  <br/> |<span data-ttu-id="97aae-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="97aae-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97aae-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="97aae-114">Remarks</span></span>

<span data-ttu-id="97aae-115">Общие папки представление содержит с предопределенным набором описатели стандартного представления, а представление папки описатели, определенные пользователем, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="97aae-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="97aae-116">Эти папки, которые не отображаются в иерархии электронной почты — это сообщение (IPM), может содержать множество спецификаторы представления, каждая из которых хранятся в виде сообщения.</span><span class="sxs-lookup"><span data-stu-id="97aae-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="97aae-117">В клиентском приложении можно выбрать объединение двух наборов указателей и сделать их оба доступными.</span><span class="sxs-lookup"><span data-stu-id="97aae-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="97aae-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="97aae-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="97aae-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="97aae-119">Header files</span></span>

<span data-ttu-id="97aae-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="97aae-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="97aae-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="97aae-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="97aae-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="97aae-122">Mapitags.h</span></span>
  
> <span data-ttu-id="97aae-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="97aae-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="97aae-124">См. также</span><span class="sxs-lookup"><span data-stu-id="97aae-124">See also</span></span>



[<span data-ttu-id="97aae-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97aae-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="97aae-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="97aae-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="97aae-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="97aae-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="97aae-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="97aae-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

