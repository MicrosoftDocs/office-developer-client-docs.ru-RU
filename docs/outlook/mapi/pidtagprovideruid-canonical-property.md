---
title: Каноническое свойство PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811589"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="b581c-103">Каноническое свойство PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="b581c-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="b581c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b581c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b581c-105">Содержит структуру **MAPIUID** поставщика услуг, который обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="b581c-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b581c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b581c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b581c-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="b581c-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="b581c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b581c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b581c-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="b581c-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="b581c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b581c-110">Data type:</span></span>  <br/> |<span data-ttu-id="b581c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b581c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b581c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b581c-112">Area:</span></span>  <br/> |<span data-ttu-id="b581c-113">Распространенные MAPI</span><span class="sxs-lookup"><span data-stu-id="b581c-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b581c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b581c-114">Remarks</span></span>

<span data-ttu-id="b581c-115">Это свойство вычисляется по всем поставщикам услуг.</span><span class="sxs-lookup"><span data-stu-id="b581c-115">This property is computed by all service providers.</span></span> <span data-ttu-id="b581c-116">Структура [MAPIUID](mapiuid.md) связанных с и обычно жестко поставщиком, в нем.</span><span class="sxs-lookup"><span data-stu-id="b581c-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="b581c-117">Обычно используется приложением клиента и интересует только адресной книги контейнеры конкретной службы.</span><span class="sxs-lookup"><span data-stu-id="b581c-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="b581c-118">Это свойство отображается только в качестве записи в столбце в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="b581c-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b581c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b581c-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b581c-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b581c-120">Header files</span></span>

<span data-ttu-id="b581c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b581c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b581c-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b581c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b581c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b581c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b581c-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b581c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b581c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b581c-125">See also</span></span>



[<span data-ttu-id="b581c-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b581c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b581c-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b581c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b581c-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b581c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b581c-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b581c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

