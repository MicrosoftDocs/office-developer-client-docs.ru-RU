---
title: Пример FolderUserFields потока
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 76ad693b05e3989bd64ba66565ae4def22110ad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564901"
---
# <a name="folderuserfields-stream-sample"></a>Пример FolderUserFields потока

**Применимо к**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается пример FolderUserFields потока. Поток содержит определение того, пользовательские поля, `TextField1`. Тип — **текст**, а в потоке FolderUserFields содержит части FolderUserFieldsAnsi и FolderUserFieldsUnicode. Для получения дополнительных сведений см [Структуры папок поля потока](folder-fields-stream-structures.md).
  
## <a name="data-dump"></a>Дамп данных

Ниже приведен дамп данных потока как она будет отображаться в двоичном редакторе.
  
|Смещение потока|Байт данных|Данные в формате ASCII|
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
   

Ниже приведен синтаксического анализа образца данных для потока **FolderUserFields** :
  
- FolderUserFieldsAnsi: Смещения 0x0.
    
  - FieldDefinitionCount: Смещение 0x0, 4 байта: 0x00000002 (2).
    
  - FieldDefinitions: Смещение 0x4, массива 2 FolderFieldDefinitionA потоков.
    
    **Первый элемент массива**:
    
    - FieldType: Смещение 0x4, 4 байта: 0x00000001 (ftString).
      
    - FieldNameLength: Смещение 0x8, два байта: 0x000A (10)
      
    - FieldName: Смещение 0xA, массив 10 символов. Значение строки ANSI: «TextField1».
      
    - Общие: Смещение 0x14.
    
      - PropSetGuid: Смещение 0x14 16 байт: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: смещение 0x24 4 байта: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: смещение 0x28, 4 байта: 0x00000000.
        
      - dwBitmap: смещение 0x2C 4 байта: 0x00000000.
        
      - dwDisplay: смещение 0x30 4 байта: 0x00000000.
        
      - iFmt: смещение 0x34 4 байта: 0x00000000.
        
      - wszFormulaLength: смещение 0x38 два байта: 0x0000 (0).
        
      - wszFormula: смещение 0x3A, массив из 0 WCHARs. Значение пустую строку.
    
    **Второй элемент массива**:
    
    - FieldType: Смещение 0x3A, 4 байта: 0x00000000 (ftNone).
      
    - FieldNameLength: Смещение 0x3E, два байта: 0x0000 (0).
      
    - FieldName: Смещение 0x40, массив из 0 символов. Значение пустую строку.
      
    - Общие: Смещение 0x40.
    
      - PropSetGuid: Смещение 0x40, 16 байт: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: смещение 0x50 4 байта: 0x00000000 (0).
        
      - dwString: смещение 0x54 4 байта: 0x00000000.
        
      - dwBitmap: смещение 0x58, 4 байта: 0x00000000.
        
      - dwDisplay: смещение 0x5C 4 байта: 0x00000000.
        
      - iFmt: смещение 0x60 4 байта: 0x00000000.
        
      - wszFormulaLength: смещение 0x64, два байта: 0x0000 (0).
        
      - wszFormula: смещение 0x66, массив из 0 WCHARs. Значение пустую строку.
    
- FolderUserFieldsUnicode: Смещение 0x66.
    
  - FieldDefinitionCount: Смещение 0x66, 4 байта: 0x00000002 (2).
    
  - FieldDefinitions: Смещение 0x6A, массива 2 FolderFieldDefinitionW потоков.
    
    **Первый элемент массива**:
    
    - FieldType: Смещение 0x6A, 4 байта: 0x00000001 (ftString).
      
    - FieldNameLength: Смещение 0x6E, два байта: 0x000A (10).
      
    - FieldName: Смещение 0x70, массив 10 WCHARs. Значение строки Юникод: «TextField1».
      
    - Общие: Смещение 0x84.
    
      - PropSetGuid: Смещение 0x84 16 байт: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: смещение 0x94, 4 байта: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: смещение 0x98, 4 байта: 0x00000000.
        
      - dwBitmap: смещение 0x9C, 4 байта: 0x00000000.
        
      - dwDisplay: смещение устройства 0xA0, 4 байта: 0x00000000.
        
      - iFmt: смещение 0xA4, 4 байта: 0x00000000.
        
      - wszFormulaLength: смещение 0xA8, два байта: 0x0000 (0).
        
      - wszFormula: смещение 0xAA, массив из 0 WCHARs. Значение пустую строку.
    
    **Второй элемент массива**:
    
    - FieldType: Смещение 0xAA, 4 байта: 0x00000000 (ftNone).
      
    - FieldNameLength: Смещение 0xAE, два байта: 0x0000 (0).
      
    - FieldName: Смещение 0xB0, массив из 0 WCHARs. Значение пустую строку.
      
    - Общие: Смещение 0xB0.
    
      - PropSetGuid: Смещение 0xB0 16 байт: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: смещение 0xC0 4 байта: 0x00000000 (0).
        
      - dwString: смещение 0xC4, 4 байта: 0x00000000.
        
      - dwBitmap: смещение 0xC8, 4 байта: 0x00000000.
        
      - dwDisplay: смещение 0xCC, 4 байта: 0x00000000.
        
      - iFmt: смещение 0xD0, 4 байта: 0x00000000.
        
      - wszFormulaLength: смещение 0xD4, два байта: 0x0000 (0).
        
      - wszFormula: смещение 0xD6, массив из 0 WCHARs. Значение пустую строку.
    
## <a name="see-also"></a>См. также

- [Поля и элементы Outlook](outlook-items-and-fields.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
- [Структура потока SkipBlock](skipblock-stream-structure.md)
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

