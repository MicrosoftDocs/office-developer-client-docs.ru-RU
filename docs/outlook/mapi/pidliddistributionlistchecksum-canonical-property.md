---
title: Каноническое свойство PidLidDistributionListChecksum
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidDistributionListChecksum
api_type:
- COM
ms.assetid: bd50ab34-caae-4258-8afc-769e3cbc5220
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ac1f0d839b1ea059ec2b8d94556808bea3850862
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357612"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="cb261-103">Каноническое свойство PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="cb261-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="cb261-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb261-105">Указывает 32-битовую проверку циклической избыточности (CRC-32) для личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="cb261-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb261-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cb261-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cb261-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="cb261-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="cb261-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="cb261-108">Property set:</span></span>  <br/> |<span data-ttu-id="cb261-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="cb261-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="cb261-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="cb261-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="cb261-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="cb261-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="cb261-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cb261-112">Data type:</span></span>  <br/> |<span data-ttu-id="cb261-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cb261-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cb261-114">Область:</span><span class="sxs-lookup"><span data-stu-id="cb261-114">Area:</span></span>  <br/> |<span data-ttu-id="cb261-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="cb261-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb261-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb261-116">Remarks</span></span>

<span data-ttu-id="cb261-117">Значение этого свойства можно использовать для определения того, когда свойство **dispidDLMembers** ([PidLidDistributionListMembers)](pidliddistributionlistmembers-canonical-property.md)было обновлено без обновления других свойств участника списка рассылки путем вычисления CRC-32 на существующем значении **dispidDLMembers** и сравнения его со значением свойства **dispidDLChecksum.**</span><span class="sxs-lookup"><span data-stu-id="cb261-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cb261-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cb261-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cb261-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="cb261-119">Protocol specifications</span></span>

<span data-ttu-id="cb261-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb261-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb261-121">Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="cb261-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cb261-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cb261-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cb261-123">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="cb261-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cb261-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="cb261-124">Header files</span></span>

<span data-ttu-id="cb261-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cb261-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="cb261-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cb261-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb261-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cb261-127">See also</span></span>



[<span data-ttu-id="cb261-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cb261-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cb261-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cb261-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cb261-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cb261-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cb261-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cb261-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

