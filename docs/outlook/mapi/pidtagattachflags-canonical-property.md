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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339335"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="84aee-103">Каноническое свойство PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="84aee-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="84aee-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84aee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84aee-105">Содержит битовуюmass флагов для вложения.</span><span class="sxs-lookup"><span data-stu-id="84aee-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84aee-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="84aee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84aee-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="84aee-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="84aee-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="84aee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84aee-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="84aee-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="84aee-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="84aee-110">Data type:</span></span>  <br/> |<span data-ttu-id="84aee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="84aee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="84aee-112">Область:</span><span class="sxs-lookup"><span data-stu-id="84aee-112">Area:</span></span>  <br/> |<span data-ttu-id="84aee-113">Вложение в сообщение</span><span class="sxs-lookup"><span data-stu-id="84aee-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84aee-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="84aee-114">Remarks</span></span>

<span data-ttu-id="84aee-115">Это свойство используется для поддержки MHTML.</span><span class="sxs-lookup"><span data-stu-id="84aee-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="84aee-116">Для битовой PR_ATTACH_FLAGS можно установить **один или несколько из следующих флагов:**</span><span class="sxs-lookup"><span data-stu-id="84aee-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="84aee-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="84aee-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="84aee-118">Указывает, что это вложение не доступно приложениям отображения HTML и должно игнорироваться при обработке MIME.</span><span class="sxs-lookup"><span data-stu-id="84aee-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="84aee-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="84aee-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="84aee-120">Указывает, что это вложение не доступно приложениям в формате RTF и должно игнорироваться MAPI.</span><span class="sxs-lookup"><span data-stu-id="84aee-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="84aee-121">Если свойство **PR_ATTACH_FLAGS** ноль или отсутствует, вложение обрабатывается всеми приложениями.</span><span class="sxs-lookup"><span data-stu-id="84aee-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="84aee-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="84aee-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84aee-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="84aee-123">Protocol specifications</span></span>

<span data-ttu-id="84aee-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84aee-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84aee-125">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="84aee-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84aee-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="84aee-126">Header files</span></span>

<span data-ttu-id="84aee-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84aee-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="84aee-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="84aee-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="84aee-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84aee-129">Mapitags.h</span></span>
  
> <span data-ttu-id="84aee-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="84aee-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84aee-131">См. также</span><span class="sxs-lookup"><span data-stu-id="84aee-131">See also</span></span>



[<span data-ttu-id="84aee-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84aee-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84aee-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="84aee-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84aee-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="84aee-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84aee-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="84aee-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

