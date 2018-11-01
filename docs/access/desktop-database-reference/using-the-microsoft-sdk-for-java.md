---
title: Использование пакета SDK (Майкрософт) для Java
TOCTitle: Using the Microsoft SDK for Java
ms:assetid: 35a1adb2-06d6-ff45-f151-f1f60ff9bfe2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249116(v=office.15)
ms:contentKeyID: 48544152
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8b34f02d01b5f119d9311e290f354ccbc71182d2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872552"
---
# <a name="using-the-microsoft-sdk-for-java"></a>Использование пакета SDK (Майкрософт) для Java


**Применимо к**: Access 2013, Office 2013

Пакет SDK Microsoft для Java — это комплект материалов для разработчиков для среды Microsoft Internet Explorer. Средства, сведения и примеры предоставляются помогут вам в разработке программы Java и приложения на основе JDK 1.1 и виртуальной машины Microsoft Win32 (виртуальной Машины Microsoft). Пакет SDK Microsoft для Java не привязан к Microsoft Visual J ++.

Служебная программа Jactivex.exe создает классы из библиотеки типов, но может быть вызван только в командной строке. Этот компонент не интегрирована в среде разработки Visual J ++. В отличие от классов, созданных с помощью [Мастера библиотеки типов Java](using-the-java-type-library-wizard.md)можно выполнить пошагово класс оболочки, созданные в пакете SDK. Это полезно для отладки, как код использует классы программы-оболочки для ADO.

Этот механизм считывает библиотека типов ADO и создает классы, которые можно создать в приложении. Эти классы создаются в следующем расположении: \\ \<каталог windows\>\\Java\\trustlib\\msado15.

Создание приложения ADO в Java, с помощью пакета SDK Microsoft для Java идентична существенно, с точки зрения исходного кода с помощью мастера Java типа библиотеки. Пример кода в разделе [ADO Java класс оболочки](ado-java-class-wrappers.md). Только фактическое различие — в процесса создания программы-оболочки для классов в первую очередь, как показано в следующих шагах.

**Чтобы создать проект ADO с помощью пакета SDK Microsoft для Java**

1.  Выполните следующую команду в командной строке. Необходимо задать путь для включения пакета SDK Microsoft для каталог Java Bin или выполните команду из этого расположения. Как правило пакет SDK Microsoft для Java установлен в ту же папку, как Visual Studio. Это оператор одной команды.
    
    ```vb 
     
    \<path to DevStudio>\<path to Java SDK>\bin\JactiveX.exe /javatlb "C:\program files\common files\system\ado\msado15.dll" 
    ```

2.  Выполните следующую команду, чтобы скомпилировать созданных классов. Переключатель /g:t включает создание символов отладки, чтобы можно было отслеживать в. Символы Java. Удалите его для построения выпуска.
    
    ```vb 
     
    jvc /g:t c:\<windows>\Java\trustlib\msado15\*.Java 
    ```

3.  Чтобы использовать эти файлы, откройте свой проект в Visual J ++. В меню **проект** выберите **Добавить в проект**. Выберите **файлы**и добавьте все. Файлы JAVA, созданные в trustlib\\msado15 каталогов в проект.

