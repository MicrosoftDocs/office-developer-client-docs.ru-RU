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
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="23c9f-103">Каноническое свойство PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="23c9f-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="23c9f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23c9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23c9f-105">Содержит битовую маску флагов, указывающих операции, доступные клиенту для объекта.</span><span class="sxs-lookup"><span data-stu-id="23c9f-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23c9f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="23c9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23c9f-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="23c9f-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="23c9f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="23c9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23c9f-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="23c9f-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="23c9f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="23c9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="23c9f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="23c9f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="23c9f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="23c9f-112">Area:</span></span>  <br/> |<span data-ttu-id="23c9f-113">Свойства управления доступом</span><span class="sxs-lookup"><span data-stu-id="23c9f-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23c9f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="23c9f-114">Remarks</span></span>

<span data-ttu-id="23c9f-115">Для клиента это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="23c9f-115">This property is read-only for the client.</span></span> <span data-ttu-id="23c9f-116">Он должен быть побитовым **или** содержать от нуля или более значений из таблицы ниже.</span><span class="sxs-lookup"><span data-stu-id="23c9f-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="23c9f-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="23c9f-117">**Name**</span></span>|<span data-ttu-id="23c9f-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="23c9f-118">**Value**</span></span>|<span data-ttu-id="23c9f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23c9f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23c9f-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="23c9f-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="23c9f-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="23c9f-121">0x00000001</span></span>  <br/> |<span data-ttu-id="23c9f-122">Запись</span><span class="sxs-lookup"><span data-stu-id="23c9f-122">Write</span></span>  <br/> |
|<span data-ttu-id="23c9f-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="23c9f-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="23c9f-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="23c9f-124">0x00000002</span></span>  <br/> |<span data-ttu-id="23c9f-125">Чтение</span><span class="sxs-lookup"><span data-stu-id="23c9f-125">Read</span></span>  <br/> |
|<span data-ttu-id="23c9f-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="23c9f-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="23c9f-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="23c9f-127">0x00000004</span></span>  <br/> |<span data-ttu-id="23c9f-128">Удаление</span><span class="sxs-lookup"><span data-stu-id="23c9f-128">Delete</span></span>  <br/> |
|<span data-ttu-id="23c9f-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="23c9f-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="23c9f-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="23c9f-130">0x00000008</span></span>  <br/> |<span data-ttu-id="23c9f-131">Создание вложенных папок в иерархии папок</span><span class="sxs-lookup"><span data-stu-id="23c9f-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="23c9f-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="23c9f-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="23c9f-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="23c9f-133">0x00000010</span></span>  <br/> |<span data-ttu-id="23c9f-134">Создание сообщений с содержимым</span><span class="sxs-lookup"><span data-stu-id="23c9f-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="23c9f-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="23c9f-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="23c9f-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="23c9f-136">0x00000020</span></span>  <br/> |<span data-ttu-id="23c9f-137">Создание связанных сообщений с содержимым</span><span class="sxs-lookup"><span data-stu-id="23c9f-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="23c9f-138">Флаги MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY и MAPI_ACCESS_READ находятся в папках и объектах сообщений, а также в столбцах **PR_ACCESS** в таблицах содержимого и связанных таблицах содержимого.</span><span class="sxs-lookup"><span data-stu-id="23c9f-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="23c9f-139">Флаги MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS и MAPI_ACCESS_CREATE_HIERARCHY доступны только для объектов Folder.</span><span class="sxs-lookup"><span data-stu-id="23c9f-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="23c9f-140">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="23c9f-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="23c9f-141">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="23c9f-141">Protocol specifications</span></span>

<span data-ttu-id="23c9f-142">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23c9f-142">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23c9f-143">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="23c9f-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="23c9f-144">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="23c9f-144">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="23c9f-145">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="23c9f-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="23c9f-146">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="23c9f-146">Header files</span></span>

<span data-ttu-id="23c9f-147">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="23c9f-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="23c9f-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="23c9f-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="23c9f-149">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="23c9f-149">Mapitags.h</span></span>
  
> <span data-ttu-id="23c9f-150">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="23c9f-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23c9f-151">См. также</span><span class="sxs-lookup"><span data-stu-id="23c9f-151">See also</span></span>



[<span data-ttu-id="23c9f-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="23c9f-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23c9f-153">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="23c9f-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23c9f-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="23c9f-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23c9f-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="23c9f-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

