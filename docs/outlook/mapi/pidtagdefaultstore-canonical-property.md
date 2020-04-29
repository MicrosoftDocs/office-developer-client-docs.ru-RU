---
title: Каноническое свойство PidTagDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0cbcc8185f6f46a1bfceb2dd6d0aaf9c5d7cab2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270107"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="dcf45-103">Каноническое свойство PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="dcf45-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="dcf45-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcf45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcf45-105">Содержит значение TRUE, если хранилище сообщений является хранилищем сообщений по умолчанию в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="dcf45-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dcf45-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dcf45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dcf45-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="dcf45-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="dcf45-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dcf45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dcf45-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="dcf45-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="dcf45-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dcf45-110">Data type:</span></span>  <br/> |<span data-ttu-id="dcf45-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="dcf45-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="dcf45-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dcf45-112">Area:</span></span>  <br/> |<span data-ttu-id="dcf45-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="dcf45-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcf45-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="dcf45-114">Remarks</span></span>

<span data-ttu-id="dcf45-115">Это свойство отображается в виде столбца в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="dcf45-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="dcf45-116">Значение основано на **PR_RESOURCE_FLAGSе** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="dcf45-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dcf45-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dcf45-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dcf45-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dcf45-118">Protocol specifications</span></span>

<span data-ttu-id="dcf45-119">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dcf45-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dcf45-120">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dcf45-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dcf45-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="dcf45-121">Header files</span></span>

<span data-ttu-id="dcf45-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="dcf45-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="dcf45-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dcf45-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="dcf45-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="dcf45-124">Mapitags.h</span></span>
  
> <span data-ttu-id="dcf45-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="dcf45-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dcf45-126">См. также</span><span class="sxs-lookup"><span data-stu-id="dcf45-126">See also</span></span>



[<span data-ttu-id="dcf45-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dcf45-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dcf45-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="dcf45-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dcf45-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dcf45-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dcf45-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dcf45-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

