---
title: Каноническое свойство PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336927"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="02320-103">Каноническое свойство PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="02320-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="02320-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02320-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02320-105">Представляет дату и время окончания сообщения журнала.</span><span class="sxs-lookup"><span data-stu-id="02320-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="02320-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="02320-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02320-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="02320-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="02320-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="02320-108">Property set:</span></span>  <br/> |<span data-ttu-id="02320-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="02320-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="02320-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="02320-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="02320-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="02320-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="02320-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="02320-112">Data type:</span></span>  <br/> |<span data-ttu-id="02320-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="02320-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="02320-114">Область:</span><span class="sxs-lookup"><span data-stu-id="02320-114">Area:</span></span>  <br/> |<span data-ttu-id="02320-115">Журнал</span><span class="sxs-lookup"><span data-stu-id="02320-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02320-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="02320-116">Remarks</span></span>

<span data-ttu-id="02320-117">Время окончания действия в UTC, которое должно быть равно свойству **dispidCommonEnd** [(PidLidCommonEnd)](pidlidcommonend-canonical-property.md)и больше или равно свойству **dispidLogStart** ([PidLidLogStart).](pidlidlogstart-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="02320-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="02320-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02320-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02320-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="02320-119">Protocol specifications</span></span>

<span data-ttu-id="02320-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02320-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02320-121">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="02320-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="02320-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02320-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02320-123">Указывает свойства и операции, которые разрешены для журналов.</span><span class="sxs-lookup"><span data-stu-id="02320-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02320-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="02320-124">Header files</span></span>

<span data-ttu-id="02320-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02320-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="02320-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="02320-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02320-127">См. также</span><span class="sxs-lookup"><span data-stu-id="02320-127">See also</span></span>



[<span data-ttu-id="02320-128">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02320-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02320-129">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02320-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02320-130">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="02320-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02320-131">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="02320-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

