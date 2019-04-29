---
title: Структура потока PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fc20c259f30ded2f96f3bf314e74207bebcac980
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422616"
---
# <a name="packedunicodestring-stream-structure"></a>Структура потока PackedUnicodeString

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Структура потока PackedUnicodeString содержит представление строки в кодировке Юникод (UTF-16). Эта строка не завершается символом NULL. Элементы данных в этом потоке хранятся в порядке байтов с прямым порядком байтов, сразу после друг друга в указанном ниже порядке. Фактические элементы данных, которые существуют, зависят от длины строки в представлении UTF – 16.
  
- Для строки, представление UTF – 16 которой содержит менее 255 Вчарс, элементы данных выглядят следующим образом:
    
  - Length: BYTE (1 байт), длина (в количестве Вчарс) представления строки в КОДИРОВКе UTF-16.
    
  - Символы: массив типа WCHAR. Количество этого массива равно элементу данных length. Данные в массиве являются представлением строки в КОДИРОВКе UTF-16.
    
- Для строки, в которой представление UTF – 16 содержит 255 в 65535 Вчарс, элементы данных выглядят следующим образом:
    
  - Префикс: BYTE (1 байт), значение 255 (0xFF).
    
  - Length: WORD (2 байта), длина (в количестве Вчарс) представления строки в КОДИРОВКе UTF-16.
    
  - Символы: массив типа WCHAR. Количество этого массива равно элементу данных length. Данные в массиве являются представлением строки в КОДИРОВКе UTF-16.
    
## <a name="see-also"></a>См. также



[Элементы и поля Outlook](outlook-items-and-fields.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)

