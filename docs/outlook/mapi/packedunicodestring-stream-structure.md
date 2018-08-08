---
title: Структура потока PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810087"
---
# <a name="packedunicodestring-stream-structure"></a>Структура потока PackedUnicodeString

  
  
**Относится к**: Outlook 
  
Структура потока PackedUnicodeString содержит представление Юникод (UTF-16) строки. Эта строка не будет завершен символом null. Элементы данных в этот поток хранятся в прямом байтовом, сразу после друг с другом в указанном ниже порядке. Фактические данные элементы, которые существуют зависят от длина строки в представление UTF-16.
  
- Поиск строки, представление UTF-16 содержит меньше, чем 255 WCHARs элементы данных, следующим образом:
    
  - Продолжительность: БАЙТА (1 байт), длины, в число WCHARs, UTF-16-представления строки.
    
  - Символы: Массив WCHAR. Число этого массива равно элемент данных длины. Данные в массиве — это представление UTF-16 строки.
    
- Поиск строки, представление UTF-16 содержит WCHARs 255 до 65535 элементы данных, следующим образом:
    
  - Префикс: БАЙТА (1 байт), значение 255 (0xff).
    
  - Продолжительность: WORD (2 байта), длины, в число WCHARs, UTF-16-представления строки.
    
  - Символы: Массив WCHAR. Число этого массива равно элемент данных длины. Данные в массиве — это представление UTF-16 строки.
    
## <a name="see-also"></a>См. также



[Поля и элементы Outlook](outlook-items-and-fields.md)
  
[Структуры потоков](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)

