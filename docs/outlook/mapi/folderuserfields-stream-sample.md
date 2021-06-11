---
title: Пример потока folderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433978"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="9df47-103">Пример потока folderUserFields</span><span class="sxs-lookup"><span data-stu-id="9df47-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="9df47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9df47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9df47-105">В этом разделе описывается пример потока FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="9df47-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="9df47-106">Поток содержит определение поля, определяемого пользователем,  `TextField1` .</span><span class="sxs-lookup"><span data-stu-id="9df47-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="9df47-107">Тип — **Текст,** а поток FolderUserFields содержит как части FolderUserFieldsAnsi, так и folderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="9df47-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="9df47-108">Дополнительные сведения см. [в рубке Folder Fields Stream Structures.](folder-fields-stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="9df47-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="9df47-109">Сброс данных</span><span class="sxs-lookup"><span data-stu-id="9df47-109">Data dump</span></span>

<span data-ttu-id="9df47-110">Ниже приводится сброс данных потока, который будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="9df47-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="9df47-111">Смещение потока</span><span class="sxs-lookup"><span data-stu-id="9df47-111">Stream offset</span></span>|<span data-ttu-id="9df47-112">Bytes data</span><span class="sxs-lookup"><span data-stu-id="9df47-112">Data bytes</span></span>|<span data-ttu-id="9df47-113">Данные ASCII</span><span class="sxs-lookup"><span data-stu-id="9df47-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="9df47-114">Ниже приводится анализ примерных данных для потока **FolderUserFields:**</span><span class="sxs-lookup"><span data-stu-id="9df47-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="9df47-115">FolderUserFieldsAnsi: смещение 0x0.</span><span class="sxs-lookup"><span data-stu-id="9df47-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="9df47-116">FieldDefinitionCount: смещение 0x0, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="9df47-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="9df47-117">FieldDefinitions: Смещение 0x4, массив из 2 потоков FolderFieldDefinitionA.</span><span class="sxs-lookup"><span data-stu-id="9df47-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="9df47-118">**Первый элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="9df47-118">**First array element**:</span></span>
    
    - <span data-ttu-id="9df47-119">FieldType: смещение 0x4, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="9df47-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="9df47-120">FieldNameLength: смещение 0x8, 2 bytes: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="9df47-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="9df47-121">Имя поля: смещение 0xA, массив из 10 ОКР.</span><span class="sxs-lookup"><span data-stu-id="9df47-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="9df47-122">Строковое значение ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="9df47-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="9df47-123">Общие: смещение 0x14.</span><span class="sxs-lookup"><span data-stu-id="9df47-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="9df47-124">PropSetGuid: Смещение 0x14, 16 bytes: {00020329-0000-0000-00000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="9df47-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="9df47-125">fcapm: Смещение 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="9df47-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="9df47-126">dwString. Смещение 0x28, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-127">dwBitmap. Смещение 0x2C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-128">dwDisplay: Смещение 0x30, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-129">iFmt. Смещение 0x34, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-130">wszFormulaLength: смещение 0x38, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="9df47-131">wszFormula: смещение 0x3A, массив 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="9df47-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="9df47-132">Пустое значение строки.</span><span class="sxs-lookup"><span data-stu-id="9df47-132">Empty string value.</span></span>
    
    <span data-ttu-id="9df47-133">**Второй элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="9df47-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="9df47-134">FieldType: смещение 0x3A, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="9df47-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="9df47-135">FieldNameLength: Смещение 0x3E, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="9df47-136">Имя поля: смещение 0x40, массив из 0 ОКР.</span><span class="sxs-lookup"><span data-stu-id="9df47-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="9df47-137">Пустое значение строки.</span><span class="sxs-lookup"><span data-stu-id="9df47-137">Empty string value.</span></span>
      
    - <span data-ttu-id="9df47-138">Общие: смещение 0x40.</span><span class="sxs-lookup"><span data-stu-id="9df47-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="9df47-139">PropSetGuid: Смещение 0x40, 16 {00000000-0000-0000-0000-000000000000} bytes: (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="9df47-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="9df47-140">fcapm. Смещение 0x50, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="9df47-141">dwString: Смещение 0x54, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-142">dwBitmap. Смещение 0x58, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-143">dwDisplay: смещение 0x5C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-144">iFmt. Смещение 0x60, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-145">wszFormulaLength: смещение 0x64, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="9df47-146">wszFormula: смещение 0x66, массив 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="9df47-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="9df47-147">Пустое значение строки.</span><span class="sxs-lookup"><span data-stu-id="9df47-147">Empty string value.</span></span>
    
