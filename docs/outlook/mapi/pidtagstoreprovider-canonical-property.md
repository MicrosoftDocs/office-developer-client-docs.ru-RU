---
title: Каноническое свойство PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412053"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="1fbf9-103">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="1fbf9-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="1fbf9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fbf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fbf9-105">Содержит структуру [MAPIUID,](mapiuid.md) определяемую поставщиком, которая указывает тип магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fbf9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1fbf9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1fbf9-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="1fbf9-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="1fbf9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1fbf9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1fbf9-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="1fbf9-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="1fbf9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1fbf9-110">Data type:</span></span>  <br/> |<span data-ttu-id="1fbf9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fbf9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1fbf9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1fbf9-112">Area:</span></span>  <br/> |<span data-ttu-id="1fbf9-113">Свойства ID</span><span class="sxs-lookup"><span data-stu-id="1fbf9-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fbf9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1fbf9-114">Remarks</span></span>

<span data-ttu-id="1fbf9-115">Структура [MAPIUID](mapiuid.md) определяет тип магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="1fbf9-116">Значение вычисляется поставщиками магазина сообщений на объектах магазина сообщений и является уникальным для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="1fbf9-117">Обычно он используется для просмотра в таблице хранения сообщений для поиска магазина нужного типа, например общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="1fbf9-118">Это свойство аналогично свойству **PR_AB_PROVIDER_ID** [(PidTagAbProviderId)](pidtagabproviderid-canonical-property.md)для адресных книг.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1fbf9-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1fbf9-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1fbf9-120">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="1fbf9-120">Header files</span></span>

<span data-ttu-id="1fbf9-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1fbf9-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1fbf9-122">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1fbf9-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1fbf9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1fbf9-124">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1fbf9-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1fbf9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="1fbf9-125">See also</span></span>



[<span data-ttu-id="1fbf9-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1fbf9-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1fbf9-127">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1fbf9-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1fbf9-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1fbf9-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1fbf9-129">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="1fbf9-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

