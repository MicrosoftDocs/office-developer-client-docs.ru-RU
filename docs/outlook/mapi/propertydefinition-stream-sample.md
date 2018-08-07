---
title: Определение свойства потока образца
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812083"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="8cd17-103">Определение свойства потока образца</span><span class="sxs-lookup"><span data-stu-id="8cd17-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="8cd17-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8cd17-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8cd17-105">В этом разделе описывается пример потока определение свойства.</span><span class="sxs-lookup"><span data-stu-id="8cd17-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="8cd17-106">Поток содержит определение того, пользовательские поля, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="8cd17-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="8cd17-107">Тип — **текст**, и определение находится в формате PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="8cd17-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="8cd17-108">Дамп данных</span><span class="sxs-lookup"><span data-stu-id="8cd17-108">Data dump</span></span>

<span data-ttu-id="8cd17-109">Ниже приведен дамп данных потока как она будет отображаться в двоичном редакторе.</span><span class="sxs-lookup"><span data-stu-id="8cd17-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="8cd17-110">Смещение потока</span><span class="sxs-lookup"><span data-stu-id="8cd17-110">Stream offset</span></span>|<span data-ttu-id="8cd17-111">Байт данных</span><span class="sxs-lookup"><span data-stu-id="8cd17-111">Data bytes</span></span>|<span data-ttu-id="8cd17-112">Данные в формате ASCII</span><span class="sxs-lookup"><span data-stu-id="8cd17-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="8cd17-113">Ниже приведен синтаксического анализа образца данных для потока определение свойства.</span><span class="sxs-lookup"><span data-stu-id="8cd17-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="8cd17-114">Версия: Смещение 0x0, два байта: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="8cd17-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="8cd17-115">FieldDefinitionCount: Смещение 0x2, 4 байта: 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="8cd17-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="8cd17-116">FieldDefinitions: Смещение 0x6 массив 1 FieldDefinition потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="8cd17-117">Флаги: Смещение 0x6 4 байта: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="8cd17-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="8cd17-118">VT: Смещение 0xA два байта: 0x8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="8cd17-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="8cd17-119">DispId: Смещение 0xC 4 байта: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="8cd17-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="8cd17-120">NmidNameLength: Смещение 0x10, два байта: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="8cd17-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="8cd17-121">NmidName: Смещение 0x12, массив 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="8cd17-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="8cd17-122">Значение строки Юникод: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="8cd17-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="8cd17-123">NameANSI: Смещение 0x26, PackedAnsiString потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="8cd17-124">Продолжительность: Смещение 0x26, 1 байт: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="8cd17-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="8cd17-125">Символов: Смещение 0x27, массив 10 символов.</span><span class="sxs-lookup"><span data-stu-id="8cd17-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="8cd17-126">Значение строки ANSI: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="8cd17-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="8cd17-127">FormulaANSI: Смещение 0x31 PackedAnsiString потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="8cd17-128">Продолжительность: Смещение 0x31, 1 байт: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="8cd17-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="8cd17-129">Символов: Смещение 0x32, массив из 0 символов.</span><span class="sxs-lookup"><span data-stu-id="8cd17-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="8cd17-130">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="8cd17-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="8cd17-131">ValidationRuleANSI: Смещение 0x32, PackedAnsiString потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="8cd17-132">Продолжительность: Смещение 0x32, 1 байт: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="8cd17-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="8cd17-133">Символов: Смещение 0x33, массив из 0 символов.</span><span class="sxs-lookup"><span data-stu-id="8cd17-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="8cd17-134">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="8cd17-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="8cd17-135">ValidationTextANSI: Смещение 0x33 PackedAnsiString потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="8cd17-136">Продолжительность: Смещение 0x33, 1 байт: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="8cd17-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="8cd17-137">Символов: Смещение 0x34, массив из 0 символов.</span><span class="sxs-lookup"><span data-stu-id="8cd17-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="8cd17-138">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="8cd17-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="8cd17-139">ErrorANSI: Смещение 0x34 PackedAnsiString потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="8cd17-140">Продолжительность: Смещение 0x34, 1 байт: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="8cd17-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="8cd17-141">Символов: Смещение 0x35, массив из 0 символов.</span><span class="sxs-lookup"><span data-stu-id="8cd17-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="8cd17-142">Пустая строка ANSI.</span><span class="sxs-lookup"><span data-stu-id="8cd17-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="8cd17-143">InternalType: Смещение 0x35 4 байта: 0x0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="8cd17-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="8cd17-144">SkipBlocks: Смещение 0x39, серии SkipBlock потоков.</span><span class="sxs-lookup"><span data-stu-id="8cd17-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="8cd17-145">Первый SkipBlock</span><span class="sxs-lookup"><span data-stu-id="8cd17-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="8cd17-146">Размер: Смещение 0x39 4 байта: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="8cd17-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="8cd17-147">Содержимое: Смещение 0x3D 21 байтовый массив.</span><span class="sxs-lookup"><span data-stu-id="8cd17-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="8cd17-148">Это первого потока SkipBlock, поэтому этот массив содержит FirstSkipBlockContent потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="8cd17-149">FieldName: Смещение 0x3D, PackedUnicodeString потока.</span><span class="sxs-lookup"><span data-stu-id="8cd17-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="8cd17-150">Продолжительность: Смещение 0x3D, 1 байт: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="8cd17-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="8cd17-151">Символов: Смещение 0x3E, массив 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="8cd17-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="8cd17-152">Значение строки Юникод: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="8cd17-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="8cd17-153">Второй SkipBlock</span><span class="sxs-lookup"><span data-stu-id="8cd17-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="8cd17-154">Размер: Смещение 0x52 4 байта: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="8cd17-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="8cd17-155">Это прерывающие поток SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="8cd17-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cd17-156">См. также</span><span class="sxs-lookup"><span data-stu-id="8cd17-156">See also</span></span>

- [<span data-ttu-id="8cd17-157">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="8cd17-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="8cd17-158">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="8cd17-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="8cd17-159">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="8cd17-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="8cd17-160">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="8cd17-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="8cd17-161">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="8cd17-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="8cd17-162">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="8cd17-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="8cd17-163">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="8cd17-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="8cd17-164">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="8cd17-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

