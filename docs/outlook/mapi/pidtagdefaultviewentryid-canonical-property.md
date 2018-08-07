---
title: Каноническое свойство PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0db245efdd8aad73b0c094c35079f50925ca4478
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811046"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a><span data-ttu-id="561c4-103">Каноническое свойство PidTagDefaultViewEntryId</span><span class="sxs-lookup"><span data-stu-id="561c4-103">PidTagDefaultViewEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="561c4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="561c4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="561c4-105">Содержит идентификатор записи представления по умолчанию папки.</span><span class="sxs-lookup"><span data-stu-id="561c4-105">Contains the entry identifier of a folder's default view.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="561c4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="561c4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="561c4-107">PR_DEFAULT_VIEW_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="561c4-107">PR_DEFAULT_VIEW_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="561c4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="561c4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="561c4-109">0x3616</span><span class="sxs-lookup"><span data-stu-id="561c4-109">0x3616</span></span>  <br/> |
|<span data-ttu-id="561c4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="561c4-110">Data type:</span></span>  <br/> |<span data-ttu-id="561c4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="561c4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="561c4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="561c4-112">Area:</span></span>  <br/> |<span data-ttu-id="561c4-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="561c4-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="561c4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="561c4-114">Remarks</span></span>

<span data-ttu-id="561c4-115">Это свойство соответствует записи идентификатор представления папок, который следует задать как начальное представление.</span><span class="sxs-lookup"><span data-stu-id="561c4-115">This property is the entry identifier of the folder view that should be set as the initial view.</span></span> <span data-ttu-id="561c4-116">Не требуется набора свойств, если представление «Обычный» для использования в качестве начальное представление.</span><span class="sxs-lookup"><span data-stu-id="561c4-116">The property need not be set if the "Normal" view is to be used as the initial view.</span></span>
  
<span data-ttu-id="561c4-117">Клиентское приложение может получить это свойство во время, когда она открывается папку и реализовать существенно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="561c4-117">A client application can obtain this property at the time it opens the folder and realize significant performance gains.</span></span> <span data-ttu-id="561c4-118">Это свойство можно использовать для быстрого получить представление по умолчанию, вместо открытия связанного содержимого таблицы и отправка ограничение.</span><span class="sxs-lookup"><span data-stu-id="561c4-118">This property can be used as a shortcut to obtain the default view, instead of opening the associated contents table and submitting a restriction.</span></span>
  
<span data-ttu-id="561c4-119">Реализация поставщика службы метода [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) можно скопировать это свойство, при копировании папки.</span><span class="sxs-lookup"><span data-stu-id="561c4-119">A service provider implementation of the [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) method can copy this property when it copies folders.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="561c4-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="561c4-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="561c4-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="561c4-121">Protocol specifications</span></span>

<span data-ttu-id="561c4-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="561c4-122">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="561c4-123">Обрабатывает операции папки.</span><span class="sxs-lookup"><span data-stu-id="561c4-123">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="561c4-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="561c4-124">Header files</span></span>

<span data-ttu-id="561c4-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="561c4-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="561c4-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="561c4-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="561c4-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="561c4-127">Mapitags.h</span></span>
  
> <span data-ttu-id="561c4-128">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="561c4-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="561c4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="561c4-129">See also</span></span>



[<span data-ttu-id="561c4-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="561c4-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="561c4-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="561c4-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="561c4-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="561c4-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="561c4-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="561c4-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

