---
title: Каноническое свойство PidLidCleanGlobalObjectId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCleanGlobalObjectId
api_type:
- COM
ms.assetid: 59b85997-7972-492e-9786-3f0f367dc3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c48fa333d407492b69da5287fa75c565bfd10e11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349219"
---
# <a name="pidlidcleanglobalobjectid-canonical-property"></a><span data-ttu-id="45680-103">Каноническое свойство PidLidCleanGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="45680-103">PidLidCleanGlobalObjectId Canonical Property</span></span>

  
  
<span data-ttu-id="45680-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45680-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45680-105">Указывает чистый глобальный **ObjectID**.</span><span class="sxs-lookup"><span data-stu-id="45680-105">Specifies the clean global **ObjectID**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45680-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="45680-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45680-107">Диспидклеанглобалобжид</span><span class="sxs-lookup"><span data-stu-id="45680-107">dispidCleanGlobalObjId</span></span>  <br/> |
|<span data-ttu-id="45680-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="45680-108">Property set:</span></span>  <br/> |<span data-ttu-id="45680-109">Псетид_митинг</span><span class="sxs-lookup"><span data-stu-id="45680-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="45680-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="45680-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="45680-111">0x00000023</span><span class="sxs-lookup"><span data-stu-id="45680-111">0x00000023</span></span>  <br/> |
|<span data-ttu-id="45680-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="45680-112">Data type:</span></span>  <br/> |<span data-ttu-id="45680-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="45680-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="45680-114">Область:</span><span class="sxs-lookup"><span data-stu-id="45680-114">Area:</span></span>  <br/> |<span data-ttu-id="45680-115">Meetings</span><span class="sxs-lookup"><span data-stu-id="45680-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45680-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="45680-116">Remarks</span></span>

<span data-ttu-id="45680-117">Формат этого свойства такой же, как и в **лид_глобал_обжид** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="45680-117">The format of this property is the same as that of **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)).</span></span> <span data-ttu-id="45680-118">Значение этого свойства должно быть равно значению **лид_глобал_обжид**, за исключением того, что поля их, Ил, M и D должны иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="45680-118">The value of this property must be equal to the value of **LID_GLOBAL_OBJID**, except the YH, YL, M, and D fields must be zero.</span></span> <span data-ttu-id="45680-119">Все объекты, ссылающиеся на экземпляр повторяющейся серии (в том числе потерянный экземпляр), а также на самом ряду повторяющихся данных, будут иметь одинаковое значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="45680-119">All objects that refer to an Instance of a recurring series (including an orphan instance), as well as the recurring series itself, will have the same value for this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45680-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="45680-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45680-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="45680-121">Protocol specifications</span></span>

<span data-ttu-id="45680-122">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45680-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45680-123">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="45680-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45680-124">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45680-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45680-125">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="45680-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45680-126">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="45680-126">Header files</span></span>

<span data-ttu-id="45680-127">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="45680-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="45680-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="45680-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45680-129">См. также</span><span class="sxs-lookup"><span data-stu-id="45680-129">See also</span></span>



[<span data-ttu-id="45680-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="45680-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="45680-131">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="45680-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45680-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="45680-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45680-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="45680-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

