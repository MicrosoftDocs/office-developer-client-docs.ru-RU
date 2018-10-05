---
title: Каноническое свойство PidLidLogFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387239"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="ca75c-103">Каноническое свойство PidLidLogFlags</span><span class="sxs-lookup"><span data-stu-id="ca75c-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="ca75c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca75c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca75c-105">Содержит метаданные о журнале.</span><span class="sxs-lookup"><span data-stu-id="ca75c-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca75c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ca75c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ca75c-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="ca75c-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="ca75c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ca75c-108">Property set:</span></span>  <br/> |<span data-ttu-id="ca75c-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="ca75c-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="ca75c-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ca75c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ca75c-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="ca75c-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="ca75c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ca75c-112">Data type:</span></span>  <br/> |<span data-ttu-id="ca75c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ca75c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ca75c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ca75c-114">Area:</span></span>  <br/> |<span data-ttu-id="ca75c-115">������</span><span class="sxs-lookup"><span data-stu-id="ca75c-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca75c-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ca75c-116">Remarks</span></span>

<span data-ttu-id="ca75c-117">Битовое поле, которое содержит метаданные о журнале должен быть ноль или «0x40000000».</span><span class="sxs-lookup"><span data-stu-id="ca75c-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ca75c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ca75c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ca75c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ca75c-119">Protocol specifications</span></span>

<span data-ttu-id="ca75c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca75c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca75c-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ca75c-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ca75c-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ca75c-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ca75c-123">Задает свойства и операции, допустимые для журналов.</span><span class="sxs-lookup"><span data-stu-id="ca75c-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ca75c-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ca75c-124">Header files</span></span>

<span data-ttu-id="ca75c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca75c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ca75c-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ca75c-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca75c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ca75c-127">See also</span></span>



[<span data-ttu-id="ca75c-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ca75c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ca75c-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ca75c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ca75c-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ca75c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ca75c-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ca75c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

