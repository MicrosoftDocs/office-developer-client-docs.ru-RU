---
title: Каноническое свойство PidTagViewDescriptorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394771"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a><span data-ttu-id="0e66c-103">Каноническое свойство PidTagViewDescriptorName</span><span class="sxs-lookup"><span data-stu-id="0e66c-103">PidTagViewDescriptorName Canonical Property</span></span>

  
  
<span data-ttu-id="0e66c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e66c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e66c-105">Содержит имя дескриптора представления.</span><span class="sxs-lookup"><span data-stu-id="0e66c-105">Contains the name of a view descriptor.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e66c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0e66c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0e66c-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span><span class="sxs-lookup"><span data-stu-id="0e66c-107">PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W</span></span>  <br/> |
|<span data-ttu-id="0e66c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0e66c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0e66c-109">0x7006</span><span class="sxs-lookup"><span data-stu-id="0e66c-109">0x7006</span></span>  <br/> |
|<span data-ttu-id="0e66c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0e66c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0e66c-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0e66c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0e66c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0e66c-112">Area:</span></span>  <br/> |<span data-ttu-id="0e66c-113">Сообщение, определенное класс передаваемого</span><span class="sxs-lookup"><span data-stu-id="0e66c-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e66c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e66c-114">Remarks</span></span>

<span data-ttu-id="0e66c-115">Эти свойства должен иметь значение пустой строке сообщения связать сведения о папке (FAI), который содержит определения представлений.</span><span class="sxs-lookup"><span data-stu-id="0e66c-115">These properties must be set to a non-empty string for a Folder Associate Information (FAI) message that contains view definitions.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0e66c-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0e66c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0e66c-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0e66c-117">Protocol specifications</span></span>

<span data-ttu-id="0e66c-118">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0e66c-118">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0e66c-119">Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.</span><span class="sxs-lookup"><span data-stu-id="0e66c-119">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0e66c-120">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0e66c-120">Header files</span></span>

<span data-ttu-id="0e66c-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0e66c-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="0e66c-122">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0e66c-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="0e66c-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0e66c-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0e66c-124">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0e66c-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0e66c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0e66c-125">See also</span></span>



[<span data-ttu-id="0e66c-126">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e66c-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0e66c-127">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0e66c-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0e66c-128">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0e66c-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0e66c-129">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0e66c-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

