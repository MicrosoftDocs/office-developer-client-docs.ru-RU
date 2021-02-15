---
title: Использование мастера библиотеки типов Java
TOCTitle: Using the Java Type Library Wizard
ms:assetid: 96af770c-c7c2-c905-3c3e-383a5b99cab2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249670(v=office.15)
ms:contentKeyID: 48546455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a27491acabd19f688eca4159a36dcfcfc486a026
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312084"
---
# <a name="using-the-java-type-library-wizard"></a>Использование мастера библиотеки типов Java


**Область применения**: Access 2013, Office 2013

Мастер библиотеки типов Java — это функция Visual J++ 1.x, интегрированная в меню "Инструменты" среды разработки.  Она предназначена для поиска в библиотеке типов и создания интерфейса Java, который обеспечивает доступ к com-объектам. Для Visual J++ 6.0 мастер библиотеки типов Java заменен [на ADO для классов Windows Foundation.](ado-wfc-programming.md)

Мастер библиотеки типов Java дает такие же результаты, как средства командной строки, включенные в [Microsoft SDK для Java.](using-the-microsoft-sdk-for-java.md) Однако вы не можете ступить в программы-оболочки класса, созданные мастером, в отличие от оберток класса, созданных пакетом Microsoft SDK для Java.

Мастер библиотеки типов Java создает классы в следующем расположении: \\ \< \> \\ Java trustlib каталога Windows \\ \\ msado15. В Summary.txt, расположенном в каталоге, в котором были созданы классы, показаны созданные определения классов.

Мастер библиотеки типов Java преобразует типы, найденные в любой библиотеке типов, в тип INT (integer). Кроме того, он определяет интерфейс, соответствующий каждому типу в библиотеке типов. Со следующим синтаксис можно ссылаться на значения типа, в который был добавлен код ADO:

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

Пример этого показан в следующем фрагменте кода для настройки свойства **CommandType** объекта **Command:**

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

Кроме того, вы можете наследоваться от оболочки с кодом типа, которая создается мастером библиотеки типов Java. В этом случае можно удалить "msado15". из синтаксиса. Однако класс должен наследоваться от каждого объекта Java и интерфейса нумерованных типов, на который он ссылается, чтобы полностью исключить необходимость ссылок на msado15. \* перед всеми объектами ADO и enumerated значениями.

Дополнительные примеры кода см. в примере [программы-оболочки java Class Wrappers для ADO.](ado-java-class-wrappers.md)

**Запуск мастера библиотеки типов Java из Visual J++ версии 1.*x***

1.  В меню **"Инструменты"** выберите мастер **библиотеки типов Java.**

2.  Выберите "Microsoft ActiveX Data Objects Library" и нажмите кнопку **"ОК".** This now (re)generates files in the \\ trustlib directory for ADO (by default at c: \\ winnt \\ java \\ trustlib \\ msado15). Если вы уже использовали Microsoft SDK для Java для создания классов для ADO, они будут заменены на классы из мастера библиотеки типов Java.

3.  Чтобы использовать эти файлы, откройте проект в Visual J++. В меню **"Проект"** выберите пункт **"Добавить в проект".** Выберите **"Файлы"** и добавьте все файлы. Java-файлы, созданные в \\ каталоге trustlib (по умолчанию в c: \\ winnt \\ java \\ trustlib \\ msado15) для вашего проекта.

