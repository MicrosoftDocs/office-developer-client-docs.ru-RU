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
# <a name="propertydefinition-stream-sample"></a>Пример потока PropertyDefinition

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается пример потока PropertyDefinition. Поток содержит определение пользовательского  `TextField1` поля. Типом является **Text,** а определение — в формате PropDefV2.
  
## <a name="data-dump"></a>Дамп данных

Ниже показан дамп данных потока, который будет отображаться в двоичном редакторе.
  
|Смещение потока|Данные вбайт|Данные ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Ниже приводится анализ примера данных для потока PropertyDefinition:
  
- Версия: смещение 0x0, 2 0x0103 (PropDefV2).
    
- FieldDefinitionCount: 0x2 смещения, 4 0x1 (1).
    
- FieldDefinitions: 0x6 смещения, массив 1 поток FieldDefinition.
    
  - Флаги: смещение 0x6, 4 0x45 (PDO_IS_CUSTOM| PDO_PRINT_SAVEAS| PDO_PRINT_SAVEAS_DEF).
    
  - VT: смещение 0xA, 2 0x8 (**VT_BSTR).**
    
  - DispId: смещение 0xC, 4 0x0 (0).
    
  - NmidNameLength: 0x10 смещения, 2 0xA (10).
    
  - NmidName: offset 0x12 массив из 10 WCHARs. Строковое значение Юникода: TextField1.
    
  - NameANSI: offset 0x26, поток PackedAnsiString.
    
    - Длина: смещение 0x26, 1 0xA (10).
      
    - Characters: Offset 0x27, array of 10 CHARs. Строковое значение ANSI: TextField1.
    
  - FormulaANSI: смещение 0x31, поток PackedAnsiString.
    
    - Длина: смещение 0x31, 1 0x0 (0).
      
    - Characters: Offset 0x32, array of 0 CHARs. Пустая строка ANSI.
    
  - ValidationRuleANSI: offset 0x32, поток PackedAnsiString.
    
    - Длина: смещение 0x32, 1 0x0 (0).
      
    - Characters: Offset 0x33, array of 0 CHARs. Пустая строка ANSI.
    
  - ValidationTextANSI: offset 0x33, поток PackedAnsiString.
    
    - Длина: смещение 0x33, 1 0x0 (0).
      
    - Characters: Offset 0x34, array of 0 CHARs. Пустая строка ANSI.
    
  - ErrorANSI: смещение 0x34, поток PackedAnsiString.
    
    - Длина: смещение 0x34, 1 0x0 (0).
      
    - Characters: Offset 0x35, array of 0 CHARs. Пустая строка ANSI.
    
  - InternalType: 0x35 смещения, 4 0x0 (iTypeString).
    
  - SkipBlocks: offset 0x39, ряд потоков SkipBlock.
    
  - First SkipBlock
    
    - Размер: смещение 0x39, 4 0x15 (21).
      
    - Content: Offset 0x3D, array of 21 bytes. Это первый поток SkipBlock, поэтому этот массив содержит поток FirstSkipBlockContent.
      
      - FieldName: offset 0x3D, PackedUnicodeString stream.
        
        - Длина: смещение 0x3D, 1 0xA (10).
          
        - Characters: Offset 0x3E, array of 10 WCHARs. Строковое значение Юникода: TextField1.
    
  - Second SkipBlock
    
    - Размер: смещение 0x52, 4 0x0 (0). Это завершающий поток SkipBlock.
    
## <a name="see-also"></a>См. также

- [Элементы и поля Outlook](outlook-items-and-fields.md)
- [Структуры потоков](stream-structures.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
- [Структура потока SkipBlock](skipblock-stream-structure.md)
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

