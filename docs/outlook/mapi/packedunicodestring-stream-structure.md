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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Структура потока PackedUnicodeString содержит представление строки Unicode (UTF-16). Эта строка не завершается null-символом. Элементы данных в этом потоке хранятся в порядке маленького byte, сразу же следуя друг за другом в порядке, перечисленном ниже. Фактические элементы данных, которые существуют, зависят от длины строки в представлении UTF-16.
  
- Для строки, представление которой UTF-16 содержит менее 255 WCHARs, элементы данных представлены следующим образом:
    
  - Длина: BYTE (1 байт), длина в количестве WCHARs представления строки UTF-16.
    
  - Символы: массив WCHAR. Количество этого массива равно элементу данных Length. Данные в массиве — это представление строки UTF-16.
    
- Для строки, представление которой UTF-16 содержит от 255 до 65535 WCHARs, элементы данных представлены следующим образом:
    
  - Префикс: BYTE (1 byte), значение 255 (0xff).
    
  - Длина: WORD (2 байта), длина в количестве WCHARs представления строки UTF-16.
    
  - Символы: массив WCHAR. Количество этого массива равно элементу данных Length. Данные в массиве — это представление строки UTF-16.
    
## <a name="see-also"></a>См. также



[Outlook Элементы и поля](outlook-items-and-fields.md)
  
[Структуры потока](stream-structures.md)
  
[Структура потока FieldDefinition](fielddefinition-stream-structure.md)

