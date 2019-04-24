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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331173"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a><span data-ttu-id="43930-103">Каноническое свойство PidLidTaskActualEffort</span><span class="sxs-lookup"><span data-stu-id="43930-103">PidLidTaskActualEffort Canonical Property</span></span>

  
  
<span data-ttu-id="43930-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43930-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43930-105">Указывает количество минут, в течение которых пользователь выполнил задачу.</span><span class="sxs-lookup"><span data-stu-id="43930-105">Indicates the number of minutes that the user performed a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43930-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="43930-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43930-107">Диспидтаскактуалеффорт</span><span class="sxs-lookup"><span data-stu-id="43930-107">dispidTaskActualEffort</span></span>  <br/> |
|<span data-ttu-id="43930-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="43930-108">Property set:</span></span>  <br/> |<span data-ttu-id="43930-109">Псетид_таск</span><span class="sxs-lookup"><span data-stu-id="43930-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="43930-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="43930-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="43930-111">0x00008110</span><span class="sxs-lookup"><span data-stu-id="43930-111">0x00008110</span></span>  <br/> |
|<span data-ttu-id="43930-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="43930-112">Data type:</span></span>  <br/> |<span data-ttu-id="43930-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43930-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43930-114">Область:</span><span class="sxs-lookup"><span data-stu-id="43930-114">Area:</span></span>  <br/> |<span data-ttu-id="43930-115">Задача</span><span class="sxs-lookup"><span data-stu-id="43930-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43930-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43930-116">Remarks</span></span>

<span data-ttu-id="43930-117">Значение должно быть больше или равно 0 и меньше, чем 0x5AE980DF (1 525 252 319), где 480 минут равно 1 день и 2400 минут равно одной неделе (восемь часов в рабочем дне и пять дней в рабочей неделе).</span><span class="sxs-lookup"><span data-stu-id="43930-117">The value must be greater than or equal to 0 and less than 0x5AE980DF (1,525,252,319), where 480 minutes equal one day and 2400 minutes equal one week (eight hours in a work day and five days in a work week).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="43930-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="43930-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43930-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="43930-119">Protocol specifications</span></span>

<span data-ttu-id="43930-120">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43930-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43930-121">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="43930-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="43930-122">[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43930-122">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43930-123">Задает свойства и операции, которые являются допустимыми для объектов контакта и личного списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="43930-123">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43930-124">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="43930-124">Header files</span></span>

<span data-ttu-id="43930-125">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="43930-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="43930-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="43930-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43930-127">См. также</span><span class="sxs-lookup"><span data-stu-id="43930-127">See also</span></span>



[<span data-ttu-id="43930-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="43930-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43930-129">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="43930-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43930-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="43930-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43930-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="43930-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

