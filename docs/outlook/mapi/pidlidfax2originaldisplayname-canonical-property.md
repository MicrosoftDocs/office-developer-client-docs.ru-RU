---
title: Каноническое свойство PidLidFax2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax2OriginalDisplayName
api_type:
- COM
ms.assetid: 7f521e27-834c-4fb5-9782-2c5d1380690f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d009118b8e4c11f70e9545302e2fd7ab9b43f00e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810308"
---
# <a name="pidlidfax2originaldisplayname-canonical-property"></a><span data-ttu-id="cb915-103">Каноническое свойство PidLidFax2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="cb915-103">PidLidFax2OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="cb915-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb915-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb915-105">Задает исходное отображаемое имя адрес домашнего факса контакта.</span><span class="sxs-lookup"><span data-stu-id="cb915-105">Specifies the original display name of the contact's home fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb915-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cb915-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb915-107">dispidFax2OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="cb915-107">dispidFax2OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="cb915-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="cb915-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb915-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cb915-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cb915-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="cb915-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb915-111">0x000080C4</span><span class="sxs-lookup"><span data-stu-id="cb915-111">0x000080C4</span></span>  <br/> |
|<span data-ttu-id="cb915-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cb915-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb915-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cb915-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cb915-114">Область:</span><span class="sxs-lookup"><span data-stu-id="cb915-114">Area:</span></span>  <br/> |<span data-ttu-id="cb915-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="cb915-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb915-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb915-116">Remarks</span></span>

<span data-ttu-id="cb915-117">Это свойство, если этот параметр указан, должен иметь значение совпадает со значением свойства **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cb915-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cb915-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cb915-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb915-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cb915-119">Protocol specifications</span></span>

<span data-ttu-id="cb915-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb915-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb915-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cb915-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb915-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb915-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb915-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="cb915-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb915-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cb915-124">Header files</span></span>

<span data-ttu-id="cb915-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb915-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb915-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cb915-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb915-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cb915-127">See also</span></span>



[<span data-ttu-id="cb915-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cb915-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb915-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cb915-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb915-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cb915-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb915-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cb915-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

