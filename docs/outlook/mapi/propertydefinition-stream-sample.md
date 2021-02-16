---
title: Пример потока PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406663"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="f1839-103">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1839-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="f1839-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1839-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1839-105">В этом разделе описывается пример потока PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1839-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="f1839-106">Поток содержит определение пользовательского  `TextField1` поля.</span><span class="sxs-lookup"><span data-stu-id="f1839-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="f1839-107">Типом является **Text,** а определение — в формате PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f1839-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="f1839-108">Дамп данных</span><span class="sxs-lookup"><span data-stu-id="f1839-108">Data dump</span></span>

<span data-ttu-id="f1839-109">Ниже показан дамп данных потока, который будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="f1839-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="f1839-110">Смещение потока</span><span class="sxs-lookup"><span data-stu-id="f1839-110">Stream offset</span></span>|<span data-ttu-id="f1839-111">Данные вбайт</span><span class="sxs-lookup"><span data-stu-id="f1839-111">Data bytes</span></span>|<span data-ttu-id="f1839-112">Данные ASCII</span><span class="sxs-lookup"><span data-stu-id="f1839-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="f1839-113">Ниже приводится анализ примера данных для потока PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="f1839-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="f1839-114">Версия: смещение 0x0, 2 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="f1839-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="f1839-115">FieldDefinitionCount: 0x2 смещения, 4 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="f1839-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="f1839-116">FieldDefinitions: 0x6 смещения, массив 1 поток FieldDefinition.</span><span class="sxs-lookup"><span data-stu-id="f1839-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="f1839-117">Флаги: смещение 0x6, 4 0x45 (PDO_IS_CUSTOM| PDO_PRINT_SAVEAS| PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="f1839-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="f1839-118">VT: смещение 0xA, 2 0x8 (**VT_BSTR).**</span><span class="sxs-lookup"><span data-stu-id="f1839-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="f1839-119">DispId: смещение 0xC, 4 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f1839-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="f1839-120">NmidNameLength: 0x10 смещения, 2 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f1839-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="f1839-121">NmidName: offset 0x12 массив из 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="f1839-122">Строковое значение Юникода: TextField1.</span><span class="sxs-lookup"><span data-stu-id="f1839-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f1839-123">NameANSI: offset 0x26, поток PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f1839-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f1839-124">Длина: смещение 0x26, 1 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f1839-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="f1839-125">Characters: Offset 0x27, array of 10 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="f1839-126">Строковое значение ANSI: TextField1.</span><span class="sxs-lookup"><span data-stu-id="f1839-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f1839-127">FormulaANSI: смещение 0x31, поток PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f1839-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f1839-128">Длина: смещение 0x31, 1 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f1839-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f1839-129">Characters: Offset 0x32, array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="f1839-130">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1839-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f1839-131">ValidationRuleANSI: offset 0x32, поток PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f1839-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f1839-132">Длина: смещение 0x32, 1 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f1839-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f1839-133">Characters: Offset 0x33, array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="f1839-134">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1839-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f1839-135">ValidationTextANSI: offset 0x33, поток PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f1839-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f1839-136">Длина: смещение 0x33, 1 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f1839-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f1839-137">Characters: Offset 0x34, array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="f1839-138">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1839-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f1839-139">ErrorANSI: смещение 0x34, поток PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f1839-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f1839-140">Длина: смещение 0x34, 1 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f1839-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f1839-141">Characters: Offset 0x35, array of 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="f1839-142">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="f1839-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f1839-143">InternalType: 0x35 смещения, 4 0x0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="f1839-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="f1839-144">SkipBlocks: offset 0x39, ряд потоков SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="f1839-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="f1839-145">First SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f1839-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="f1839-146">Размер: смещение 0x39, 4 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="f1839-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="f1839-147">Content: Offset 0x3D, array of 21 bytes.</span><span class="sxs-lookup"><span data-stu-id="f1839-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="f1839-148">Это первый поток SkipBlock, поэтому этот массив содержит поток FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="f1839-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="f1839-149">FieldName: offset 0x3D, PackedUnicodeString stream.</span><span class="sxs-lookup"><span data-stu-id="f1839-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="f1839-150">Длина: смещение 0x3D, 1 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f1839-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="f1839-151">Characters: Offset 0x3E, array of 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f1839-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="f1839-152">Строковое значение Юникода: TextField1.</span><span class="sxs-lookup"><span data-stu-id="f1839-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f1839-153">Second SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f1839-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="f1839-154">Размер: смещение 0x52, 4 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f1839-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="f1839-155">Это завершающий поток SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="f1839-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1839-156">См. также</span><span class="sxs-lookup"><span data-stu-id="f1839-156">See also</span></span>

- [<span data-ttu-id="f1839-157">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="f1839-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="f1839-158">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="f1839-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="f1839-159">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f1839-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="f1839-160">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="f1839-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="f1839-161">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f1839-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="f1839-162">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="f1839-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="f1839-163">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="f1839-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="f1839-164">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="f1839-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

