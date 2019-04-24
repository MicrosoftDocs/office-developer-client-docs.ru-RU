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

Microsoft SDK для Java — это набор разработчиков для среды Microsoft Internet Explorer. Средства, сведения и примеры предоставляются для упрощения разработки программ и приложений Java на основе ЖДК 1,1 и виртуальной машины Microsoft Win32 (Microsoft VM). ПАКЕТ Microsoft SDK для Java не связан с Microsoft Visual J++.

Служебная программа Жактивекс. exe создает классы из библиотеки типов, но может вызываться только в командной строке. Эта функция не интегрирована с средой разработки Visual J++. В отличие от классов, созданных с помощью [мастера библиотек типов Java](using-the-java-type-library-wizard.md), вы можете перейти к оболочкам классов, СОЗДАНным пакетом SDK. Это полезно для отладки того, как код использует классы оболочки ADO.

Этот механизм считывает библиотеку типов ADO и создает классы, которые можно создавать в приложении. Он создает эти классы в следующем расположении: \\ \<каталог\>\\Windows Java\\трустлиб\\Msado15.

Создание приложения ADO в Java с помощью Microsoft SDK для Java является принципиально идентичным, с точки зрения исходного кода, с помощью мастера библиотек типов Java. Пример кода приведен в разделе [оболочки классов ADO Java](ado-java-class-wrappers.md). Единственное реальное отличие состоит в том, как вы создаете классы оберток в первом месте, как показано в приведенных ниже шагах.

**Создание проекта ADO с помощью Microsoft SDK для Java**

1.  Выполните следующую команду в командной строки. Необходимо задать путь, чтобы включить каталог Microsoft SDK для Java, или выполнить команду из этого расположения. Как правило, Microsoft SDK для Java устанавливается в ту же папку, что и Visual Studio. Это один командный оператор.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Выполните следующую команду, чтобы скомпилировать созданные классы. Параметр/g: t включает создание символов отладки, чтобы можно было выполнить трассировку в файле. Символы Java. Удалите его для сборок выпуска.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Чтобы использовать эти файлы, откройте проект в Visual J++. В меню **проект** выберите команду **Добавить в проект**. Выберите **файлы**и добавьте все файлы. Файлы JAVA, созданные в каталоге\\трустлиб MsADO15, в свой проект.

