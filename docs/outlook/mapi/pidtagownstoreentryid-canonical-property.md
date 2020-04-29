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
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427376"
---
# <a name="pidtagownstoreentryid-canonical-property"></a><span data-ttu-id="7ed60-103">Каноническое свойство PidTagOwnStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="7ed60-103">PidTagOwnStoreEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7ed60-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ed60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ed60-105">Содержит идентификатор строго связанного хранилища сообщений транспорта.</span><span class="sxs-lookup"><span data-stu-id="7ed60-105">Contains the entry identifier of a transport's tightly coupled message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ed60-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="7ed60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ed60-107">PR_OWN_STORE_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7ed60-107">PR_OWN_STORE_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7ed60-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="7ed60-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ed60-109">0x3E06</span><span class="sxs-lookup"><span data-stu-id="7ed60-109">0x3E06</span></span>  <br/> |
|<span data-ttu-id="7ed60-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="7ed60-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ed60-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7ed60-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7ed60-112">Область:</span><span class="sxs-lookup"><span data-stu-id="7ed60-112">Area:</span></span>  <br/> |<span data-ttu-id="7ed60-113">Свойства хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="7ed60-113">Message Store Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ed60-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ed60-114">Remarks</span></span>

<span data-ttu-id="7ed60-115">Это свойство указывает идентификатор для тесно связанного хранилища, если он существует.</span><span class="sxs-lookup"><span data-stu-id="7ed60-115">This property specifies the entry identifier for the tightly coupled store, if one exists.</span></span> <span data-ttu-id="7ed60-116">Например, поставщик транспорта может указать идентификатор записи хранилища личных папок, чтобы диспетчер очереди MAPI мог подключить поставщик транспорта к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="7ed60-116">For example, a transport provider can specify the private folder store entry identifier so that the MAPI spooler can connect the transport provider to the store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7ed60-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7ed60-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7ed60-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="7ed60-118">Header files</span></span>

<span data-ttu-id="7ed60-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="7ed60-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ed60-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="7ed60-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ed60-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="7ed60-121">Mapitags.h</span></span>
  
> <span data-ttu-id="7ed60-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="7ed60-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ed60-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7ed60-123">See also</span></span>



[<span data-ttu-id="7ed60-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed60-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ed60-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed60-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ed60-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="7ed60-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ed60-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="7ed60-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

