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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385167"
---
# <a name="pidtagdefaultstore-canonical-property"></a><span data-ttu-id="6cd44-103">Каноническое свойство PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="6cd44-103">PidTagDefaultStore Canonical Property</span></span>

  
  
<span data-ttu-id="6cd44-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cd44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cd44-105">Содержит значение TRUE, если хранилища сообщений — это хранилище сообщений по умолчанию в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cd44-105">Contains TRUE if a message store is the default message store in the message store table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cd44-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6cd44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6cd44-107">PR_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="6cd44-107">PR_DEFAULT_STORE</span></span>  <br/> |
|<span data-ttu-id="6cd44-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6cd44-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6cd44-109">0x3400</span><span class="sxs-lookup"><span data-stu-id="6cd44-109">0x3400</span></span>  <br/> |
|<span data-ttu-id="6cd44-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6cd44-110">Data type:</span></span>  <br/> |<span data-ttu-id="6cd44-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6cd44-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6cd44-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6cd44-112">Area:</span></span>  <br/> |<span data-ttu-id="6cd44-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd44-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cd44-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6cd44-114">Remarks</span></span>

<span data-ttu-id="6cd44-115">Это свойство в виде столбцов в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cd44-115">This property appears as a column in the message store table.</span></span> <span data-ttu-id="6cd44-116">Значение основано на **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6cd44-116">The value is based on **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6cd44-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6cd44-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6cd44-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6cd44-118">Protocol specifications</span></span>

<span data-ttu-id="6cd44-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6cd44-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6cd44-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6cd44-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6cd44-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6cd44-121">Header files</span></span>

<span data-ttu-id="6cd44-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6cd44-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6cd44-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6cd44-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6cd44-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6cd44-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6cd44-125">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6cd44-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6cd44-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6cd44-126">See also</span></span>



[<span data-ttu-id="6cd44-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd44-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6cd44-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd44-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6cd44-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6cd44-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6cd44-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6cd44-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

