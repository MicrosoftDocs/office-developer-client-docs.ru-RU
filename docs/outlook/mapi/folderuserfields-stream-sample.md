---
title: Пример FolderUserFields потока
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 72c71a6109f55f7ec06499e214a1aa11292a9e52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808456"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="200f8-103">Пример FolderUserFields потока</span><span class="sxs-lookup"><span data-stu-id="200f8-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="200f8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="200f8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="200f8-105">В этом разделе описывается пример FolderUserFields потока.</span><span class="sxs-lookup"><span data-stu-id="200f8-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="200f8-106">Поток содержит определение того, пользовательские поля, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="200f8-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="200f8-107">Тип — **текст**, а в потоке FolderUserFields содержит части FolderUserFieldsAnsi и FolderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="200f8-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="200f8-108">Для получения дополнительных сведений см [Структуры папок поля потока](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="200f8-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="200f8-109">Дамп данных</span><span class="sxs-lookup"><span data-stu-id="200f8-109">Data dump</span></span>

<span data-ttu-id="200f8-110">Ниже приведен дамп данных потока как она будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="200f8-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="200f8-111">Смещение потока</span><span class="sxs-lookup"><span data-stu-id="200f8-111">Stream offset</span></span>|<span data-ttu-id="200f8-112">Байт данных</span><span class="sxs-lookup"><span data-stu-id="200f8-112">Data bytes</span></span>|<span data-ttu-id="200f8-113">Данные в формате ASCII</span><span class="sxs-lookup"><span data-stu-id="200f8-113">ASCII data</span></span>|
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
   

<span data-ttu-id="200f8-114">Ниже приведен синтаксического анализа образца данных для потока **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="200f8-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="200f8-115">FolderUserFieldsAnsi: Смещения 0x0.</span><span class="sxs-lookup"><span data-stu-id="200f8-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="200f8-116">FieldDefinitionCount: Смещение 0x0, 4 байта: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="200f8-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="200f8-117">FieldDefinitions: Смещение 0x4, массива 2 FolderFieldDefinitionA потоков.</span><span class="sxs-lookup"><span data-stu-id="200f8-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="200f8-118">**Первый элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="200f8-118">**First array element**:</span></span>
    
    - <span data-ttu-id="200f8-119">FieldType: Смещение 0x4, 4 байта: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="200f8-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="200f8-120">FieldNameLength: Смещение 0x8, два байта: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="200f8-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="200f8-121">FieldName: Смещение 0xA, массив 10 символов.</span><span class="sxs-lookup"><span data-stu-id="200f8-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="200f8-122">Значение строки ANSI: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="200f8-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="200f8-123">Общие: Смещение 0x14.</span><span class="sxs-lookup"><span data-stu-id="200f8-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="200f8-124">PropSetGuid: Смещение 0x14 16 байт: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="200f8-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="200f8-125">fcapm: смещение 0x24 4 байта: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="200f8-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="200f8-126">dwString: смещение 0x28, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-127">dwBitmap: смещение 0x2C 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-128">dwDisplay: смещение 0x30 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-129">iFmt: смещение 0x34 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-130">wszFormulaLength: смещение 0x38 два байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="200f8-131">wszFormula: смещение 0x3A, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="200f8-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="200f8-132">Значение пустую строку.</span><span class="sxs-lookup"><span data-stu-id="200f8-132">Empty string value.</span></span>
    
    <span data-ttu-id="200f8-133">**Второй элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="200f8-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="200f8-134">FieldType: Смещение 0x3A, 4 байта: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="200f8-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="200f8-135">FieldNameLength: Смещение 0x3E, два байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="200f8-136">FieldName: Смещение 0x40, массив из 0 символов.</span><span class="sxs-lookup"><span data-stu-id="200f8-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="200f8-137">Значение пустую строку.</span><span class="sxs-lookup"><span data-stu-id="200f8-137">Empty string value.</span></span>
      
    - <span data-ttu-id="200f8-138">Общие: Смещение 0x40.</span><span class="sxs-lookup"><span data-stu-id="200f8-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="200f8-139">PropSetGuid: Смещение 0x40, 16 байт: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="200f8-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="200f8-140">fcapm: смещение 0x50 4 байта: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="200f8-141">dwString: смещение 0x54 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-142">dwBitmap: смещение 0x58, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-143">dwDisplay: смещение 0x5C 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-144">iFmt: смещение 0x60 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-145">wszFormulaLength: смещение 0x64, два байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="200f8-146">wszFormula: смещение 0x66, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="200f8-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="200f8-147">Значение пустую строку.</span><span class="sxs-lookup"><span data-stu-id="200f8-147">Empty string value.</span></span>
    
