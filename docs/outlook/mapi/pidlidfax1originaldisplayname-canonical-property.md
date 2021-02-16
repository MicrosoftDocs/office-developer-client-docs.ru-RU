---
title: Каноническое свойство PidLidFax1OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFax1OriginalDisplayName
api_type:
- COM
ms.assetid: 1520e27f-e261-4a94-be06-31cd47bea4a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e24637ed9e29ab887833b6ed5ff7453353684a47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332132"
---
# <a name="pidlidfax1originaldisplayname-canonical-property"></a><span data-ttu-id="51108-103">Каноническое свойство PidLidFax1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="51108-103">PidLidFax1OriginalDisplayName Canonical Property</span></span>

  
  
<span data-ttu-id="51108-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51108-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51108-105">Указывает исходное отображаемого имени бизнес-адреса факса контакта.</span><span class="sxs-lookup"><span data-stu-id="51108-105">Specifies the original display name of the contact's business fax address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51108-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="51108-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51108-107">dispidFax1OriginalDisplayName</span><span class="sxs-lookup"><span data-stu-id="51108-107">dispidFax1OriginalDisplayName</span></span>  <br/> |
|<span data-ttu-id="51108-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="51108-108">Property set:</span></span>  <br/> |<span data-ttu-id="51108-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="51108-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="51108-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="51108-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51108-111">0x000080B4</span><span class="sxs-lookup"><span data-stu-id="51108-111">0x000080B4</span></span>  <br/> |
|<span data-ttu-id="51108-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="51108-112">Data type:</span></span>  <br/> |<span data-ttu-id="51108-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="51108-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="51108-114">Область:</span><span class="sxs-lookup"><span data-stu-id="51108-114">Area:</span></span>  <br/> |<span data-ttu-id="51108-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="51108-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51108-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="51108-116">Remarks</span></span>

<span data-ttu-id="51108-117">При его значении этому свойству необходимо установить то же **значение, что** и для свойства PR_NORMALIZED_SUBJECT ([PidTagNormalizedSubject).](pidtagnormalizedsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="51108-117">This property, if present, must be set to the same value as the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="51108-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="51108-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51108-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="51108-119">Protocol specifications</span></span>

<span data-ttu-id="51108-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51108-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51108-121">Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="51108-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51108-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51108-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51108-123">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="51108-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="51108-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="51108-124">Header files</span></span>

<span data-ttu-id="51108-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51108-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="51108-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="51108-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51108-127">См. также</span><span class="sxs-lookup"><span data-stu-id="51108-127">See also</span></span>



[<span data-ttu-id="51108-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="51108-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51108-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="51108-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51108-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="51108-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51108-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="51108-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

