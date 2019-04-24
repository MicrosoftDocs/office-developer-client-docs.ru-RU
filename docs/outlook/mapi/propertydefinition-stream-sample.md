---
title: Пример потока PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328506"
---
# <a name="propertydefinition-stream-sample"></a>Пример потока PropertyDefinition

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается пример потока PropertyDefinition. Поток содержит определение определяемого пользователем поля `TextField1`. Тип — **текст**, а определение — в формате PropDefV2.
  
## <a name="data-dump"></a>Дамп данных

Ниже приведен дамп данных потока, как он будет отображаться в двоичном редакторе.
  
|Смещение потока|Байты данных|Данные ASCII|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
Ниже приведен пример синтаксического анализа данных для потока PropertyDefinition:
  
- Версия: смещение 0x0, 2 байта: 0x0103 (PropDefV2).
    
- Фиелддефинитионкаунт: смещение 0x2, 4 байта: 0x1 (1).
    
- Фиелддефинитионс: offset 0x6, массив из 1 FieldDefinition Stream.
    
  - Flags: offset 0x6, 4 байта: 0x45 (ПДО_ИС_КУСТОМ | ПДО_ПРИНТ_САВЕАС | ПДО_ПРИНТ_САВЕАС_ДЕФ).
    
  - VT: offset 0xA, 2 байта: 0x8 (**вт_бстр**).
    
  - DISPID: offset 0xC, 4 байта: 0x0 (0).
    
  - Нмиднамеленгс: offset 0x10, 2 байта: 0xA (10).
    
  - Нмиднаме: offset 0x12, массив из 10 Вчарс. Строковое значение Юникода: "TextField1".
    
  - Намеанси: offset 0x26, PackedAnsiString Stream.
    
    - Length: offset 0x26, 1 байт: 0xA (10).
      
    - Символы: offset 0x27, массив из 10 знаков. Строковое значение ANSI: "TextField1".
    
  - Формулаанси: offset 0x31, PackedAnsiString Stream.
    
    - Length: offset 0x31, 1 байт: 0x0 (0).
      
    - Символы: offset 0x32, массив 0 знаков. Пустая строка ANSI.
    
  - Валидатионрулеанси: смещение 0x32, PackedAnsiString Stream.
    
    - Length: смещение 0x32, 1 байт: 0x0 (0).
      
    - Символы: offset 0x33, массив 0 знаков. Пустая строка ANSI.
    
  - Валидатионтекстанси: offset 0x33, PackedAnsiString Stream.
    
    - Length: offset 0x33, 1 байт: 0x0 (0).
      
    - Символы: offset 0x34, массив 0 знаков. Пустая строка ANSI.
    
  - Ерроранси: offset 0x34, PackedAnsiString Stream.
    
    - Length: offset 0x34, 1 байт: 0x0 (0).
      
    - Символы: offset 0x35, массив 0 знаков. Пустая строка ANSI.
    
  - Интерналтипе: offset 0x35, 4 байта: 0x0 (Итипестринг).
    
  - Скипблоккс: offset 0x39, ряд SkipBlock потоков.
    
  - Первая SkipBlock
    
    - Size: offset 0x39, 4 байта: 0x15 (21).
      
    - Content: offset 0x3D, массив из 21 байт. Это первый поток SkipBlock, поэтому этот массив содержит поток FirstSkipBlockContent.
      
      - FieldName: offset 0x3D, PackedUnicodeString Stream.
        
        - Length: offset 0x3D, 1 байт: 0xA (10).
          
        - Символы: offset 0x3E, Array из 10 Вчарс. Строковое значение Юникода: "TextField1".
    
  - Вторая SkipBlock
    
    - Size: offset 0x52, 4 байта: 0x0 (0). Это завершающий поток SkipBlock.
    
## <a name="see-also"></a>См. также

- [Элементы и поля Outlook](outlook-items-and-fields.md)
- [Структуры потока](stream-structures.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
- [Структура потока SkipBlock](skipblock-stream-structure.md)
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

