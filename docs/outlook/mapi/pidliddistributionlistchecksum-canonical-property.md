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
ms.openlocfilehash: bba1e78d79800b1c8e56ad50ce1abb144d4c9aae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810250"
---
# <a name="pidliddistributionlistchecksum-canonical-property"></a><span data-ttu-id="c43b2-103">Каноническое свойство PidLidDistributionListChecksum</span><span class="sxs-lookup"><span data-stu-id="c43b2-103">PidLidDistributionListChecksum Canonical Property</span></span>

  
  
<span data-ttu-id="c43b2-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c43b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c43b2-105">Указывает, 32-разрядная версия циклическая проверка (контрольной СУММЫ-32) полиномиальной контрольная сумма для списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="c43b2-105">Specifies the 32-bit cyclic redundancy check (CRC-32) polynomial checksum for a personal distribution list.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c43b2-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c43b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c43b2-107">dispidDLChecksum</span><span class="sxs-lookup"><span data-stu-id="c43b2-107">dispidDLChecksum</span></span>  <br/> |
|<span data-ttu-id="c43b2-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c43b2-108">Property set:</span></span>  <br/> |<span data-ttu-id="c43b2-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c43b2-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c43b2-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c43b2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c43b2-111">0x0000804C</span><span class="sxs-lookup"><span data-stu-id="c43b2-111">0x0000804C</span></span>  <br/> |
|<span data-ttu-id="c43b2-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c43b2-112">Data type:</span></span>  <br/> |<span data-ttu-id="c43b2-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c43b2-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c43b2-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c43b2-114">Area:</span></span>  <br/> |<span data-ttu-id="c43b2-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="c43b2-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c43b2-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c43b2-116">Remarks</span></span>

<span data-ttu-id="c43b2-117">Значение этого свойства можно использовать для обнаружения при обновлении без обновления других свойств члена рассылки списка, вычисления контрольной СУММЫ-32 на существующий свойство **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) значение **dispidDLMembers** и сравнение со значением свойства **dispidDLChecksum** .</span><span class="sxs-lookup"><span data-stu-id="c43b2-117">The value of this property can be used to detect when the **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)) property was updated without updating the other personal distribution list member properties by computing the CRC-32 on the existing value of **dispidDLMembers** and comparing it with the value of the **dispidDLChecksum** property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c43b2-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c43b2-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c43b2-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c43b2-119">Protocol specifications</span></span>

<span data-ttu-id="c43b2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c43b2-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c43b2-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c43b2-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c43b2-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c43b2-122">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c43b2-123">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="c43b2-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c43b2-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c43b2-124">Header files</span></span>

<span data-ttu-id="c43b2-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c43b2-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c43b2-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c43b2-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c43b2-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c43b2-127">See also</span></span>



[<span data-ttu-id="c43b2-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c43b2-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c43b2-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c43b2-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c43b2-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c43b2-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c43b2-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c43b2-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

