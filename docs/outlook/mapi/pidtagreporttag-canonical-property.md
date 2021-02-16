---
title: Каноническое свойство PidTagReportTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 870fbf2228206253261124907d6bd420f95fb7c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331432"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="f6b7a-103">Каноническое свойство PidTagReportTag</span><span class="sxs-lookup"><span data-stu-id="f6b7a-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="f6b7a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6b7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6b7a-105">Содержит двоичное значение тега, которое система обмена сообщениями должна скопировать в любой отчет, созданный для сообщения.</span><span class="sxs-lookup"><span data-stu-id="f6b7a-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6b7a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f6b7a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6b7a-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="f6b7a-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="f6b7a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f6b7a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6b7a-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="f6b7a-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="f6b7a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f6b7a-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6b7a-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f6b7a-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f6b7a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f6b7a-112">Area:</span></span>  <br/> |<span data-ttu-id="f6b7a-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b7a-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6b7a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6b7a-114">Remarks</span></span>

<span data-ttu-id="f6b7a-115">Это свойство, как **и свойство PR_SUBJECT_IPM** ([PidTagSubjectMessageId),](pidtagsubjectmessageid-canonical-property.md)используется для сопоставления отчета с исходным сообщением.</span><span class="sxs-lookup"><span data-stu-id="f6b7a-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f6b7a-116">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f6b7a-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6b7a-117">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f6b7a-117">Protocol specifications</span></span>

<span data-ttu-id="f6b7a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6b7a-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6b7a-119">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f6b7a-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f6b7a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6b7a-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6b7a-121">Указывает свойства и операции, которые разрешены для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f6b7a-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6b7a-122">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="f6b7a-122">Header files</span></span>

<span data-ttu-id="f6b7a-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6b7a-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6b7a-124">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f6b7a-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6b7a-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6b7a-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f6b7a-126">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f6b7a-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6b7a-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f6b7a-127">See also</span></span>



[<span data-ttu-id="f6b7a-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b7a-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6b7a-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b7a-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6b7a-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b7a-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6b7a-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f6b7a-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

