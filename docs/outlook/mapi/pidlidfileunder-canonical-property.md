---
title: Каноническое свойство PidLidFileUnder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnder
api_type:
- COM
ms.assetid: 55afc4bb-c5fc-4162-a293-7d82644b1965
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 02aa1766421f7c116eabac4c9661be1b5b1adee1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359572"
---
# <a name="pidlidfileunder-canonical-property"></a><span data-ttu-id="16e2f-103">Каноническое свойство PidLidFileUnder</span><span class="sxs-lookup"><span data-stu-id="16e2f-103">PidLidFileUnder Canonical Property</span></span>

  
  
<span data-ttu-id="16e2f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16e2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16e2f-105">Указывает имя, в котором будет храниться контакт при отображении списка контактов.</span><span class="sxs-lookup"><span data-stu-id="16e2f-105">Specifies the name under which the contact is filed when displaying a list of contacts.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="16e2f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="16e2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16e2f-107">Диспидфилеундер</span><span class="sxs-lookup"><span data-stu-id="16e2f-107">dispidFileUnder</span></span>  <br/> |
|<span data-ttu-id="16e2f-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="16e2f-108">Property set:</span></span>  <br/> |<span data-ttu-id="16e2f-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="16e2f-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="16e2f-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="16e2f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="16e2f-111">0x00008005</span><span class="sxs-lookup"><span data-stu-id="16e2f-111">0x00008005</span></span>  <br/> |
|<span data-ttu-id="16e2f-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="16e2f-112">Data type:</span></span>  <br/> |<span data-ttu-id="16e2f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16e2f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="16e2f-114">Область:</span><span class="sxs-lookup"><span data-stu-id="16e2f-114">Area:</span></span>  <br/> |<span data-ttu-id="16e2f-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="16e2f-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16e2f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="16e2f-116">Remarks</span></span>

<span data-ttu-id="16e2f-117">Приложение должно считать это свойство пустым ПТ_УНИКОДЕ, если оно отсутствует в контакте.</span><span class="sxs-lookup"><span data-stu-id="16e2f-117">The application should treat this property as an empty PT_UNICODE if it is missing from the contact.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="16e2f-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="16e2f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16e2f-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="16e2f-119">Protocol specifications</span></span>

<span data-ttu-id="16e2f-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16e2f-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16e2f-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="16e2f-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="16e2f-122">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16e2f-122">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16e2f-123">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="16e2f-123">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="16e2f-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="16e2f-124">Header files</span></span>

<span data-ttu-id="16e2f-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="16e2f-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="16e2f-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="16e2f-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16e2f-127">См. также</span><span class="sxs-lookup"><span data-stu-id="16e2f-127">See also</span></span>



[<span data-ttu-id="16e2f-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="16e2f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="16e2f-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="16e2f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16e2f-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="16e2f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16e2f-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="16e2f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

