---
title: Каноническое свойство PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810778"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="c36ac-103">Каноническое свойство PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="c36ac-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="c36ac-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c36ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c36ac-105">Содержит структуру [MAPIUID](mapiuid.md) поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="c36ac-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c36ac-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c36ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c36ac-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="c36ac-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="c36ac-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c36ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c36ac-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="c36ac-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="c36ac-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c36ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="c36ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c36ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c36ac-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c36ac-112">Area:</span></span>  <br/> |<span data-ttu-id="c36ac-113">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="c36ac-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c36ac-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c36ac-114">Remarks</span></span>

<span data-ttu-id="c36ac-115">Структура **MAPIUID** определяет, какой поставщик адресной книги предоставляет этот контейнер определенный в иерархии контейнеров.</span><span class="sxs-lookup"><span data-stu-id="c36ac-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="c36ac-116">Значение является уникальным для каждого поставщика.</span><span class="sxs-lookup"><span data-stu-id="c36ac-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="c36ac-117">Поставщика адресных книг можно обеспечить более одного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="c36ac-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="c36ac-118">Например поставщика, который предоставляет два разных контейнеров можно опубликовать **PR_AB_PROVIDER_ID** уникальных идентификаторов для каждого контейнера.</span><span class="sxs-lookup"><span data-stu-id="c36ac-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="c36ac-119">**PR_AB_PROVIDER_ID** является аналогом свойства **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) для хранилищ сообщений.</span><span class="sxs-lookup"><span data-stu-id="c36ac-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="c36ac-120">Клиентские приложения могут использовать **PR_AB_PROVIDER_ID** для поиска строк, связанных с ними в иерархии таблицы адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c36ac-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c36ac-121">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c36ac-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c36ac-122">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c36ac-122">Header files</span></span>

<span data-ttu-id="c36ac-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c36ac-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c36ac-124">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="c36ac-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="c36ac-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c36ac-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c36ac-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c36ac-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c36ac-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c36ac-127">See also</span></span>



[<span data-ttu-id="c36ac-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c36ac-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c36ac-129">Каноническое свойство PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="c36ac-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="c36ac-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c36ac-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c36ac-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c36ac-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c36ac-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c36ac-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

