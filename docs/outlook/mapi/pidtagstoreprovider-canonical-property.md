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
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="8ad62-103">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="8ad62-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="8ad62-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ad62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ad62-105">Содержит определенную поставщиком структуру [мапиуид](mapiuid.md) , которая указывает тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ad62-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ad62-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8ad62-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ad62-107">ПР_МДБ_ПРОВИДЕР</span><span class="sxs-lookup"><span data-stu-id="8ad62-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="8ad62-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8ad62-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ad62-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="8ad62-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="8ad62-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8ad62-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ad62-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8ad62-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8ad62-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8ad62-112">Area:</span></span>  <br/> |<span data-ttu-id="8ad62-113">Свойства идентификатора</span><span class="sxs-lookup"><span data-stu-id="8ad62-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ad62-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ad62-114">Remarks</span></span>

<span data-ttu-id="8ad62-115">Структура [мапиуид](mapiuid.md) определяет тип хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ad62-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="8ad62-116">Значение вычисляется поставщиками хранилища сообщений в объектах хранилища сообщений и является уникальным для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="8ad62-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="8ad62-117">Обычно он используется для просмотра таблицы хранилища сообщений, чтобы найти магазин требуемого типа, например общедоступные папки.</span><span class="sxs-lookup"><span data-stu-id="8ad62-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="8ad62-118">Это свойство является аналогом свойства **пр_аб_провидер_ид** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) для адресных книг.</span><span class="sxs-lookup"><span data-stu-id="8ad62-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ad62-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ad62-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8ad62-120">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8ad62-120">Header files</span></span>

<span data-ttu-id="8ad62-121">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8ad62-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ad62-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8ad62-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ad62-123">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="8ad62-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8ad62-124">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="8ad62-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ad62-125">См. также</span><span class="sxs-lookup"><span data-stu-id="8ad62-125">See also</span></span>



[<span data-ttu-id="8ad62-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad62-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ad62-127">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad62-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ad62-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8ad62-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ad62-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8ad62-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

