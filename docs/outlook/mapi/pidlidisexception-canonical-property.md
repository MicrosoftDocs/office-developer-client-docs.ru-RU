---
title: Каноническое свойство PidLidIsException
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315451"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="5ad4c-103">Каноническое свойство PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="5ad4c-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="5ad4c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ad4c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ad4c-105">Указывает, что объект, представляющий исключение (включая потерянный экземпляр).</span><span class="sxs-lookup"><span data-stu-id="5ad4c-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5ad4c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="5ad4c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5ad4c-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="5ad4c-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="5ad4c-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="5ad4c-108">Property set:</span></span>  <br/> |<span data-ttu-id="5ad4c-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="5ad4c-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="5ad4c-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="5ad4c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5ad4c-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="5ad4c-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="5ad4c-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="5ad4c-112">Data type:</span></span>  <br/> |<span data-ttu-id="5ad4c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5ad4c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5ad4c-114">Область:</span><span class="sxs-lookup"><span data-stu-id="5ad4c-114">Area:</span></span>  <br/> |<span data-ttu-id="5ad4c-115">Собрания</span><span class="sxs-lookup"><span data-stu-id="5ad4c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ad4c-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ad4c-116">Remarks</span></span>

<span data-ttu-id="5ad4c-117">Значение FALSE указывает, что объект, представляющий повторяющиеся ряды или один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="5ad4c-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="5ad4c-118">Отсутствие этого свойства для любого объекта указывает значение FALSE, за исключением внедренного сообщения Exception, для которого предполагается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5ad4c-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5ad4c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5ad4c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5ad4c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="5ad4c-120">Protocol specifications</span></span>

<span data-ttu-id="5ad4c-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ad4c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ad4c-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="5ad4c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5ad4c-123">[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5ad4c-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5ad4c-124">Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="5ad4c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5ad4c-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="5ad4c-125">Header files</span></span>

<span data-ttu-id="5ad4c-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5ad4c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="5ad4c-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="5ad4c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5ad4c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="5ad4c-128">See also</span></span>



[<span data-ttu-id="5ad4c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="5ad4c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5ad4c-130">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="5ad4c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5ad4c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="5ad4c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5ad4c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="5ad4c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

