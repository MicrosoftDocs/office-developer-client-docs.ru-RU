---
title: Каноническое свойство PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316515"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="d5c27-103">Каноническое свойство PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="d5c27-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="d5c27-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5c27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5c27-105">Содержит битовую маску флагов, указывающих операции, доступные клиенту для объекта.</span><span class="sxs-lookup"><span data-stu-id="d5c27-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d5c27-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d5c27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d5c27-107">ПР_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="d5c27-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="d5c27-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d5c27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d5c27-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="d5c27-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="d5c27-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d5c27-110">Data type:</span></span>  <br/> |<span data-ttu-id="d5c27-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d5c27-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d5c27-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d5c27-112">Area:</span></span>  <br/> |<span data-ttu-id="d5c27-113">Свойства управления доступом</span><span class="sxs-lookup"><span data-stu-id="d5c27-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5c27-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d5c27-114">Remarks</span></span>

<span data-ttu-id="d5c27-115">Для клиента это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d5c27-115">This property is read-only for the client.</span></span> <span data-ttu-id="d5c27-116">Он должен быть побитовым **или** содержать от нуля или более значений из таблицы ниже.</span><span class="sxs-lookup"><span data-stu-id="d5c27-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="d5c27-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="d5c27-117">**Name**</span></span>|<span data-ttu-id="d5c27-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="d5c27-118">**Value**</span></span>|<span data-ttu-id="d5c27-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5c27-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5c27-120">МАПИ_АКЦЕСС_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="d5c27-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="d5c27-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5c27-121">0x00000001</span></span>  <br/> |<span data-ttu-id="d5c27-122">Запись</span><span class="sxs-lookup"><span data-stu-id="d5c27-122">Write</span></span>  <br/> |
|<span data-ttu-id="d5c27-123">МАПИ_АКЦЕСС_РЕАД</span><span class="sxs-lookup"><span data-stu-id="d5c27-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="d5c27-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d5c27-124">0x00000002</span></span>  <br/> |<span data-ttu-id="d5c27-125">Чтение</span><span class="sxs-lookup"><span data-stu-id="d5c27-125">Read</span></span>  <br/> |
|<span data-ttu-id="d5c27-126">МАПИ_АКЦЕСС_ДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="d5c27-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="d5c27-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d5c27-127">0x00000004</span></span>  <br/> |<span data-ttu-id="d5c27-128">Delete</span><span class="sxs-lookup"><span data-stu-id="d5c27-128">Delete</span></span>  <br/> |
|<span data-ttu-id="d5c27-129">МАПИ_АКЦЕСС_КРЕАТЕ_ХИЕРАРЧИ</span><span class="sxs-lookup"><span data-stu-id="d5c27-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="d5c27-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d5c27-130">0x00000008</span></span>  <br/> |<span data-ttu-id="d5c27-131">Создание вложенных папок в иерархии папок</span><span class="sxs-lookup"><span data-stu-id="d5c27-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="d5c27-132">МАПИ_АКЦЕСС_КРЕАТЕ_КОНТЕНТС</span><span class="sxs-lookup"><span data-stu-id="d5c27-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="d5c27-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5c27-133">0x00000010</span></span>  <br/> |<span data-ttu-id="d5c27-134">Создание сообщений с содержимым</span><span class="sxs-lookup"><span data-stu-id="d5c27-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="d5c27-135">МАПИ_АКЦЕСС_КРЕАТЕ_АССОЦИАТЕД</span><span class="sxs-lookup"><span data-stu-id="d5c27-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="d5c27-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d5c27-136">0x00000020</span></span>  <br/> |<span data-ttu-id="d5c27-137">Создание связанных сообщений с содержимым</span><span class="sxs-lookup"><span data-stu-id="d5c27-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="d5c27-138">Флаги МАПИ_АКЦЕСС_ДЕЛЕТЕ, МАПИ_АКЦЕСС_МОДИФИ и МАПИ_АКЦЕСС_РЕАД находятся в папках и объектах сообщений, а также в столбцах **пр_акцесс** в таблицах контента и связанных таблицах содержимого.</span><span class="sxs-lookup"><span data-stu-id="d5c27-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="d5c27-139">Флаги МАПИ_АКЦЕСС_КРЕАТЕ_АССОЦИАТЕД, МАПИ_АКЦЕСС_КРЕАТЕ_КОНТЕНТС и МАПИ_АКЦЕСС_КРЕАТЕ_ХИЕРАРЧИ доступны только для объектов Folder.</span><span class="sxs-lookup"><span data-stu-id="d5c27-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d5c27-140">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5c27-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d5c27-141">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d5c27-141">Protocol specifications</span></span>

<span data-ttu-id="d5c27-142">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5c27-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5c27-143">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d5c27-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d5c27-144">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d5c27-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d5c27-145">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="d5c27-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d5c27-146">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d5c27-146">Header files</span></span>

<span data-ttu-id="d5c27-147">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d5c27-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="d5c27-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d5c27-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="d5c27-149">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d5c27-149">Mapitags.h</span></span>
  
> <span data-ttu-id="d5c27-150">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="d5c27-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5c27-151">См. также</span><span class="sxs-lookup"><span data-stu-id="d5c27-151">See also</span></span>



[<span data-ttu-id="d5c27-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c27-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d5c27-153">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c27-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d5c27-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d5c27-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d5c27-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d5c27-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

