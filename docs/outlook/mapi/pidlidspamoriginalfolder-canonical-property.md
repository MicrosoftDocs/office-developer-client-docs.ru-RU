---
title: Каноническое свойство PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331558"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="17da4-103">Каноническое свойство PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="17da4-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="17da4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17da4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17da4-105">Указывает, в какой папке было сообщение до фильтрации в нежелательной папке электронной почты.</span><span class="sxs-lookup"><span data-stu-id="17da4-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="17da4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="17da4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="17da4-107">dispidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="17da4-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="17da4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="17da4-108">Property set:</span></span>  <br/> |<span data-ttu-id="17da4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="17da4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="17da4-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="17da4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="17da4-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="17da4-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="17da4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="17da4-112">Data type:</span></span>  <br/> |<span data-ttu-id="17da4-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="17da4-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="17da4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="17da4-114">Area:</span></span>  <br/> |<span data-ttu-id="17da4-115">Спам</span><span class="sxs-lookup"><span data-stu-id="17da4-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17da4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="17da4-116">Remarks</span></span>

<span data-ttu-id="17da4-117">Значением этого свойства является **EntryID** папки, которая содержала сообщение перед его перемещением.</span><span class="sxs-lookup"><span data-stu-id="17da4-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="17da4-118">Это свойство должно быть установлено, когда сообщение помечено как спам.</span><span class="sxs-lookup"><span data-stu-id="17da4-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="17da4-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="17da4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="17da4-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="17da4-120">Protocol specifications</span></span>

<span data-ttu-id="17da4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17da4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17da4-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="17da4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="17da4-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="17da4-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="17da4-124">Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="17da4-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="17da4-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="17da4-125">Header files</span></span>

<span data-ttu-id="17da4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="17da4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="17da4-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="17da4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17da4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="17da4-128">See also</span></span>



[<span data-ttu-id="17da4-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="17da4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="17da4-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="17da4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="17da4-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="17da4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="17da4-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="17da4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

