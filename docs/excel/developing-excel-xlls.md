---
title: Разработка XLL-файлов Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- надстройки — [excel 2007], разработка XLL-файлов — [Excel 2007], XLL-файлы — [Excel 2007], разработка
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701097"
---
# <a name="developing-excel-xlls"></a>Разработка XLL-файлов Excel

**Область применения**: Excel 2013 | Office 2013 | Visual Studio 
  
Основная цель написания XLL-файлов Microsoft Excel и использования API C — создание высокопроизводительных функций. Применения высокопроизводительных функций — и, начиная с Excel 2007, возможность писать многопоточные интерфейсы для мощных серверных ресурсов — делают их очень важной частью расширения Excel. Производительность XLL-файлов была повышена в Excel 2007 путем добавления новых типов данных и, что самое важное, поддержки многопоточности.
  
В API C нет высокоуровневых функций быстрой разработки на Microsoft Visual Basic для приложений (VBA), COM или Microsoft .NET Framework. Управление памятью осуществляется на низком уровне, и поэтому возлагает большую ответственность на разработчика. Многие функции Excel, предоставляемые через COM (что делает их доступными через VBA и .NET Framework), недоступны интерфейсу API C.


- [Понятия, связанные с программированием для Excel](excel-programming-concepts.md)
  
- [Работа с библиотеками DLL](working-with-dlls.md)
  
- [Доступ к коду XLL в Excel](accessing-xll-code-in-excel.md)
  
- [Вызов функций XLL из диалоговых окон "Мастер функций" и "Замена"](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [Вызов Excel из библиотеки DLL или XLL](calling-into-excel-from-the-dll-or-xll.md)
  
- [Создание XLL-файлов](creating-xlls.md)
  
- [Оценка имен и других выражений в формулах листов](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [Многопоточность и управление памятью](multithreading-and-memory-management.md)
  
- [Асинхронные пользовательские функции](asynchronous-user-defined-functions.md)
  
- [Функции защиты кластеров](cluster-safe-functions.md)
  
- [Разрешение прерывания длительных операций пользователем](permitting-user-breaks-in-lengthy-operations.md)
  
- [Отображение диалоговых окон из библиотеки DLL или XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [Доступ к дескрипторам основного окна и экземпляра Excel](how-to-access-excel-instance-and-main-window-handles.md)
  
- [Обратная совместимость](backward-compatibility.md)
  