- <span data-ttu-id="200f8-148">FolderUserFieldsUnicode: Смещение 0x66.</span><span class="sxs-lookup"><span data-stu-id="200f8-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="200f8-149">FieldDefinitionCount: Смещение 0x66, 4 байта: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="200f8-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="200f8-150">FieldDefinitions: Смещение 0x6A, массива 2 FolderFieldDefinitionW потоков.</span><span class="sxs-lookup"><span data-stu-id="200f8-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="200f8-151">**Первый элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="200f8-151">**First array element**:</span></span>
    
    - <span data-ttu-id="200f8-152">FieldType: Смещение 0x6A, 4 байта: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="200f8-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="200f8-153">FieldNameLength: Смещение 0x6E, два байта: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="200f8-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="200f8-154">FieldName: Смещение 0x70, массив 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="200f8-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="200f8-155">Значение строки Юникод: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="200f8-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="200f8-156">Общие: Смещение 0x84.</span><span class="sxs-lookup"><span data-stu-id="200f8-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="200f8-157">PropSetGuid: Смещение 0x84 16 байт: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="200f8-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="200f8-158">fcapm: смещение 0x94, 4 байта: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="200f8-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="200f8-159">dwString: смещение 0x98, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-160">dwBitmap: смещение 0x9C, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-161">dwDisplay: смещение устройства 0xA0, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-162">iFmt: смещение 0xA4, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-163">wszFormulaLength: смещение 0xA8, два байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="200f8-164">wszFormula: смещение 0xAA, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="200f8-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="200f8-165">Значение пустую строку.</span><span class="sxs-lookup"><span data-stu-id="200f8-165">Empty string value.</span></span>
    
    <span data-ttu-id="200f8-166">**Второй элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="200f8-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="200f8-167">FieldType: Смещение 0xAA, 4 байта: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="200f8-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="200f8-168">FieldNameLength: Смещение 0xAE, два байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="200f8-169">FieldName: Смещение 0xB0, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="200f8-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="200f8-170">Значение пустую строку.</span><span class="sxs-lookup"><span data-stu-id="200f8-170">Empty string value.</span></span>
      
    - <span data-ttu-id="200f8-171">Общие: Смещение 0xB0.</span><span class="sxs-lookup"><span data-stu-id="200f8-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="200f8-172">PropSetGuid: Смещение 0xB0 16 байт: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="200f8-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="200f8-173">fcapm: смещение 0xC0 4 байта: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="200f8-174">dwString: смещение 0xC4, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-175">dwBitmap: смещение 0xC8, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-176">dwDisplay: смещение 0xCC, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-177">iFmt: смещение 0xD0, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="200f8-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="200f8-178">wszFormulaLength: смещение 0xD4, два байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="200f8-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="200f8-179">wszFormula: смещение 0xD6, массив из 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="200f8-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="200f8-180">Значение пустую строку.</span><span class="sxs-lookup"><span data-stu-id="200f8-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="200f8-181">См. также</span><span class="sxs-lookup"><span data-stu-id="200f8-181">See also</span></span>

- [<span data-ttu-id="200f8-182">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="200f8-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="200f8-183">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="200f8-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="200f8-184">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="200f8-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="200f8-185">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="200f8-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="200f8-186">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="200f8-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="200f8-187">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="200f8-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="200f8-188">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="200f8-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

