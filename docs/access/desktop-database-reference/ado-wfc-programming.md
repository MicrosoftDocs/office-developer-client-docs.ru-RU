---
title: ADO/WFC Programming
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88343d14a9419cbc3425e0c21dee08d243f2e697
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480281"
---
# <a name="adowfc-programming"></a>ADO/WFC Programming


**Применимо к**: Access 2013 | Office 2013

Для Microsoft Visual J ++ 6.0 ADO расширен для работы с Windows Foundation классы (WFC) следующим образом. Во-первых набор классов Java был реализован, который расширяет интерфейс ADO и создает уведомления интересно программиста Java; классы Java также предоставляют функции, которые возвращают типы Java для пользователя. В целях повышения производительности класс Java непосредственно обращается к собственных типов данных в объекте набор строк OLE DB и возвращает их программисту Java как типы Java без предварительного преобразования их в и из него переменную типа variant. Также была расширена ADO для работы с уведомления о событиях в платформе WFC.

ADO для Windows классов (ADO/WFC) поддерживает все стандартные ADO методы, свойства, объектов и событий. Тем не менее операции, которые требуют вариант в качестве параметра и отображение высокая производительность на языке, такие как Microsoft Visual Basic, отображение снижения производительности на языке, например Visual J ++. По этой причине ADO/WFC также предоставляет функции для доступа к данным на объект [поля](field-object-ado.md) , вступили в собственных типов данных Java вместо тип данных variant.

Для получения дополнительных сведений в ADO документацию о пакетах ADO/WFC [ADO/WFC синтаксис](https://msdn.microsoft.com/library/jj250066\(v=office.15\))см.

## <a name="referencing-the-library"></a>Создание ссылок на библиотеку

Для импорта классов данных ADO/WFC в проекте, необходимо включите следующую строку кода:

```java 
 
import com.ms.wfc.data.*; 
```

