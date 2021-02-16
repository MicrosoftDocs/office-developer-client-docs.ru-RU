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
# <a name="folderuserfields-stream-sample"></a>Пример потока FolderUserFields

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе описывается пример потока FolderUserFields. Поток содержит определение пользовательского  `TextField1` поля. Типом является **Text,** а поток FolderUserFields содержит части FolderUserFieldsAnsi и FolderUserFieldsUnicode. Дополнительные сведения см. в [подстроках потока полей папок.](folder-fields-stream-structures.md)
  
## <a name="data-dump"></a>Дамп данных

Ниже показан дамп данных потока, который будет отображаться в двоичном редакторе.
  
|Смещение потока|Данные вбайт|Данные ASCII|
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
   

Ниже приводится анализ примеров данных для потока **FolderUserFields:**
  
- FolderUserFieldsAnsi: смещение 0x0.
    
  - FieldDefinitionCount: 0x0 смещения, 4 0x00000002 (2).
    
  - FieldDefinitions: 0x4 смещения, массив из 2 потоков FolderFieldDefinitionA.
    
    **Первый элемент массива:**
    
    - FieldType: смещение 0x4, 4 0x00000001 (ftString).
      
    - FieldNameLength: 0x8 смещения, 2 0x000A (10)
      
    - FieldName: 0xA offset, массив из 10 chars. Строковое значение ANSI: TextField1.
      
    - Common: Offset 0x14.
    
      - PropSetGuid: offset 0x14, 16 bytes: {00020329-0000-0000-C000-00000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: смещение 0x24, 4 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: смещение 0x28, 4 0x00000000.
        
      - dwBitmap: смещение 0x2C, 4 0x00000000.
        
      - dwDisplay: смещение 0x30, 4 0x00000000.
        
      - iFmt: смещение 0x34, 4 0x00000000.
        
      - wszFormulaLength: 0x38 смещения, 2 0x0000 (0).
        
      - wszFormula: 0x3A смещения, массив из 0 WCHARs. Пустое строко значение.
    
    **Второй элемент массива:**
    
    - FieldType: 0x3A смещения, 4 0x00000000 (ftNone).
      
    - FieldNameLength: 0x3E смещения, 2 0x0000 (0).
      
    - FieldName: offset 0x40, массив 0 CHARs. Пустое строко значение.
      
    - Common: Offset 0x40.
    
      - PropSetGuid: смещение 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: смещение 0x50, 4 0x00000000 (0).
        
      - dwString: смещение 0x54, 4 0x00000000.
        
      - dwBitmap: смещение 0x58, 4 0x00000000.
        
      - dwDisplay: смещение 0x5C, 4 0x00000000.
        
      - iFmt: смещение 0x60, 4 0x00000000.
        
      - wszFormulaLength: 0x64 смещения, 2 0x0000 (0).
        
      - wszFormula: 0x66 смещения, массив из 0 WCHARs. Пустое строко значение.
    
- FolderUserFieldsUnicode: offset 0x66.
    
  - FieldDefinitionCount: offset 0x66, 4 bytes: 0x00000002 (2).
    
  - FieldDefinitions: 0x6A offset, массив из 2 потоков FolderFieldDefinitionW.
    
    **Первый элемент массива:**
    
    - FieldType: 0x6A смещения, 4 0x00000001 (ftString).
      
    - FieldNameLength: 0x6E смещения, 2 0x000A (10).
      
    - FieldName: 0x70, массив из 10 WCHARs. Строковое значение Юникода: TextField1.
      
    - Common: Offset 0x84.
    
      - PropSetGuid: offset 0x84, 16 bytes: {00020329-0000-0000-C000-00000000046} (PS_PUBLIC_STRINGS).
        
      - fcapm: смещение 0x94, 4 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP| FCAPM_CAN_EDIT_IN_ITEM).
        
      - dwString: смещение 0x98, 4 0x00000000.
        
      - dwBitmap: смещение 0x9C, 4 0x00000000.
        
      - dwDisplay: смещение 0xA0, 4 0x00000000.
        
      - iFmt: смещение 0xA4, 4 0x00000000.
        
      - wszFormulaLength: 0xA8 смещения, 2 0x0000 (0).
        
      - wszFormula: 0xAA смещения, массив из 0 WCHARs. Пустое строко значение.
    
    **Второй элемент массива:**
    
    - FieldType: 0xAA смещения, 4 0x00000000 (ftNone).
      
    - FieldNameLength: 0xAE смещения, 2 0x0000 (0).
      
    - FieldName: offset 0xB0, массив 0 WCHARs. Пустое строко значение.
      
    - Common: Offset 0xB0.
    
      - PropSetGuid: offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).
        
      - fcapm: смещение 0xC0, 4 0x00000000 (0).
        
      - dwString: смещение 0xC4, 4 0x00000000.
        
      - dwBitmap: смещение 0xC8, 4 0x00000000.
        
      - dwDisplay: смещение 0xCC, 4 0x00000000.
        
      - iFmt: смещение 0xD0, 4 0x00000000.
        
      - wszFormulaLength: 0xD4 смещения, 2 0x0000 (0).
        
      - wszFormula: 0xD6 смещения, массив из 0 WCHARs. Пустое строко значение.
    
## <a name="see-also"></a>См. также

- [Элементы и поля Outlook](outlook-items-and-fields.md)
- [Структура потока PropertyDefinition](propertydefinition-stream-structure.md)
- [Структура потока FieldDefinition](fielddefinition-stream-structure.md)
- [Структура потока SkipBlock](skipblock-stream-structure.md)
- [Структура потока FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)
- [Структура потока PackedAnsiString](packedansistring-stream-structure.md)
- [Структура потока PackedUnicodeString](packedunicodestring-stream-structure.md)

