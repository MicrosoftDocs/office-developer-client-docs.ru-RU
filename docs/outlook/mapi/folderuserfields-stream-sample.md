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
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="19487-103">Пример потока FolderUserFields</span><span class="sxs-lookup"><span data-stu-id="19487-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="19487-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19487-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19487-105">В этом разделе описывается пример потока FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="19487-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="19487-106">Поток содержит определение определяемого пользователем поля `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="19487-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="19487-107">Типом является **Text**, а поток FolderUserFields содержит как части фолдерусерфиелдсанси, так и фолдерусерфиелдсуникоде.</span><span class="sxs-lookup"><span data-stu-id="19487-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="19487-108">Дополнительные сведения см. [](folder-fields-stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="19487-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="19487-109">Дамп данных</span><span class="sxs-lookup"><span data-stu-id="19487-109">Data dump</span></span>

<span data-ttu-id="19487-110">Ниже приведен дамп данных потока, как он будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="19487-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="19487-111">Смещение потока</span><span class="sxs-lookup"><span data-stu-id="19487-111">Stream offset</span></span>|<span data-ttu-id="19487-112">Байты данных</span><span class="sxs-lookup"><span data-stu-id="19487-112">Data bytes</span></span>|<span data-ttu-id="19487-113">Данные ASCII</span><span class="sxs-lookup"><span data-stu-id="19487-113">ASCII data</span></span>|
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
   

<span data-ttu-id="19487-114">Ниже приведен пример синтаксического анализа данных для потока **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="19487-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="19487-115">Фолдерусерфиелдсанси: смещение 0x0.</span><span class="sxs-lookup"><span data-stu-id="19487-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="19487-116">Фиелддефинитионкаунт: offset 0x0, 4 байта: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="19487-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="19487-117">Фиелддефинитионс: offset 0x4, массив из 2 Фолдерфиелддефинитиона потоков.</span><span class="sxs-lookup"><span data-stu-id="19487-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="19487-118">**Первый элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="19487-118">**First array element**:</span></span>
    
    - <span data-ttu-id="19487-119">FieldType: offset 0x4, 4 байта: 0x00000001 (Фтстринг).</span><span class="sxs-lookup"><span data-stu-id="19487-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="19487-120">Фиелднамеленгс: offset 0x8, 2 байта: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="19487-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="19487-121">FieldName: offset 0xA, массив из 10 знаков.</span><span class="sxs-lookup"><span data-stu-id="19487-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="19487-122">Строковое значение ANSI: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="19487-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="19487-123">Common: offset 0x14.</span><span class="sxs-lookup"><span data-stu-id="19487-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="19487-124">Пропсетгуид: offset 0x14, 16 байт: {00020329-0000-0000-C000-000000000046} (ПС_ПУБЛИК_СТРИНГС).</span><span class="sxs-lookup"><span data-stu-id="19487-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="19487-125">фкапм: offset 0x24, 4 байта: 0x80000007 (ФКАПМ_КАН_ЕДИТ | ФКАПМ_КАН_СОРТ | ФКАПМ_КАН_ГРАУП | ФКАПМ_КАН_ЕДИТ_ИН_ИТЕМ).</span><span class="sxs-lookup"><span data-stu-id="19487-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="19487-126">Двстринг: offset 0x28, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-127">Двбитмап: offset 0x2C, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-128">Двдисплай: offset 0x30, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-129">Ифмт: offset 0x34, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-130">Всзформулаленгс: offset 0x38, 2 байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="19487-131">Всзформула: offset 0x3A, массив 0 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="19487-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="19487-132">Пустое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="19487-132">Empty string value.</span></span>
    
    <span data-ttu-id="19487-133">**Второй элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="19487-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="19487-134">FieldType: offset 0x3A, 4 байта: 0x00000000 (Фтноне).</span><span class="sxs-lookup"><span data-stu-id="19487-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="19487-135">Фиелднамеленгс: offset 0x3E, 2 байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="19487-136">FieldName: смещение 0x40, массив 0 знаков.</span><span class="sxs-lookup"><span data-stu-id="19487-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="19487-137">Пустое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="19487-137">Empty string value.</span></span>
      
    - <span data-ttu-id="19487-138">Общие: смещение 0x40.</span><span class="sxs-lookup"><span data-stu-id="19487-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="19487-139">Пропсетгуид: смещение 0x40, 16 байт: {00000000-0000-0000-0000-000000000000} (гуид_нулл).</span><span class="sxs-lookup"><span data-stu-id="19487-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="19487-140">фкапм: offset 0x50, 4 байта: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="19487-141">Двстринг: offset 0x54, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-142">Двбитмап: offset 0x58, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-143">Двдисплай: offset 0x5C, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-144">Ифмт: offset 0x60, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-145">Всзформулаленгс: offset 0x64, 2 байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="19487-146">Всзформула: offset 0x66, массив 0 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="19487-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="19487-147">Пустое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="19487-147">Empty string value.</span></span>
    
- <span data-ttu-id="19487-148">Фолдерусерфиелдсуникоде: offset 0x66.</span><span class="sxs-lookup"><span data-stu-id="19487-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="19487-149">Фиелддефинитионкаунт: offset 0x66, 4 байта: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="19487-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="19487-150">Фиелддефинитионс: offset 0x6A, массив из 2 Фолдерфиелддефинитионв потоков.</span><span class="sxs-lookup"><span data-stu-id="19487-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="19487-151">**Первый элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="19487-151">**First array element**:</span></span>
    
    - <span data-ttu-id="19487-152">FieldType: offset 0x6A, 4 байта: 0x00000001 (Фтстринг).</span><span class="sxs-lookup"><span data-stu-id="19487-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="19487-153">Фиелднамеленгс: offset 0x6E, 2 байта: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="19487-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="19487-154">FieldName: смещение 0x70, массив 10 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="19487-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="19487-155">Строковое значение Юникода: "TextField1".</span><span class="sxs-lookup"><span data-stu-id="19487-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="19487-156">Common: offset 0x84.</span><span class="sxs-lookup"><span data-stu-id="19487-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="19487-157">Пропсетгуид: offset 0x84, 16 байт: {00020329-0000-0000-C000-000000000046} (ПС_ПУБЛИК_СТРИНГС).</span><span class="sxs-lookup"><span data-stu-id="19487-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="19487-158">фкапм: offset 0x94, 4 байта: 0x80000007 (ФКАПМ_КАН_ЕДИТ | ФКАПМ_КАН_СОРТ | ФКАПМ_КАН_ГРАУП | ФКАПМ_КАН_ЕДИТ_ИН_ИТЕМ).</span><span class="sxs-lookup"><span data-stu-id="19487-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="19487-159">Двстринг: offset 0x98, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-160">Двбитмап: offset 0x9C, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-161">Двдисплай: offset 0xA0, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-162">Ифмт: offset 0xA4, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-163">Всзформулаленгс: offset 0xA8, 2 байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="19487-164">Всзформула: offset 0xAA, массив 0 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="19487-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="19487-165">Пустое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="19487-165">Empty string value.</span></span>
    
    <span data-ttu-id="19487-166">**Второй элемент массива**:</span><span class="sxs-lookup"><span data-stu-id="19487-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="19487-167">FieldType: offset 0xAA, 4 байта: 0x00000000 (Фтноне).</span><span class="sxs-lookup"><span data-stu-id="19487-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="19487-168">Фиелднамеленгс: offset 0xAE, 2 байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="19487-169">FieldName: смещение 0xB0, массив 0 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="19487-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="19487-170">Пустое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="19487-170">Empty string value.</span></span>
      
    - <span data-ttu-id="19487-171">Common: offset 0xB0.</span><span class="sxs-lookup"><span data-stu-id="19487-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="19487-172">Пропсетгуид: offset 0xB0, 16 байт: {00000000-0000-0000-0000-000000000000} (гуид_нулл).</span><span class="sxs-lookup"><span data-stu-id="19487-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="19487-173">фкапм: offset 0xC0, 4 байта: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="19487-174">Двстринг: offset 0xC4, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-175">Двбитмап: offset 0xC8, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-176">Двдисплай: offset 0xCC, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-177">Ифмт: offset 0xD0, 4 байта: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="19487-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="19487-178">Всзформулаленгс: offset 0xD4, 2 байта: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="19487-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="19487-179">Всзформула: offset 0xD6, массив 0 Вчарс.</span><span class="sxs-lookup"><span data-stu-id="19487-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="19487-180">Пустое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="19487-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19487-181">См. также</span><span class="sxs-lookup"><span data-stu-id="19487-181">See also</span></span>

- [<span data-ttu-id="19487-182">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="19487-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="19487-183">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="19487-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="19487-184">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="19487-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="19487-185">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="19487-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="19487-186">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="19487-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="19487-187">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="19487-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="19487-188">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="19487-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

