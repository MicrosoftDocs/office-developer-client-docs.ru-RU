---
title: Определение свойства потока образца
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc216302cb68be4b0e9d57f60f491adebcba1975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573931"
---
# <a name="propertydefinition-stream-sample"></a>Определение свойства потока образца

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается пример потока определение свойства. Поток содержит определение того, пользовательские поля, `TextField1`. Тип — **текст**, и определение находится в формате PropDefV2.
  
## <a name="data-dump"></a>Дамп данных

Ниже приведен дамп данных потока как она будет отображаться в двоичном редакторе.
  
|Смещение потока|Байт данных|Данные в формате ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Ниже приведен синтаксического анализа образца данных для потока определение свойства.
  
- Версия: Смещение 0x0, два байта: 0x0103 (PropDefV2).
    
- FieldDefinitionCount: Смещение 0x2, 4 байта: 0x1 (1).
    
- FieldDefinitions: Смещение 0x6 массив 1 FieldDefinition потока.
    
  - Флаги: Смещение 0x6 4 байта: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).
    
  - VT: Смещение 0xA два байта: 0x8 (**VT_BSTR**).
    
  - DispId: Смещение 0xC 4 байта: 0x0 (0).
    
  - NmidNameLength: Смещение 0x10, два байта: 0xA (10).
    
  - NmidName: Смещение 0x12, массив 10 WCHARs. Значение строки Юникод: «TextField1».
    
  - NameANSI: Смещение 0x26, PackedAnsiString потока.
    
    - Продолжительность: Смещение 0x26, 1 байт: 0xA (10).
      
    - Символов: Смещение 0x27, массив 10 символов. Значение строки ANSI: «TextField1».
    
  - FormulaANSI: Смещение 0x31 PackedAnsiString потока.
    
    - Продолжительность: Смещение 0x31, 1 байт: 0x0 (0).
      
    - Символов: Смещение 0x32, массив из 0 символов. Пустая строка ANSI.
    
  - ValidationRuleANSI: Смещение 0x32, PackedAnsiString потока.
    
    - Продолжительность: Смещение 0x32, 1 байт: 0x0 (0).
      
    - Символов: Смещение 0x33, массив из 0 символов. Пустая строка ANSI.
    
  - ValidationTextANSI: Смещение 0x33 PackedAnsiString потока.
    
    - Продолжительность: Смещение 0x33, 1 байт: 0x0 (0).
      
    - Символов: Смещение 0x34, массив из 0 символов. Пустая строка ANSI.
    
  - ErrorANSI: Смещение 0x34 PackedAnsiString потока.
    
    - Продолжительность: Смещение 0x34, 1 байт: 0x0 (0).
      
    - Символов: Смещение 0x35, массив из 0 символов. Пустая строка ANSI.
    
  - InternalType: Смещение 0x35 4 байта: 0x0 (iTypeString).
    
  - SkipBlocks: Смещение 0x39, серии SkipBlock потоков.
    
  - Первый SkipBlock
    
    - Размер: Смещение 0x39 4 байта: 0x15 (21).
      
    - Содержимое: Смещение 0x3D 21 байтовый массив. Это первого потока SkipBlock, поэтому этот массив содержит FirstSkipBlockContent потока.
      
      - FieldName: Смещение 0x3D, PackedUnicodeString потока.
        
        - Продолжительность: Смещение 0x3D, 1 байт: 0xA (10).
          
        - Символов: Смещение 0x3E, массив 10 WCHARs. Значение строки Юникод: «TextField1».
    
  - Второй SkipBlock
    
    - Размер: Смещение 0x52 4 байта: 0x0 (0). Это прерывающие поток SkipBlock.
    
## <a name="see-also"></a>См. также

- [Поля и элементы Outlook](outlook-items-and-fields.md)
- [Структуры потоков](stream-structures.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
- [Структура потока SkipBlock](skipblock-stream-structure.md)
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

