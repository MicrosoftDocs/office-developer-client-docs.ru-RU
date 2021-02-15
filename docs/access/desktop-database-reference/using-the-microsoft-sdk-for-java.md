---
title: Использование пакета Microsoft SDK для Java
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d297d019602cef7b6fbc4f5b0125b87ef642213f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305998"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Использование пакета Microsoft SDK для Java


**Область применения**: Access 2013, Office 2013

Пакет Microsoft SDK для Java — это набор разработчиков для среды Microsoft Internet Explorer. Предоставляются инструменты, сведения и примеры, которые помогут вам разрабатывать java-программы и applets на основе JDK 1.1 и виртуальной машины Microsoft Win32 (microsoft VM). Microsoft SDK для Java не привязан к Microsoft Visual J++.

С Jactivex.exe создает классы из библиотеки типов, но их можно вызвать только в командной строке. Эта функция не интегрирована со средой разработки Visual J++. В отличие от классов, созданных мастером библиотеки типов [Java,](using-the-java-type-library-wizard.md)вы можете ступить в оболочки класса, созданные пакетом SDK. Это полезно для отладки того, как код использует классы-оболочки ADO.

Этот механизм считывает библиотеку типов ADO и создает классы, которые можно создать в приложении. Эти классы создаются в следующем расположении: \\ \< Java \> \\ \\ trustlib \\ msado15 каталога Windows.

Создание приложения ADO на Java с помощью Microsoft SDK для Java практически идентично с точки зрения исходных кодов и использованию мастера библиотеки типов Java. Пример кода см. в примере [программы-оболочки java Class Wrappers для ADO.](ado-java-class-wrappers.md) Единственное реальное различие заключается в том, как сначала создаются классы-оболочки, как показано в шагах ниже.

**Создание проекта ADO с помощью Microsoft SDK для Java**

1.  Запустите следующую команду из командной подсказки. Необходимо настроить путь, чтобы включить каталог Microsoft SDK для Java Bin, или выполнить команду из этого расположения. Как правило, Microsoft SDK для Java устанавливается в том же расположении, что и Visual Studio. Это один командный пункт.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Чтобы скомпилировать созданные классы, запустите следующую команду. Переключатель /g:t включает генерацию символов отлаки, чтобы можно было отследить их. Символы Java. Удалите его для сборки выпусков.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Чтобы использовать эти файлы, откройте проект в Visual J++. В меню **"Проект"** выберите пункт **"Добавить в проект".** Выберите **"Файлы"** и добавьте все файлы. Java-файлы, созданные в каталоге \\ trustlib msado15 для вашего проекта.

