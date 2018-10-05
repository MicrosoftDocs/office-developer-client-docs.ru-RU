---
title: Каноническое свойство PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394330"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="3d5dd-103">Каноническое свойство PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="3d5dd-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="3d5dd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d5dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d5dd-105">Содержит битовую маску флагов для вложения.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d5dd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3d5dd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d5dd-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3d5dd-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3d5dd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3d5dd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d5dd-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="3d5dd-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="3d5dd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3d5dd-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d5dd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3d5dd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3d5dd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="3d5dd-112">Area:</span></span>  <br/> |<span data-ttu-id="3d5dd-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="3d5dd-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d5dd-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d5dd-114">Remarks</span></span>

<span data-ttu-id="3d5dd-115">Это свойство используется для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="3d5dd-116">Один или несколько из следующих флагов можно задать для битовой маски **PR_ATTACH_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="3d5dd-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="3d5dd-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="3d5dd-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="3d5dd-118">Указывает, что это вложение не доступен для приложений отображения HTML и должны учитываться в многоцелевые расширения почтового стандарта Интернета (MIME) обработки.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="3d5dd-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="3d5dd-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="3d5dd-120">Указывает, что это вложение не доступен для приложений, визуализации в форматированный текст (RTF) и должны учитываться MAPI.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="3d5dd-121">Если свойство **PR_ATTACH_FLAGS** равно нулю или отсутствует вложения — для обработки всех приложений.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3d5dd-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d5dd-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d5dd-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3d5dd-123">Protocol specifications</span></span>

<span data-ttu-id="3d5dd-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d5dd-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d5dd-125">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d5dd-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3d5dd-126">Header files</span></span>

<span data-ttu-id="3d5dd-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d5dd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d5dd-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d5dd-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d5dd-129">Mapitags.h</span></span>
  
> <span data-ttu-id="3d5dd-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="3d5dd-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d5dd-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3d5dd-131">See also</span></span>



[<span data-ttu-id="3d5dd-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d5dd-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3d5dd-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3d5dd-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3d5dd-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3d5dd-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3d5dd-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3d5dd-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

