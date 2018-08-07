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
ms.openlocfilehash: 1980e3bd815b370f125f4449dd7b7f340a7dcb9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812034"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="b0d40-103">Каноническое свойство PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="b0d40-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="b0d40-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0d40-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0d40-105">Содержит идентификатор записи папки пользовательских представлений.</span><span class="sxs-lookup"><span data-stu-id="b0d40-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0d40-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b0d40-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0d40-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b0d40-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="b0d40-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b0d40-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0d40-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="b0d40-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="b0d40-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b0d40-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0d40-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b0d40-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b0d40-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b0d40-112">Area:</span></span>  <br/> |<span data-ttu-id="b0d40-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d40-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0d40-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b0d40-114">Remarks</span></span>

<span data-ttu-id="b0d40-115">Общие папки представление содержит с предопределенным набором описатели стандартного представления, а представление папки описатели, определенные пользователем, обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b0d40-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="b0d40-116">Эти папки, которые не отображаются в иерархии электронной почты — это сообщение (IPM), может содержать множество спецификаторы представления, каждая из которых хранятся в виде сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0d40-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="b0d40-117">В клиентском приложении можно выбрать объединение двух наборов указателей и сделать их оба доступными.</span><span class="sxs-lookup"><span data-stu-id="b0d40-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0d40-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b0d40-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b0d40-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b0d40-119">Header files</span></span>

<span data-ttu-id="b0d40-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0d40-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0d40-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b0d40-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0d40-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b0d40-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b0d40-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b0d40-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0d40-124">См. также</span><span class="sxs-lookup"><span data-stu-id="b0d40-124">See also</span></span>



[<span data-ttu-id="b0d40-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d40-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0d40-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d40-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0d40-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d40-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0d40-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b0d40-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

