---
title: Каноническое свойство PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425675"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="21e3b-103">Каноническое свойство PidTagMessageSecurityLabel</span><span class="sxs-lookup"><span data-stu-id="21e3b-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="21e3b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21e3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21e3b-105">Содержит метку безопасности для сообщения.</span><span class="sxs-lookup"><span data-stu-id="21e3b-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21e3b-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="21e3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21e3b-107">ПР_МЕССАЖЕ_СЕКУРИТИ_ЛАБЕЛ</span><span class="sxs-lookup"><span data-stu-id="21e3b-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="21e3b-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="21e3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21e3b-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="21e3b-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="21e3b-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="21e3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="21e3b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="21e3b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="21e3b-112">Область:</span><span class="sxs-lookup"><span data-stu-id="21e3b-112">Area:</span></span>  <br/> |<span data-ttu-id="21e3b-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="21e3b-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21e3b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="21e3b-114">Remarks</span></span>

<span data-ttu-id="21e3b-115">Это свойство предоставляет основу для защиты сообщения с помощью свойства **пр_мессаже_токен** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="21e3b-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="21e3b-116">Связь с содержимым сообщения гарантируется маркером.</span><span class="sxs-lookup"><span data-stu-id="21e3b-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="21e3b-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="21e3b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="21e3b-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="21e3b-118">Header files</span></span>

<span data-ttu-id="21e3b-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="21e3b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="21e3b-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="21e3b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="21e3b-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="21e3b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="21e3b-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="21e3b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21e3b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="21e3b-123">See also</span></span>



[<span data-ttu-id="21e3b-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="21e3b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21e3b-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="21e3b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21e3b-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="21e3b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21e3b-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="21e3b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

