---
title: Структура потока PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404507"
---
# <a name="packedansistring-stream-structure"></a>Структура потока PackedAnsiString

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока PackedAnsiString содержит представление строки ANSI на основе страницы кода ANSI компьютера, на котором Outlook Microsoft. Эта строка не завершается null-символом. Элементы данных в этом потоке хранятся в порядке маленького byte, сразу же следуя друг за другом в порядке, перечисленном ниже. Фактические элементы данных, которые существуют, зависят от длины строки в представлении ANSI.
  
- Для строки, представление anSI которой содержит менее 255 bytes, элементы данных представлены следующим образом:
    
  - Длина: BYTE (1 byte), длина , в количестве bytes, представления ANSI строки.
    
  - Символы: массив CHAR. Количество этого массива равно элементу данных Length. Данные в массиве — это представление ANSI строки.
    
- Для строки, представление anSI которой содержит от 255 до 65535 bytes, элементы данных представлены следующим образом:
    
  - Префикс: BYTE (1 byte), значение 255 (0xff).
    
  - Длина: WORD (2 bytes), длина в количестве bytes, представления ANSI строки.
    
  - Символы: массив CHAR. Количество этого массива равно элементу данных Length. Данные в массиве — это представление ANSI строки.
    
## <a name="see-also"></a>См. также



[Outlook Элементы и поля](outlook-items-and-fields.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)

