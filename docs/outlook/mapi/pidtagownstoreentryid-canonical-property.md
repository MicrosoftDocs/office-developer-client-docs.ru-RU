---
title: Каноническое свойство PidTagOwnStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 54014ab25d268c161465349b4e33c6a1df19f140
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591701"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="493f5-103">Каноническое свойство PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="493f5-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="493f5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="493f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="493f5-105">Содержит идентификатор записи хранилища тесно связанных сообщения транспорта.</span><span class="sxs-lookup"><span data-stu-id="493f5-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="493f5-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="493f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="493f5-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="493f5-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="493f5-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="493f5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="493f5-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="493f5-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="493f5-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="493f5-110">Data type:</span></span>  <br/> |<span data-ttu-id="493f5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="493f5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="493f5-112">Область:</span><span class="sxs-lookup"><span data-stu-id="493f5-112">Area:</span></span>  <br/> |<span data-ttu-id="493f5-113">Свойства хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="493f5-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="493f5-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="493f5-114">Remarks</span></span>

<span data-ttu-id="493f5-115">Это свойство определяет идентификатор записи для тесно связанных хранилища, если он существует.</span><span class="sxs-lookup"><span data-stu-id="493f5-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="493f5-116">Например поставщика транспорта можно указать личной папки хранения идентификатор записи диспетчер очереди MAPI для подключения к хранилищу поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="493f5-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="493f5-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="493f5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="493f5-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="493f5-118">Header files</span></span>

<span data-ttu-id="493f5-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="493f5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="493f5-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="493f5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="493f5-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="493f5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="493f5-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="493f5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="493f5-123">См. также</span><span class="sxs-lookup"><span data-stu-id="493f5-123">See also</span></span>



[<span data-ttu-id="493f5-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="493f5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="493f5-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="493f5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="493f5-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="493f5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="493f5-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="493f5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

