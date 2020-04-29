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
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422777"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="c4d5d-103">Каноническое свойство PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="c4d5d-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="c4d5d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4d5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4d5d-105">Содержит структуру **мапиуид** поставщика услуг, который обрабатывает сообщение.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4d5d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4d5d-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="c4d5d-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="c4d5d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c4d5d-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="c4d5d-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="c4d5d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c4d5d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c4d5d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c4d5d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c4d5d-112">Area:</span></span>  <br/> |<span data-ttu-id="c4d5d-113">Общие протоколы MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d5d-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4d5d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4d5d-114">Remarks</span></span>

<span data-ttu-id="c4d5d-115">Это свойство вычисляется всеми поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-115">This property is computed by all service providers.</span></span> <span data-ttu-id="c4d5d-116">Он содержит структуру [мапиуид](mapiuid.md) , связанную с, и обычно жестко запрограммированную поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="c4d5d-117">Он обычно используется клиентским приложением, которое заинтересовано только в контейнерах адресной книги, предоставленных определенным поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="c4d5d-118">Это свойство отображается только в качестве записи столбца в таблице поставщика.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c4d5d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c4d5d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c4d5d-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c4d5d-120">Header files</span></span>

<span data-ttu-id="c4d5d-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c4d5d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4d5d-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="c4d5d-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="c4d5d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c4d5d-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="c4d5d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4d5d-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c4d5d-125">See also</span></span>



[<span data-ttu-id="c4d5d-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d5d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4d5d-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d5d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4d5d-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c4d5d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4d5d-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c4d5d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

