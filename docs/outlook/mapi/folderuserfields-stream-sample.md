---
title: Пример потока FolderUserFields
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
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="792d9-103">Пример потока FolderUserFields</span><span class="sxs-lookup"><span data-stu-id="792d9-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="792d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="792d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="792d9-105">В этом разделе описывается пример потока FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="792d9-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="792d9-106">Поток содержит определение пользовательского  `TextField1` поля.</span><span class="sxs-lookup"><span data-stu-id="792d9-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="792d9-107">Типом является **Text,** а поток FolderUserFields содержит части FolderUserFieldsAnsi и FolderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="792d9-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="792d9-108">Дополнительные сведения см. в [подстроках потока полей папок.](folder-fields-stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="792d9-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="792d9-109">Дамп данных</span><span class="sxs-lookup"><span data-stu-id="792d9-109">Data dump</span></span>

<span data-ttu-id="792d9-110">Ниже показан дамп данных потока, который будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="792d9-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="792d9-111">Смещение потока</span><span class="sxs-lookup"><span data-stu-id="792d9-111">Stream offset</span></span>|<span data-ttu-id="792d9-112">Данные вбайт</span><span class="sxs-lookup"><span data-stu-id="792d9-112">Data bytes</span></span>|<span data-ttu-id="792d9-113">Данные ASCII</span><span class="sxs-lookup"><span data-stu-id="792d9-113">ASCII data</span></span>|
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
   

<span data-ttu-id="792d9-114">Ниже приводится анализ примеров данных для потока **FolderUserFields:**</span><span class="sxs-lookup"><span data-stu-id="792d9-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="792d9-115">FolderUserFieldsAnsi: смещение 0x0.</span><span class="sxs-lookup"><span data-stu-id="792d9-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="792d9-116">FieldDefinitionCount: 0x0 смещения, 4 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="792d9-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="792d9-117">FieldDefinitions: 0x4 смещения, массив из 2 потоков FolderFieldDefinitionA.</span><span class="sxs-lookup"><span data-stu-id="792d9-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="792d9-118">**Первый элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="792d9-118">**First array element**:</span></span>
    
    - <span data-ttu-id="792d9-119">FieldType: смещение 0x4, 4 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="792d9-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="792d9-120">FieldNameLength: 0x8 смещения, 2 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="792d9-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="792d9-121">FieldName: 0xA offset, массив из 10 chars.</span><span class="sxs-lookup"><span data-stu-id="792d9-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="792d9-122">Строковое значение ANSI: TextField1.</span><span class="sxs-lookup"><span data-stu-id="792d9-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="792d9-123">Common: Offset 0x14.</span><span class="sxs-lookup"><span data-stu-id="792d9-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="792d9-124">PropSetGuid: offset 0x14, 16 bytes: {00020329-0000-0000-C000-00000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="792d9-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="792d9-125">fcapm: смещение 0x24, 4 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="792d9-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="792d9-126">dwString: смещение 0x28, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-127">dwBitmap: смещение 0x2C, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-128">dwDisplay: смещение 0x30, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-129">iFmt: смещение 0x34, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-130">wszFormulaLength: 0x38 смещения, 2 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="792d9-131">wszFormula: 0x3A смещения, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="792d9-132">Пустое строко значение.</span><span class="sxs-lookup"><span data-stu-id="792d9-132">Empty string value.</span></span>
    
    <span data-ttu-id="792d9-133">**Второй элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="792d9-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="792d9-134">FieldType: 0x3A смещения, 4 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="792d9-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="792d9-135">FieldNameLength: 0x3E смещения, 2 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="792d9-136">FieldName: offset 0x40, массив 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="792d9-137">Пустое строко значение.</span><span class="sxs-lookup"><span data-stu-id="792d9-137">Empty string value.</span></span>
      
    - <span data-ttu-id="792d9-138">Common: Offset 0x40.</span><span class="sxs-lookup"><span data-stu-id="792d9-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="792d9-139">PropSetGuid: смещение 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="792d9-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="792d9-140">fcapm: смещение 0x50, 4 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="792d9-141">dwString: смещение 0x54, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-142">dwBitmap: смещение 0x58, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-143">dwDisplay: смещение 0x5C, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-144">iFmt: смещение 0x60, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-145">wszFormulaLength: 0x64 смещения, 2 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="792d9-146">wszFormula: 0x66 смещения, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="792d9-147">Пустое строко значение.</span><span class="sxs-lookup"><span data-stu-id="792d9-147">Empty string value.</span></span>
    
- <span data-ttu-id="792d9-148">FolderUserFieldsUnicode: offset 0x66.</span><span class="sxs-lookup"><span data-stu-id="792d9-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="792d9-149">FieldDefinitionCount: offset 0x66, 4 bytes: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="792d9-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="792d9-150">FieldDefinitions: 0x6A offset, массив из 2 потоков FolderFieldDefinitionW.</span><span class="sxs-lookup"><span data-stu-id="792d9-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="792d9-151">**Первый элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="792d9-151">**First array element**:</span></span>
    
    - <span data-ttu-id="792d9-152">FieldType: 0x6A смещения, 4 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="792d9-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="792d9-153">FieldNameLength: 0x6E смещения, 2 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="792d9-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="792d9-154">FieldName: 0x70, массив из 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="792d9-155">Строковое значение Юникода: TextField1.</span><span class="sxs-lookup"><span data-stu-id="792d9-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="792d9-156">Common: Offset 0x84.</span><span class="sxs-lookup"><span data-stu-id="792d9-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="792d9-157">PropSetGuid: offset 0x84, 16 bytes: {00020329-0000-0000-C000-00000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="792d9-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="792d9-158">fcapm: смещение 0x94, 4 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="792d9-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="792d9-159">dwString: смещение 0x98, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-160">dwBitmap: смещение 0x9C, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-161">dwDisplay: смещение 0xA0, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-162">iFmt: смещение 0xA4, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-163">wszFormulaLength: 0xA8 смещения, 2 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="792d9-164">wszFormula: 0xAA смещения, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="792d9-165">Пустое строко значение.</span><span class="sxs-lookup"><span data-stu-id="792d9-165">Empty string value.</span></span>
    
    <span data-ttu-id="792d9-166">**Второй элемент массива:**</span><span class="sxs-lookup"><span data-stu-id="792d9-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="792d9-167">FieldType: 0xAA смещения, 4 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="792d9-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="792d9-168">FieldNameLength: 0xAE смещения, 2 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="792d9-169">FieldName: offset 0xB0, массив 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="792d9-170">Пустое строко значение.</span><span class="sxs-lookup"><span data-stu-id="792d9-170">Empty string value.</span></span>
      
    - <span data-ttu-id="792d9-171">Common: Offset 0xB0.</span><span class="sxs-lookup"><span data-stu-id="792d9-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="792d9-172">PropSetGuid: offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="792d9-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="792d9-173">fcapm: смещение 0xC0, 4 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="792d9-174">dwString: смещение 0xC4, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-175">dwBitmap: смещение 0xC8, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-176">dwDisplay: смещение 0xCC, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-177">iFmt: смещение 0xD0, 4 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="792d9-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="792d9-178">wszFormulaLength: 0xD4 смещения, 2 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="792d9-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="792d9-179">wszFormula: 0xD6 смещения, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="792d9-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="792d9-180">Пустое строко значение.</span><span class="sxs-lookup"><span data-stu-id="792d9-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="792d9-181">См. также</span><span class="sxs-lookup"><span data-stu-id="792d9-181">See also</span></span>

- [<span data-ttu-id="792d9-182">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="792d9-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="792d9-183">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="792d9-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="792d9-184">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="792d9-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="792d9-185">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="792d9-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="792d9-186">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="792d9-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="792d9-187">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="792d9-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="792d9-188">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="792d9-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

