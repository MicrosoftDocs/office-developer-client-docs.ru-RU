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
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810793"
---
# <a name="pidtagaccess-canonical-property"></a><span data-ttu-id="fbd90-103">Каноническое свойство PidTagAccess</span><span class="sxs-lookup"><span data-stu-id="fbd90-103">PidTagAccess Canonical Property</span></span>

  
  
<span data-ttu-id="fbd90-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbd90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbd90-105">Содержит битовую маску флагов, указывающее, операции, которые доступны для клиента для объекта.</span><span class="sxs-lookup"><span data-stu-id="fbd90-105">Contains a bitmask of flags indicating the operations that are available to the client for the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fbd90-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="fbd90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fbd90-107">PR_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fbd90-107">PR_ACCESS</span></span>  <br/> |
|<span data-ttu-id="fbd90-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="fbd90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fbd90-109">0x0FF4</span><span class="sxs-lookup"><span data-stu-id="fbd90-109">0x0FF4</span></span>  <br/> |
|<span data-ttu-id="fbd90-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="fbd90-110">Data type:</span></span>  <br/> |<span data-ttu-id="fbd90-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="fbd90-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="fbd90-112">Область:</span><span class="sxs-lookup"><span data-stu-id="fbd90-112">Area:</span></span>  <br/> |<span data-ttu-id="fbd90-113">Элемент управления доступа к свойствам</span><span class="sxs-lookup"><span data-stu-id="fbd90-113">Access Control Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbd90-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="fbd90-114">Remarks</span></span>

<span data-ttu-id="fbd90-115">Это свойство доступно только для чтения для клиента.</span><span class="sxs-lookup"><span data-stu-id="fbd90-115">This property is read-only for the client.</span></span> <span data-ttu-id="fbd90-116">Он должен быть побитовое **или** ноль или больше значений из следующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="fbd90-116">It must be a bitwise **OR** of zero or more values from the following table.</span></span> 
  
|<span data-ttu-id="fbd90-117">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fbd90-117">**Name**</span></span>|<span data-ttu-id="fbd90-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="fbd90-118">**Value**</span></span>|<span data-ttu-id="fbd90-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbd90-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fbd90-120">MAPI_ACCESS_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fbd90-120">MAPI_ACCESS_MODIFY</span></span>  <br/> |<span data-ttu-id="fbd90-121">0x00000001</span><span class="sxs-lookup"><span data-stu-id="fbd90-121">0x00000001</span></span>  <br/> |<span data-ttu-id="fbd90-122">Запись</span><span class="sxs-lookup"><span data-stu-id="fbd90-122">Write</span></span>  <br/> |
|<span data-ttu-id="fbd90-123">MAPI_ACCESS_READ</span><span class="sxs-lookup"><span data-stu-id="fbd90-123">MAPI_ACCESS_READ</span></span>  <br/> |<span data-ttu-id="fbd90-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="fbd90-124">0x00000002</span></span>  <br/> |<span data-ttu-id="fbd90-125">Чтение</span><span class="sxs-lookup"><span data-stu-id="fbd90-125">Read</span></span>  <br/> |
|<span data-ttu-id="fbd90-126">MAPI_ACCESS_DELETE</span><span class="sxs-lookup"><span data-stu-id="fbd90-126">MAPI_ACCESS_DELETE</span></span>  <br/> |<span data-ttu-id="fbd90-127">0x00000004</span><span class="sxs-lookup"><span data-stu-id="fbd90-127">0x00000004</span></span>  <br/> |<span data-ttu-id="fbd90-128">Delete</span><span class="sxs-lookup"><span data-stu-id="fbd90-128">Delete</span></span>  <br/> |
|<span data-ttu-id="fbd90-129">MAPI_ACCESS_CREATE_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="fbd90-129">MAPI_ACCESS_CREATE_HIERARCHY</span></span>  <br/> |<span data-ttu-id="fbd90-130">0x00000008</span><span class="sxs-lookup"><span data-stu-id="fbd90-130">0x00000008</span></span>  <br/> |<span data-ttu-id="fbd90-131">Создание вложенных папок в иерархии папок</span><span class="sxs-lookup"><span data-stu-id="fbd90-131">Create subfolders in the folder hierarchy</span></span>  <br/> |
|<span data-ttu-id="fbd90-132">MAPI_ACCESS_CREATE_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="fbd90-132">MAPI_ACCESS_CREATE_CONTENTS</span></span>  <br/> |<span data-ttu-id="fbd90-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbd90-133">0x00000010</span></span>  <br/> |<span data-ttu-id="fbd90-134">Создание сообщения</span><span class="sxs-lookup"><span data-stu-id="fbd90-134">Create content messages</span></span>  <br/> |
|<span data-ttu-id="fbd90-135">MAPI_ACCESS_CREATE_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="fbd90-135">MAPI_ACCESS_CREATE_ASSOCIATED</span></span>  <br/> |<span data-ttu-id="fbd90-136">0x00000020</span><span class="sxs-lookup"><span data-stu-id="fbd90-136">0x00000020</span></span>  <br/> |<span data-ttu-id="fbd90-137">Создание связанного содержимого сообщений</span><span class="sxs-lookup"><span data-stu-id="fbd90-137">Create associated content messages</span></span>  <br/> |
   
<span data-ttu-id="fbd90-138">Флаги MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY и MAPI_ACCESS_READ находятся в папке и объекты сообщений и в столбце **PR_ACCESS** в содержимое и связанного содержимого таблицы.</span><span class="sxs-lookup"><span data-stu-id="fbd90-138">The MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY, and MAPI_ACCESS_READ flags are found on folder and message objects and in the **PR_ACCESS** column in contents tables and associated contents tables.</span></span> <span data-ttu-id="fbd90-139">Флаги MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS и MAPI_ACCESS_CREATE_HIERARCHY находятся в папке объекты только.</span><span class="sxs-lookup"><span data-stu-id="fbd90-139">The MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS, and MAPI_ACCESS_CREATE_HIERARCHY flags are found on folder objects only.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fbd90-140">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fbd90-140">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fbd90-141">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="fbd90-141">Protocol specifications</span></span>

<span data-ttu-id="fbd90-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbd90-142">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbd90-143">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fbd90-143">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fbd90-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fbd90-144">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fbd90-145">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="fbd90-145">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fbd90-146">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="fbd90-146">Header files</span></span>

<span data-ttu-id="fbd90-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fbd90-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="fbd90-148">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="fbd90-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="fbd90-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fbd90-149">Mapitags.h</span></span>
  
> <span data-ttu-id="fbd90-150">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="fbd90-150">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fbd90-151">См. также</span><span class="sxs-lookup"><span data-stu-id="fbd90-151">See also</span></span>



[<span data-ttu-id="fbd90-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fbd90-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fbd90-153">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="fbd90-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fbd90-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="fbd90-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fbd90-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="fbd90-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