- <span data-ttu-id="9df47-148">FolderUserFieldsUnicode: Смещение 0x66.</span><span class="sxs-lookup"><span data-stu-id="9df47-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="9df47-149">FieldDefinitionCount: смещение 0x66, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="9df47-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="9df47-150">FieldDefinitions: Смещение 0x6A, массив из 2 потоков FolderFieldDefinitionW.</span><span class="sxs-lookup"><span data-stu-id="9df47-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="9df47-151">**Первый элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="9df47-151">**First array element**:</span></span>
    
    - <span data-ttu-id="9df47-152">FieldType: смещение 0x6A, 4 bytes: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="9df47-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="9df47-153">FieldNameLength: Смещение 0x6E, 2 bytes: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="9df47-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="9df47-154">Имя поля: смещение 0x70, массив из 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="9df47-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="9df47-155">Значение строки Unicode: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="9df47-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="9df47-156">Общие: смещение 0x84.</span><span class="sxs-lookup"><span data-stu-id="9df47-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="9df47-157">PropSetGuid: смещение 0x84, 16 bytes: {00020329-0000-0000-00000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="9df47-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="9df47-158">fcapm. Смещение 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="9df47-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="9df47-159">dwString: смещение 0x98, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-160">dwBitmap. Смещение 0x9C, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-161">dwDisplay. Смещение 0xA0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-162">iFmt. Смещение 0xA4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-163">wszFormulaLength: смещение 0xA8, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="9df47-164">wszFormula: смещение 0xAA, массив 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="9df47-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="9df47-165">Пустое значение строки.</span><span class="sxs-lookup"><span data-stu-id="9df47-165">Empty string value.</span></span>
    
    <span data-ttu-id="9df47-166">**Второй элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="9df47-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="9df47-167">FieldType: смещение 0xAA, 4 bytes: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="9df47-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="9df47-168">FieldNameLength: смещение 0xAE, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="9df47-169">Имя поля: смещение 0xB0, массив 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="9df47-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="9df47-170">Пустое значение строки.</span><span class="sxs-lookup"><span data-stu-id="9df47-170">Empty string value.</span></span>
      
    - <span data-ttu-id="9df47-171">Общие: смещение 0xB0.</span><span class="sxs-lookup"><span data-stu-id="9df47-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="9df47-172">PropSetGuid: Смещение 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="9df47-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="9df47-173">fcapm. Смещение 0xC0, 4 bytes: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="9df47-174">dwString. Смещение 0xC4, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-175">dwBitmap. Смещение 0xC8, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-176">dwDisplay: смещение 0xCC, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-177">iFmt. Смещение 0xD0, 4 bytes: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="9df47-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="9df47-178">wszFormulaLength: смещение 0xD4, 2 bytes: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="9df47-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="9df47-179">wszFormula: смещение 0xD6, массив 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="9df47-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="9df47-180">Пустое значение строки.</span><span class="sxs-lookup"><span data-stu-id="9df47-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9df47-181">См. также</span><span class="sxs-lookup"><span data-stu-id="9df47-181">See also</span></span>

- [<span data-ttu-id="9df47-182">Outlook Элементы и поля</span><span class="sxs-lookup"><span data-stu-id="9df47-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="9df47-183">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="9df47-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="9df47-184">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="9df47-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="9df47-185">Структура skipBlock Stream</span><span class="sxs-lookup"><span data-stu-id="9df47-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="9df47-186">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="9df47-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="9df47-187">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="9df47-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="9df47-188">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="9df47-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

