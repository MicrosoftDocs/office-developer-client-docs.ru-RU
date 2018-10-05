---
title: Каноническое свойство PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382584"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="4a043-103">Каноническое свойство PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="4a043-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="4a043-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a043-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a043-105">Указывает, что пользователь выполнять задачи в минутах.</span><span class="sxs-lookup"><span data-stu-id="4a043-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4a043-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="4a043-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a043-107">dispidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="4a043-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="4a043-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="4a043-108">Property set:</span></span>  <br/> |<span data-ttu-id="4a043-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="4a043-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="4a043-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="4a043-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4a043-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="4a043-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="4a043-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="4a043-112">Data type:</span></span>  <br/> |<span data-ttu-id="4a043-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4a043-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4a043-114">Область:</span><span class="sxs-lookup"><span data-stu-id="4a043-114">Area:</span></span>  <br/> |<span data-ttu-id="4a043-115">Task</span><span class="sxs-lookup"><span data-stu-id="4a043-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a043-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="4a043-116">Remarks</span></span>

<span data-ttu-id="4a043-117">Значение должно быть больше или равно 0 и меньше, чем 0x5AE980DF (1,525,252,319), где 480 минут равно один день и 2400 минут равно 1 неделя (8 часов рабочего дня и пять дней в неделе).</span><span class="sxs-lookup"><span data-stu-id="4a043-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4a043-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4a043-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a043-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="4a043-119">Protocol specifications</span></span>

<span data-ttu-id="4a043-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a043-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a043-121">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="4a043-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4a043-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a043-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a043-123">Задает свойства и операции, допустимые для объектов списка рассылки и контактов.</span><span class="sxs-lookup"><span data-stu-id="4a043-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a043-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="4a043-124">Header files</span></span>

<span data-ttu-id="4a043-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a043-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a043-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="4a043-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a043-127">См. также</span><span class="sxs-lookup"><span data-stu-id="4a043-127">See also</span></span>



[<span data-ttu-id="4a043-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a043-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a043-129">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="4a043-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a043-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="4a043-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a043-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="4a043-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

