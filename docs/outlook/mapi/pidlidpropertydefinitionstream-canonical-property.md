---
title: Каноническое свойство PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b5ddb87111cfb0039cb1150338945615bbd5afc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315941"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a><span data-ttu-id="19ccb-103">Каноническое свойство PidLidPropertyDefinitionStream</span><span class="sxs-lookup"><span data-stu-id="19ccb-103">PidLidPropertyDefinitionStream Canonical Property</span></span>

  
  
<span data-ttu-id="19ccb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19ccb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19ccb-105">Представляет определения пользовательских полей и параметров привязки данных встроенных полей сообщения.</span><span class="sxs-lookup"><span data-stu-id="19ccb-105">Represents definitions of user-defined fields and data-binding settings of built-in fields of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="19ccb-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="19ccb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="19ccb-107">dispidPropDefStream</span><span class="sxs-lookup"><span data-stu-id="19ccb-107">dispidPropDefStream</span></span>  <br/> |
|<span data-ttu-id="19ccb-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="19ccb-108">Property set:</span></span>  <br/> |<span data-ttu-id="19ccb-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="19ccb-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="19ccb-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="19ccb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="19ccb-111">0x00008540</span><span class="sxs-lookup"><span data-stu-id="19ccb-111">0x00008540</span></span>  <br/> |
|<span data-ttu-id="19ccb-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="19ccb-112">Data type:</span></span>  <br/> |<span data-ttu-id="19ccb-113">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="19ccb-113">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="19ccb-114">Область:</span><span class="sxs-lookup"><span data-stu-id="19ccb-114">Area:</span></span>  <br/> |<span data-ttu-id="19ccb-115">Настройка времени запуска</span><span class="sxs-lookup"><span data-stu-id="19ccb-115">Run-time configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="19ccb-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="19ccb-116">Remarks</span></span>

<span data-ttu-id="19ccb-117">Значение свойства **PidLidPropertyDefinitionStream** сохранено как часть пользовательского определения формы для сообщения.</span><span class="sxs-lookup"><span data-stu-id="19ccb-117">The value of the **PidLidPropertyDefinitionStream** property is saved as part of the custom form definition for the message.</span></span> 
  
<span data-ttu-id="19ccb-118">Значение этого свойства — двоичный поток.</span><span class="sxs-lookup"><span data-stu-id="19ccb-118">The value of this property is a binary stream.</span></span> <span data-ttu-id="19ccb-119">Сведения о структуре этого потока см. в структуре [потока PropertyDefinition.](propertydefinition-stream-structure.md)</span><span class="sxs-lookup"><span data-stu-id="19ccb-119">For information on the structure of this stream, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="19ccb-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="19ccb-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="19ccb-121">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="19ccb-121">Protocol specifications</span></span>

<span data-ttu-id="19ccb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="19ccb-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="19ccb-123">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="19ccb-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="19ccb-124">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="19ccb-124">Header files</span></span>

<span data-ttu-id="19ccb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="19ccb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="19ccb-126">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="19ccb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19ccb-127">См. также</span><span class="sxs-lookup"><span data-stu-id="19ccb-127">See also</span></span>



[<span data-ttu-id="19ccb-128">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="19ccb-128">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="19ccb-129">Добавление определения для нового поля User-Defined</span><span class="sxs-lookup"><span data-stu-id="19ccb-129">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="19ccb-130">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="19ccb-130">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="19ccb-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19ccb-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="19ccb-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="19ccb-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="19ccb-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="19ccb-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="19ccb-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="19ccb-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

