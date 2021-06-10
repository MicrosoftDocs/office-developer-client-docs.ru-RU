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

Microsoft SDK для Java — это набор разработчиков для среды Microsoft Internet Explorer. Для разработки java-программ и applets на основе JDK 1.1 и виртуальной машины Microsoft Win32 (Microsoft VM) предоставляются средства, сведения и примеры. SDK Microsoft для Java не привязан к Microsoft Visual J++.

Утилита Jactivex.exe создает классы из библиотеки типов, но может вызываться только в командной строке. Эта функция не интегрирована с средой разработки Visual J++. В отличие от классов, созданных мастером [библиотеки java type,](using-the-java-type-library-wizard.md)можно ввести обертки классов, созданные SDK. Это полезно для отладки использования кодом классов оболочки ADO.

Этот механизм считывает библиотеку типов ADO и создает классы, которые можно мгновенно использовать в приложении. Он создает эти классы в следующем расположении: \\ \< windows directory \> \\ Java \\ trustlib \\ msado15.

Создание приложения ADO на Java с помощью Microsoft SDK для Java принципиально идентично с точки зрения исходных кодов использованию мастера библиотеки java type. Пример кода см. в [примере ADO Java Class Wrappers.](ado-java-class-wrappers.md) Единственное реальное различие заключается в том, как вы создаете классы оболочки в первую очередь, как показано на ниже.

**Создание проекта ADO с помощью Microsoft SDK для Java**

1.  Запустите следующее из командной подсказки. Необходимо задать путь к включению каталога Microsoft SDK для Java Bin или выполнить команду из этого расположения. Как правило, microsoft SDK для Java устанавливается в том же месте, что и Visual Studio. Это одно командная команда.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Запустите следующую команду для компиляции созданных классов. Переключатель /g:t включает генерацию символов отключки, чтобы вы могли отслеживать . Символы Java. Удалите его для сборки выпуска.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Чтобы использовать эти файлы, откройте проект в Visual J++. Из меню **Project** выберите **Добавить в Project.** Выберите **Файлы** и добавьте все . Java-файлы, созданные в каталоге \\ trustlib msado15 для проекта.

