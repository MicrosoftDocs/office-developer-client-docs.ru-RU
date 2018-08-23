---
title: Каноническое свойство PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55da942e59c619dd384bef58349aa3a00d4a6d8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571474"
---
# <a name="pidtagbodycrc-canonical-property"></a><span data-ttu-id="4e257-103">Каноническое свойство PidTagBodyCrc</span><span class="sxs-lookup"><span data-stu-id="4e257-103">PidTagBodyCrc Canonical Property</span></span>

  
  
<span data-ttu-id="4e257-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e257-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e257-105">Содержит значение суммы циклической на текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e257-105">Contains a cyclic redundancy check (CRC) value on the message text.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e257-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4e257-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e257-107">PR_BODY_CRC</span><span class="sxs-lookup"><span data-stu-id="4e257-107">PR_BODY_CRC</span></span>  <br/> |
|<span data-ttu-id="4e257-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="4e257-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e257-109">0x0E1C</span><span class="sxs-lookup"><span data-stu-id="4e257-109">0x0E1C</span></span>  <br/> |
|<span data-ttu-id="4e257-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4e257-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e257-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4e257-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4e257-112">Область:</span><span class="sxs-lookup"><span data-stu-id="4e257-112">Area:</span></span>  <br/> |<span data-ttu-id="4e257-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="4e257-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e257-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e257-114">Remarks</span></span>

<span data-ttu-id="4e257-115">Хранилище сообщений можно использовать любой контрольной СУММЫ алгоритм, который создает значение PT_LONG.</span><span class="sxs-lookup"><span data-stu-id="4e257-115">The message store can use any CRC algorithm that generates a PT_LONG value.</span></span> <span data-ttu-id="4e257-116">Его следует вычислять это свойство как часть метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) при **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) свойство имеет значение в первый раз, а также при последующем был изменен.</span><span class="sxs-lookup"><span data-stu-id="4e257-116">It must compute this property as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method when the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property has been set for the first time and whenever it has been subsequently modified.</span></span>
  
<span data-ttu-id="4e257-117">Клиентское приложение использует **PR_BODY_CRC** для облегчения сравнения строк текста сообщения, содержащихся в **PR_BODY** свойств или их варианты.</span><span class="sxs-lookup"><span data-stu-id="4e257-117">A client application uses **PR_BODY_CRC** to aid in comparing message text strings contained in **PR_BODY** properties or their variants.</span></span> <span data-ttu-id="4e257-118">При использовании этого свойства клиента можно быстро и легко обнаруживать при изменении текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="4e257-118">Using this property, the client can quickly and easily detect when the message text has changed.</span></span> <span data-ttu-id="4e257-119">Его можно реализовать высокую производительность с помощью **PR_BODY_CRC** вместо получения **PR_BODY** хранилища сообщений и сравнение с локальной версией.</span><span class="sxs-lookup"><span data-stu-id="4e257-119">It can realize significant performance gains by using **PR_BODY_CRC** instead of obtaining **PR_BODY** from the message store and comparing it with a local version.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e257-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e257-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e257-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4e257-121">Header files</span></span>

<span data-ttu-id="4e257-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e257-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e257-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4e257-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e257-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4e257-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4e257-125">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="4e257-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e257-126">См. также</span><span class="sxs-lookup"><span data-stu-id="4e257-126">See also</span></span>



[<span data-ttu-id="4e257-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4e257-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e257-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4e257-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e257-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4e257-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e257-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4e257-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

