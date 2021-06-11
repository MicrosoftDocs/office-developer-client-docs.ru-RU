---
title: Каноническое свойство PidLidVerbResponse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidVerbResponse
api_type:
- COM
ms.assetid: 6f3db5ac-f1cb-4c55-ab88-c126dd5f48ee
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 474df017954618e6411494454c1405445563b862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360559"
---
# <a name="pidlidverbresponse-canonical-property"></a><span data-ttu-id="1b5eb-103">Каноническое свойство PidLidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="1b5eb-103">PidLidVerbResponse Canonical Property</span></span>

  
  
<span data-ttu-id="1b5eb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b5eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b5eb-105">Указывает параметр голосования, выбранный респондентом.</span><span class="sxs-lookup"><span data-stu-id="1b5eb-105">Specifies the voting option that a respondent selected.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b5eb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1b5eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b5eb-107">dispidVerbResponse</span><span class="sxs-lookup"><span data-stu-id="1b5eb-107">dispidVerbResponse</span></span>  <br/> |
|<span data-ttu-id="1b5eb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="1b5eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="1b5eb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="1b5eb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="1b5eb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1b5eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1b5eb-111">0x00008524</span><span class="sxs-lookup"><span data-stu-id="1b5eb-111">0x00008524</span></span>  <br/> |
|<span data-ttu-id="1b5eb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1b5eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="1b5eb-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1b5eb-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1b5eb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="1b5eb-114">Area:</span></span>  <br/> |<span data-ttu-id="1b5eb-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="1b5eb-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b5eb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b5eb-116">Remarks</span></span>

<span data-ttu-id="1b5eb-117">Это свойство обычно задалось одному из делимитативных значений, содержащихся в свойстве **dispidVerbStream** [(PidLidVerbStream),](pidlidverbstream-canonical-property.md)на котором голосует респондент.</span><span class="sxs-lookup"><span data-stu-id="1b5eb-117">This property is usually set to one of the delimited values that are contained in the **dispidVerbStream** ([PidLidVerbStream](pidlidverbstream-canonical-property.md)) property on which the respondent votes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1b5eb-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1b5eb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b5eb-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1b5eb-119">Protocol specifications</span></span>

<span data-ttu-id="1b5eb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b5eb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b5eb-121">Предоставляет определение набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="1b5eb-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b5eb-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b5eb-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b5eb-123">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1b5eb-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b5eb-124">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="1b5eb-124">Header files</span></span>

<span data-ttu-id="1b5eb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b5eb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b5eb-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1b5eb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b5eb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="1b5eb-127">See also</span></span>



[<span data-ttu-id="1b5eb-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b5eb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b5eb-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1b5eb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b5eb-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1b5eb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b5eb-131">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="1b5eb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

