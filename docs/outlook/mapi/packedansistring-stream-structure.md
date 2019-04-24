---
title: Структура потока PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348512"
---
# <a name="packedansistring-stream-structure"></a>Структура потока PackedAnsiString

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока PackedAnsiString содержит представление строки в КОДИРОВКе ANSI на основе кодовой страницы ANSI компьютера, на котором работает Microsoft Outlook. Эта строка не завершается символом NULL. Элементы данных в этом потоке хранятся в порядке байтов с прямым порядком байтов, сразу после друг друга в указанном ниже порядке. Фактические элементы данных, которые существуют, зависят от длины строки в представлении ANSI.
  
- Для строки, в которой представление ANSI содержит менее 255 байт, используются следующие элементы данных:
    
  - Length: BYTE (1 байт), длина (в байтах) представления строки в формате ANSI.
    
  - Символы: массив CHAR. Количество этого массива равно элементу данных length. Данные в массиве являются представлением строки в формате ANSI.
    
- Для строки, в которой представление ANSI содержит 255 – 65535 байт, элементы данных выглядят следующим образом:
    
  - Префикс: BYTE (1 байт), значение 255 (0xFF).
    
  - Length: WORD (2 байта), длина (в байтах) представления строки в формате ANSI.
    
  - Символы: массив CHAR. Количество этого массива равно элементу данных length. Данные в массиве являются представлением строки в формате ANSI.
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)

