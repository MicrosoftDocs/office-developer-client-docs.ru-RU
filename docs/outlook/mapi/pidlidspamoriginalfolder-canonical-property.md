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
# <a name="pidlidspamoriginalfolder-canonical-property"></a><span data-ttu-id="c4a0d-103">Каноническое свойство PidLidSpamOriginalFolder</span><span class="sxs-lookup"><span data-stu-id="c4a0d-103">PidLidSpamOriginalFolder Canonical Property</span></span>

  
  
<span data-ttu-id="c4a0d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4a0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4a0d-105">Указывает папку, в которую было отправлено сообщение, прежде чем оно было отфильтровано в папку нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="c4a0d-105">Indicates which folder a message was in before it was filtered into the junk email folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c4a0d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c4a0d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c4a0d-107">Диспидспаморигиналфолдер</span><span class="sxs-lookup"><span data-stu-id="c4a0d-107">dispidSpamOriginalFolder</span></span>  <br/> |
|<span data-ttu-id="c4a0d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c4a0d-108">Property set:</span></span>  <br/> |<span data-ttu-id="c4a0d-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="c4a0d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c4a0d-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="c4a0d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c4a0d-111">0x0000859C</span><span class="sxs-lookup"><span data-stu-id="c4a0d-111">0x0000859C</span></span>  <br/> |
|<span data-ttu-id="c4a0d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c4a0d-112">Data type:</span></span>  <br/> |<span data-ttu-id="c4a0d-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="c4a0d-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="c4a0d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c4a0d-114">Area:</span></span>  <br/> |<span data-ttu-id="c4a0d-115">Нежелательная почта</span><span class="sxs-lookup"><span data-stu-id="c4a0d-115">Spam</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4a0d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4a0d-116">Remarks</span></span>

<span data-ttu-id="c4a0d-117">Значением этого свойства является идентификатор **EntryID** папки, которая содержит сообщение, прежде чем оно было перемещено.</span><span class="sxs-lookup"><span data-stu-id="c4a0d-117">The value of this property is the **EntryID** of the folder that contained the message before it was moved.</span></span> <span data-ttu-id="c4a0d-118">Это свойство должно быть задано, когда сообщение помечено как нежелательная почта.</span><span class="sxs-lookup"><span data-stu-id="c4a0d-118">This property should be set when a message is marked as spam.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c4a0d-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c4a0d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c4a0d-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c4a0d-120">Protocol specifications</span></span>

<span data-ttu-id="c4a0d-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4a0d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4a0d-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c4a0d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c4a0d-123">[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c4a0d-123">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c4a0d-124">Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c4a0d-124">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c4a0d-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="c4a0d-125">Header files</span></span>

<span data-ttu-id="c4a0d-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="c4a0d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c4a0d-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c4a0d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4a0d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c4a0d-128">See also</span></span>



[<span data-ttu-id="c4a0d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c4a0d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c4a0d-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="c4a0d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c4a0d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c4a0d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c4a0d-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c4a0d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

