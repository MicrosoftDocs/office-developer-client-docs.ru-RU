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

Мастер библиотеки типов Java — это функция Visual J++ 1.x, интегрированная в меню **Tools** среды разработки. Его цель — поиск библиотеки типов и создание интерфейса Java, который позволяет получать доступ к объектам COM. Для Visual J++ 6.0 мастер библиотеки java типа был заменен на ADO для [Windows классов Foundation.](ado-wfc-programming.md)

Мастер библиотеки типов Java дает такие же результаты, как и средства командной строки, включенные в [Microsoft SDK для Java.](using-the-microsoft-sdk-for-java.md) Однако нельзя ступить в обертки классов, созданные мастером, в отличие от оберток классов, созданных Microsoft SDK для Java.

Мастер библиотеки типов Java создает классы в следующем расположении: \\ \< windows directory \> \\ Java \\ trustlib \\ msado15. В Summary.txt, расположенном в каталоге, в котором были созданы классы, показаны созданные определения классов.

Мастер библиотеки типов Java преобразует переоцененные типы, найденные в любой библиотеке типа, для введите INT (integer). Он также определяет интерфейс, соответствующий каждому типу в библиотеке типов. Вы можете ссылаться на значения типа ADO, который приводится в следующем синтаксисе:

```vb 
 
msado15.<Enum Name>.<constant Name> 
```

Пример этого показан в следующем фрагменте кода для настройки свойства **CommandType** объекта **Command:**

```vb 
 
Cmd1.putCommandType( msado15.CommandTypeEnum.adCmdStoredProc ); 
```

Поочередно можно наследовать из обертки типа, которая создается мастером библиотеки java type. Если это так, можно удалить "msado15". из синтаксиса. Однако вашему классу необходимо наследовать от каждого объекта Java и переучесть тип интерфейса, ссылаясь на который он ссылается, чтобы полностью устранить необходимость ссылаться на msado15. \* перед всеми объектами ADO и переумещенными значениями.

Дополнительные примеры кода см. в [примере ADO Java Class Wrappers.](ado-java-class-wrappers.md)

**Запуск мастера библиотеки java типа из visual J++ версии 1.*x***

1.  Из меню **Tools** выберите **мастера библиотеки java type**.

2.  Выберите "Microsoft ActiveX библиотеку объектов данных" и нажмите **кнопку ОК**. Теперь (re)generates files in the \\ trustlib directory for ADO (by default at c: \\ winnt \\ Java \\ trustlib \\ msado15). Если вы уже использовали SDK Microsoft для Java для создания классов для ADO, они будут заменены мастером библиотеки java type.

3.  Чтобы использовать эти файлы, откройте проект в Visual J++. Из меню **Project** выберите **Добавить в Project.** Выберите **Файлы** и добавьте все . Java-файлы, созданные в \\ каталоге trustlib (по умолчанию c: \\ winnt \\ Java \\ trustlib \\ msado15) для вашего проекта.

