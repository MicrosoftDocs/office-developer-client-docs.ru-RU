---
title: Ссылки на таблицы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- ссылки [Excel 2007], таблицы, ссылки на листа [Excel 2007], ссылки на внешние таблицы [Excel 2007], активный листа [Excel 2007], текущий листа [Excel 2007], ссылки на внутренние таблицы [Excel 2007]
localization_priority: Normal
ms.assetid: 53406fb8-4ca5-4204-a6ad-b21ca9e6a100
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2944f73a3144837a4be8aff7c7fed9a8d2158203
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416463"
---
# <a name="worksheet-references"></a>Ссылки на таблицы

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Ссылка в Microsoft Excel — это тип данных, который ссылается на прямоугольный блок ячеек (который может быть только одной ячейкой), или в некоторых случаях несколько разроных блоков ячеек. Внутри Excel используется один тип ссылок для ячеек на текущем листе, известный как внутренняя ссылка. Любая ячейка, не на текущем листе, описывается другим типом ссылки, известной как внешняя ссылка. В следующем разделе см. определение активного и текущего.
  
## <a name="active-vs-current"></a>Active vs. Current

В Excel термин active относится к просмотру пользователя. Активная книга и таблица — это те книги, которые пользователь в настоящее время ищет или, если Excel потерял фокус на другое приложение, смотрел, когда Excel последний раз был фокус. Активный лист всегда находится в активной книге. Одна или несколько ячеек, выбранных в активном листе, называются активными ячейками. Если встроенный объект имеет фокус, последние выбранные ячейки по-прежнему активны. 
  
Текущий термин относится к Excel пересчета. Текущая книга и таблица — это те, которые в настоящее время пересчитываются. Текущий лист всегда находится в текущей книге. Пересчитаемая ячейка называется текущей ячейкой или в случае пересчета формулы массива текущими ячейками. 
  
Важные моменты, которые следует помнить:
  
- Активная книга/таблица/ячейка обычно не является текущей, хотя она может быть.
    
- Функция надстройки, будь то в модуле Visual Basic для приложений (VBA) или DLL или XLL, всегда вызвана из текущей ячейки на текущем листе или одна из них в случае многоуровневого пересчета (MTR).
    
Многие Excel, которые предоставляют сведения о ячейке, диапазоне ячеек или листе в книге, различают активную книгу, лист или ячейку и текущую книгу, лист или ячейку. Это различие отражается в типах данных, используемых для описания ссылок на блоки ячеек, как описано в следующем разделе.
  
## <a name="internal-and-external-worksheet-references"></a>Ссылки на внутренние и внешние таблицы

Главное различие между внутренними и внешними ссылками состоит в том, что внешний тип справочных данных содержит ID для таблицы, а также описание, на которые ссылаются ячейки. Внутренняя ссылка не содержит ссылки на лист, неявно подразумевается, что лист является текущим листом. 
  
Многие функции API C возвращают ссылки или принимают справочные аргументы. Любая функция API C, которая принимает справочные аргументы, принимает внутренние или внешние ссылки, за исключением **функции xlSheetNm,** которая требует внешней ссылки. Некоторые функции возвращают только внутренние или внешние ссылки. Например, функция C API [xlfCaller](xlfcaller.md) возвращает ссылку на ячейки вызова по определению на текущем листе. Возвращаемая ссылка всегда является внутренней ссылкой, хотя функция может возвращать нестандартные типы, в которых функция не вызвана из ячейки таблицы. Функция C API [xlSheetId](xlsheetid.md) всегда возвращает ID таблицы, содержаной в внешнем типе справочных данных. 
  
Другое ключевое различие между внутренними и внешними типами ссылок состоит в том, что тип внешних эталонных данных может описывать несколько несоединяемых блоков ячеек на одном листе. Внутренние ссылки могут описывать только один блок на текущем листе. Несоединяемые ссылки можно передать любой функции, которая принимает аргумент диапазона.
  
## <a name="see-also"></a>См. также



[Понятия, связанные с программированием для Excel](excel-programming-concepts.md)
  
[Оценка имен и других выражений в формулах листов](evaluating-names-and-other-worksheet-formula-expressions.md)
  
[Оценка выражений и листов Excel](excel-worksheet-and-expression-evaluation.md)

