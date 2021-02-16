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
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427313"
---
# <a name="pidtagviewsentryid-canonical-property"></a><span data-ttu-id="c8a67-103">Каноническое свойство PidTagViewsEntryId</span><span class="sxs-lookup"><span data-stu-id="c8a67-103">PidTagViewsEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="c8a67-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8a67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8a67-105">Содержит идентификатор записи для папки пользовательских представлений.</span><span class="sxs-lookup"><span data-stu-id="c8a67-105">Contains the entry identifier of the user-defined Views folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c8a67-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c8a67-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c8a67-107">PR_VIEWS_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c8a67-107">PR_VIEWS_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="c8a67-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c8a67-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c8a67-109">0x35E5</span><span class="sxs-lookup"><span data-stu-id="c8a67-109">0x35E5</span></span>  <br/> |
|<span data-ttu-id="c8a67-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c8a67-110">Data type:</span></span>  <br/> |<span data-ttu-id="c8a67-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c8a67-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c8a67-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c8a67-112">Area:</span></span>  <br/> |<span data-ttu-id="c8a67-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="c8a67-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8a67-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8a67-114">Remarks</span></span>

<span data-ttu-id="c8a67-115">Общая папка представления содержит предварительно определенный набор стандартных определителей представления, а папка представления содержит определители, определенные пользователем системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c8a67-115">The common view folder contains a predefined set of standard view specifiers, while the view folder contains specifiers defined by a messaging user.</span></span> <span data-ttu-id="c8a67-116">В этих папках, которые не видны в иерархии межличностных сообщений (IPM), может храниться множество о указаний представления, каждая из которых хранится в качестве сообщения.</span><span class="sxs-lookup"><span data-stu-id="c8a67-116">These folders, which are not visible in the interpersonal message (IPM) hierarchy, can hold many view specifiers, each one stored as a message.</span></span> <span data-ttu-id="c8a67-117">Клиентские приложения могут объединить два набора о указаний и сделать их доступными.</span><span class="sxs-lookup"><span data-stu-id="c8a67-117">The client application can choose to merge the two sets of specifiers and make them both available.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8a67-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c8a67-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c8a67-119">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c8a67-119">Header files</span></span>

<span data-ttu-id="c8a67-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8a67-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8a67-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c8a67-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="c8a67-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c8a67-122">Mapitags.h</span></span>
  
> <span data-ttu-id="c8a67-123">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c8a67-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8a67-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c8a67-124">See also</span></span>



[<span data-ttu-id="c8a67-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8a67-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8a67-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8a67-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8a67-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c8a67-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8a67-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c8a67-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

