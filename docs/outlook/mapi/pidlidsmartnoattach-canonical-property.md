---
title: Каноническое свойство PidLidSmartNoAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSmartNoAttach
api_type:
- COM
ms.assetid: 60299c1b-1b46-4c3a-8fb9-a2b4d3383aac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7dddca6a17b07047d1447a57347fbe47a04471e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331320"
---
# <a name="pidlidsmartnoattach-canonical-property"></a><span data-ttu-id="4b843-103">Каноническое свойство PidLidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="4b843-103">PidLidSmartNoAttach Canonical Property</span></span>

  
  
<span data-ttu-id="4b843-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b843-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b843-105">Представляет, считаются ли вложения в сообщении скрытыми.</span><span class="sxs-lookup"><span data-stu-id="4b843-105">Represents whether the attachments on a message are considered as hidden.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b843-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4b843-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b843-107">dispidSmartNoAttach</span><span class="sxs-lookup"><span data-stu-id="4b843-107">dispidSmartNoAttach</span></span>  <br/> |
|<span data-ttu-id="4b843-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4b843-108">Property set:</span></span>  <br/> |<span data-ttu-id="4b843-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4b843-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4b843-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4b843-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4b843-111">0x00008514</span><span class="sxs-lookup"><span data-stu-id="4b843-111">0x00008514</span></span>  <br/> |
|<span data-ttu-id="4b843-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4b843-112">Data type:</span></span>  <br/> |<span data-ttu-id="4b843-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="4b843-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="4b843-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4b843-114">Area:</span></span>  <br/> |<span data-ttu-id="4b843-115">Конфигурация времени запуска</span><span class="sxs-lookup"><span data-stu-id="4b843-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b843-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4b843-116">Remarks</span></span>

<span data-ttu-id="4b843-117">Это свойство TRUE, если вложения сообщения считаются скрытыми.</span><span class="sxs-lookup"><span data-stu-id="4b843-117">This property is TRUE if the attachments of the message are considered as hidden.</span></span>
  
<span data-ttu-id="4b843-118">Он указывает, не имеет ли объект сообщения видимых вложений для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="4b843-118">It indicates whether the message object has no end-user visible attachments.</span></span> <span data-ttu-id="4b843-119">Это свойство может быть неустановленным; если это так, предполагается значение FALSE по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b843-119">This property may be unset; if so, a default value of FALSE is assumed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b843-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4b843-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b843-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4b843-121">Protocol specifications</span></span>

<span data-ttu-id="4b843-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b843-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b843-123">Предоставляет определение набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="4b843-123">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4b843-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b843-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b843-125">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="4b843-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b843-126">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="4b843-126">Header files</span></span>

<span data-ttu-id="4b843-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b843-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b843-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4b843-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b843-129">См. также</span><span class="sxs-lookup"><span data-stu-id="4b843-129">See also</span></span>



[<span data-ttu-id="4b843-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4b843-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b843-131">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4b843-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b843-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4b843-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b843-133">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="4b843-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

