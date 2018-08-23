---
title: Каноническое свойство PidLidFax2OriginalEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax2OriginalEntryId
api_type:
- COM
ms.assetid: da80d72f-9389-463f-8665-f26bb30c0ed2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f6b8a00070cba755eb043e90586528674e461514
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592614"
---
# <a name="pidlidfax2originalentryid-canonical-property"></a><span data-ttu-id="08075-103">Каноническое свойство PidLidFax2OriginalEntryId</span><span class="sxs-lookup"><span data-stu-id="08075-103">PidLidFax2OriginalEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="08075-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08075-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08075-105">Указывает исходный код записи адрес домашнего факса контакта.</span><span class="sxs-lookup"><span data-stu-id="08075-105">Specifies the original EntryID of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08075-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="08075-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08075-107">dispidFax2OriginalEntryID</span><span class="sxs-lookup"><span data-stu-id="08075-107">dispidFax2OriginalEntryID</span></span>  <br/> |
|<span data-ttu-id="08075-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="08075-108">Property set:</span></span>  <br/> |<span data-ttu-id="08075-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="08075-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="08075-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="08075-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="08075-111">0x000080C5</span><span class="sxs-lookup"><span data-stu-id="08075-111">0x000080C5</span></span>  <br/> |
|<span data-ttu-id="08075-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="08075-112">Data type:</span></span>  <br/> |<span data-ttu-id="08075-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08075-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08075-114">Область:</span><span class="sxs-lookup"><span data-stu-id="08075-114">Area:</span></span>  <br/> |<span data-ttu-id="08075-115">Contact</span><span class="sxs-lookup"><span data-stu-id="08075-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08075-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="08075-116">Remarks</span></span>

<span data-ttu-id="08075-117">Это свойство, если этот параметр указан, необходимо указать одноразовых EntryId, соответствующий этот адрес факса.</span><span class="sxs-lookup"><span data-stu-id="08075-117">This property, if present, must specify the one-off EntryId that corresponds to this fax address.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08075-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="08075-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08075-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="08075-119">Protocol specifications</span></span>

<span data-ttu-id="08075-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08075-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08075-121">Содержит определение набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="08075-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08075-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08075-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08075-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="08075-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08075-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="08075-124">Header files</span></span>

<span data-ttu-id="08075-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08075-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="08075-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="08075-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08075-127">См. также</span><span class="sxs-lookup"><span data-stu-id="08075-127">See also</span></span>



[<span data-ttu-id="08075-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08075-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08075-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08075-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08075-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="08075-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08075-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="08075-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

