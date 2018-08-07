---
title: Разработка XLL-файлов Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- надстройки - [excel 2007], разработка XLL-модулей - [Excel 2007], XLL-модулей - [Excel 2007], разработка
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807157"
---
# <a name="developing-excel-xlls"></a>Разработка XLL-файлов Excel

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Главной причиной для записи Microsoft Excel XLL-модулей и с помощью интерфейса API для C — Создание высокопроизводительных функций. Приложения высокопроизводительные функции — и, начиная с версии Excel 2007, возможность записи многопоточных интерфейсы мощные серверные ресурсы — сделать его важной частью возможностями расширения Excel. Производительность XLL-модулей для дальнейшей был улучшенные в Excel 2007 путем добавления новых типов данных и, наиболее важные, поддержку многопоточность.
  
Интерфейса API для C нет более высокого уровня функций быстрой разработки Microsoft Visual Basic для приложений (VBA), COM или Microsoft .NET Framework. Управление памятью — низкий уровень и поэтому размещает больше, ответственность за на разработчика. Многие функции Excel, предоставляемые посредством COM, делая их доступными через VBA и .NET Framework, не представленных C API-интерфейса.


- [Понятия, связанные с программированием для Excel](excel-programming-concepts.md)
  
- [Работа с библиотеками DLL](working-with-dlls.md)
  
- [Доступ к коду XLL в Excel](accessing-xll-code-in-excel.md)
  
- [Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [����� � Excel �� DLL ��� XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Создание XLL-файлов](creating-xlls.md)
  
- [Оценка имен и других выражений в формулах листов](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Многопоточность и управление памятью](multithreading-and-memory-management.md)
  
- [Асинхронные пользовательские функции](asynchronous-user-defined-functions.md)
  
- [Функции защиты кластеров](cluster-safe-functions.md)
  
- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
  
- [Отображение диалоговых окон из библиотеки DLL или XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Доступ к дескрипторам основного окна и экземпляра Excel](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Обратная совместимость](backward-compatibility.md)
  

