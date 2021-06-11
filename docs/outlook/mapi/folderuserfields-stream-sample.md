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
# <a name="folderuserfields-stream-sample"></a>Пример потока folderUserFields

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается пример потока FolderUserFields. Поток содержит определение поля, определяемого пользователем,  `TextField1` . Тип — **Текст,** а поток FolderUserFields содержит как части FolderUserFieldsAnsi, так и folderUserFieldsUnicode. Дополнительные сведения см. [в рубке Folder Fields Stream Structures.](folder-fields-stream-structures.md)
  
## <a name="data-dump"></a>Сброс данных

Ниже приводится сброс данных потока, который будет отображаться в двоичном редакторе.
  
|Смещение потока|Bytes data|Данные ASCII|
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
   

Ниже приводится анализ примерных данных для потока **FolderUserFields:**
  
- FolderUserFieldsAnsi: смещение 0x0.
    
  - FieldDefinitionCount: смещение 0x0, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: Смещение 0x4, массив из 2 потоков FolderFieldDefinitionA.
    
    **Первый элемент массива:**
    
    - FieldType: смещение 0x4, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: смещение 0x8, 2 bytes: 0x000A (10)
      
    - Имя поля: смещение 0xA, массив из 10 ОКР. Строковое значение ANSI: "TextField1".
      
    - Общие: смещение 0x14.
    
      - PropSetGuid: Смещение 0x14, 16 bytes: {00020329-0000-0000-00000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: Смещение 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString. Смещение 0x28, 4 bytes: 0x00000000.
        
      - dwBitmap. Смещение 0x2C, 4 bytes: 0x00000000.
        
      - dwDisplay: Смещение 0x30, 4 bytes: 0x00000000.
        
      - iFmt. Смещение 0x34, 4 bytes: 0x00000000.
        
      - wszFormulaLength: смещение 0x38, 2 bytes: 0x0000 (0).
        
      - wszFormula: смещение 0x3A, массив 0 WCHARs. Пустое значение строки.
    
    **Второй элемент массива:**
    
    - FieldType: смещение 0x3A, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: Смещение 0x3E, 2 bytes: 0x0000 (0).
      
    - Имя поля: смещение 0x40, массив из 0 ОКР. Пустое значение строки.
      
    - Общие: смещение 0x40.
    
      - PropSetGuid: Смещение 0x40, 16 {00000000-0000-0000-0000-000000000000} bytes: (GUID_NULL).
        
      - fcapm. Смещение 0x50, 4 bytes: 0x00000000 (0).
        
      - dwString: Смещение 0x54, 4 bytes: 0x00000000.
        
      - dwBitmap. Смещение 0x58, 4 bytes: 0x00000000.
        
      - dwDisplay: смещение 0x5C, 4 bytes: 0x00000000.
        
      - iFmt. Смещение 0x60, 4 bytes: 0x00000000.
        
      - wszFormulaLength: смещение 0x64, 2 bytes: 0x0000 (0).
        
      - wszFormula: смещение 0x66, массив 0 WCHARs. Пустое значение строки.
    
- FolderUserFieldsUnicode: Смещение 0x66.
    
  - FieldDefinitionCount: смещение 0x66, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: Смещение 0x6A, массив из 2 потоков FolderFieldDefinitionW.
    
    **Первый элемент массива:**
    
    - FieldType: смещение 0x6A, 4 bytes: 0x00000001 (ftString).
      
    - FieldNameLength: Смещение 0x6E, 2 bytes: 0x000A (10).
      
    - Имя поля: смещение 0x70, массив из 10 WCHARs. Значение строки Unicode: "TextField1".
      
    - Общие: смещение 0x84.
    
      - PropSetGuid: смещение 0x84, 16 bytes: {00020329-0000-0000-00000000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm. Смещение 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: смещение 0x98, 4 bytes: 0x00000000.
        
      - dwBitmap. Смещение 0x9C, 4 bytes: 0x00000000.
        
      - dwDisplay. Смещение 0xA0, 4 bytes: 0x00000000.
        
      - iFmt. Смещение 0xA4, 4 bytes: 0x00000000.
        
      - wszFormulaLength: смещение 0xA8, 2 bytes: 0x0000 (0).
        
      - wszFormula: смещение 0xAA, массив 0 WCHARs. Пустое значение строки.
    
    **Второй элемент массива:**
    
    - FieldType: смещение 0xAA, 4 bytes: 0x00000000 (ftNone).
      
    - FieldNameLength: смещение 0xAE, 2 bytes: 0x0000 (0).
      
    - Имя поля: смещение 0xB0, массив 0 WCHARs. Пустое значение строки.
      
    - Общие: смещение 0xB0.
    
      - PropSetGuid: Смещение 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm. Смещение 0xC0, 4 bytes: 0x00000000 (0).
        
      - dwString. Смещение 0xC4, 4 bytes: 0x00000000.
        
      - dwBitmap. Смещение 0xC8, 4 bytes: 0x00000000.
        
      - dwDisplay: смещение 0xCC, 4 bytes: 0x00000000.
        
      - iFmt. Смещение 0xD0, 4 bytes: 0x00000000.
        
      - wszFormulaLength: смещение 0xD4, 2 bytes: 0x0000 (0).
        
      - wszFormula: смещение 0xD6, массив 0 WCHARs. Пустое значение строки.
    
## <a name="see-also"></a>См. также

- [Outlook Элементы и поля](outlook-items-and-fields.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
- [Структура skipBlock Stream](skipblock-stream-structure.md)
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

