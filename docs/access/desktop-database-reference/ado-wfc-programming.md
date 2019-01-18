---
title: Программирование ADO/WFC
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 904b5e3930c0e7e7b1d98f94bd39cfbf816aa145
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720508"
---
# <a name="adowfc-programming"></a>Программирование ADO/WFC

**Применимо к**: Access 2013, Office 2013

Для Microsoft Visual J ++ 6.0 ADO расширен для работы с Windows Foundation классы (WFC) следующим образом. Во-первых набор классов Java был реализован, который расширяет интерфейс ADO и создает уведомления интересно программиста Java; классы Java также предоставляют функции, которые возвращают типы Java для пользователя. В целях повышения производительности класс Java непосредственно обращается к собственных типов данных в объекте набор строк OLE DB и возвращает их программисту Java как типы Java без предварительного преобразования их в и из него переменную типа variant. Также была расширена ADO для работы с уведомления о событиях в платформе WFC.

ADO для Windows классов (ADO/WFC) поддерживает все стандартные ADO методы, свойства, объектов и событий. Тем не менее операции, которые требуют вариант в качестве параметра и отображение высокая производительность на языке, такие как Microsoft Visual Basic, отображение снижения производительности на языке, например Visual J ++. По этой причине ADO/WFC также предоставляет функции для доступа к данным на объект [поля](field-object-ado.md) , вступили в собственных типов данных Java вместо тип данных variant.

Для получения дополнительных сведений в ADO документацию о пакетах ADO/WFC [ADO/WFC синтаксис](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)см.

## <a name="referencing-the-library"></a>Создание ссылок на библиотеку

Для импорта классов данных ADO/WFC в проекте, необходимо включите следующую строку кода:

```java 
 
import com.ms.wfc.data.*; 
```

