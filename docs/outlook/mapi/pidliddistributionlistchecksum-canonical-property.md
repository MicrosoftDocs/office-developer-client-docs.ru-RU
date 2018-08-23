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
ms.openlocfilehash: 44752e147569619589b23a380b2fefa511724ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571733"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="4dc91-103">Каноническое свойство PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="4dc91-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="4dc91-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4dc91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4dc91-105">Указывает, 32-разрядная версия циклическая проверка (контрольной СУММЫ-32) полиномиальной контрольная сумма для списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="4dc91-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4dc91-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4dc91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4dc91-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="4dc91-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="4dc91-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4dc91-108">Property set:</span></span>  <br/> |<span data-ttu-id="4dc91-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="4dc91-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="4dc91-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4dc91-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4dc91-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="4dc91-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="4dc91-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4dc91-112">Data type:</span></span>  <br/> |<span data-ttu-id="4dc91-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4dc91-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4dc91-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4dc91-114">Area:</span></span>  <br/> |<span data-ttu-id="4dc91-115">Contact</span><span class="sxs-lookup"><span data-stu-id="4dc91-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dc91-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4dc91-116">Remarks</span></span>

<span data-ttu-id="4dc91-117">Значение этого свойства можно использовать для обнаружения при обновлении без обновления других свойств члена рассылки списка, вычисления контрольной СУММЫ-32 на существующий свойство **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) значение **dispidDLMembers** и сравнение со значением свойства **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="4dc91-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4dc91-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4dc91-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4dc91-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4dc91-119">Protocol specifications</span></span>

<span data-ttu-id="4dc91-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dc91-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dc91-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4dc91-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4dc91-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4dc91-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4dc91-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="4dc91-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4dc91-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4dc91-124">Header files</span></span>

<span data-ttu-id="4dc91-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4dc91-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4dc91-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4dc91-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4dc91-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4dc91-127">See also</span></span>



[<span data-ttu-id="4dc91-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4dc91-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4dc91-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4dc91-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4dc91-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4dc91-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4dc91-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4dc91-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

