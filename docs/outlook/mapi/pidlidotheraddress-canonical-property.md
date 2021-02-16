---
title: Каноническое свойство PidLidOtherAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOtherAddress
api_type:
- COM
ms.assetid: 2b8acb69-4c84-4075-8457-d7aadce26c73
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0b05e83e48bf144ca317a64f90fb533f6d7d1c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359075"
---
# <a name="pidlidotheraddress-canonical-property"></a><span data-ttu-id="27c1c-103">Каноническое свойство PidLidOtherAddress</span><span class="sxs-lookup"><span data-stu-id="27c1c-103">PidLidOtherAddress Canonical Property</span></span>

  
  
<span data-ttu-id="27c1c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27c1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27c1c-105">Указывает полный адрес другого адреса контакта.</span><span class="sxs-lookup"><span data-stu-id="27c1c-105">Specifies the complete address of the contact's other address.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27c1c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="27c1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27c1c-107">dispidOtherAddress</span><span class="sxs-lookup"><span data-stu-id="27c1c-107">dispidOtherAddress</span></span>  <br/> |
|<span data-ttu-id="27c1c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="27c1c-108">Property set:</span></span>  <br/> |<span data-ttu-id="27c1c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="27c1c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="27c1c-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="27c1c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="27c1c-111">0x0000801C</span><span class="sxs-lookup"><span data-stu-id="27c1c-111">0x0000801C</span></span>  <br/> |
|<span data-ttu-id="27c1c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="27c1c-112">Data type:</span></span>  <br/> |<span data-ttu-id="27c1c-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27c1c-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="27c1c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="27c1c-114">Area:</span></span>  <br/> |<span data-ttu-id="27c1c-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="27c1c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27c1c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="27c1c-116">Remarks</span></span>

<span data-ttu-id="27c1c-117">Это свойство должно быть комбинацией других свойств физического адреса и основано на региональных региональных данных клиента.</span><span class="sxs-lookup"><span data-stu-id="27c1c-117">This property should be a combination of other physical address properties, and is based on client locale.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27c1c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="27c1c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27c1c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="27c1c-119">Protocol specifications</span></span>

<span data-ttu-id="27c1c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27c1c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27c1c-121">Предоставляет определение набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="27c1c-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27c1c-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27c1c-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27c1c-123">Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="27c1c-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27c1c-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="27c1c-124">Header files</span></span>

<span data-ttu-id="27c1c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27c1c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="27c1c-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="27c1c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27c1c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="27c1c-127">See also</span></span>



[<span data-ttu-id="27c1c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="27c1c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27c1c-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="27c1c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27c1c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="27c1c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27c1c-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="27c1c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

