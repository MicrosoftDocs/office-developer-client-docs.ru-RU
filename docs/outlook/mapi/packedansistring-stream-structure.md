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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Структура потока PackedAnsiString содержит представление строки ANSI на основе кодовой страницы ANSI компьютера, на котором запущен Microsoft Outlook. Эта строка не завершается символом NULL. Элементы данных в этом потоке хранятся в порядке с небольшим набором элементов, сразу же после друг друга в порядке, приведенном ниже. Фактические элементы данных зависят от длины строки в представлении ANSI.
  
- Для строки, представление ANSI которой содержит менее 255 bytes, элементы данных:
    
  - Length: BYTE (1 byte), the length, in number of bytes, of the ANSI representation of the string.
    
  - Characters: An array of CHAR. Количество массивов равно элементу данных Length. Данные в массиве — это anSI-представление строки.
    
- Для строки, представление ANSI которой содержит от 255 до 65535 элементов данных:
    
  - Префикс: BYTE (1 byte), значение 255 (0xff).
    
  - Длина: WORD (2 bytes), длина строки ANSI (в количестве в количествах).
    
  - Characters: An array of CHAR. Количество массивов равно элементу данных Length. Данные в массиве — это anSI-представление строки.
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Структуры потоков](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)

