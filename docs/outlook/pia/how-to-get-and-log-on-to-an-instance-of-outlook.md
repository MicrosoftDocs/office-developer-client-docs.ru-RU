---
title: Получение экземпляра Outlook и вход в него
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-and-log-on-to-an-instance-of-outlook?redirectedfrom=MSDN
ms:contentKeyID: 55119926
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: edcf2053a2f678b2280e1735ee728196cc431d31
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819345"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a>Получение экземпляра Outlook и вход в него

В этом разделе показано получение объекта [Application](https://docs.microsoft.com/en-us/dotnet/api/microsoft.office.interop.outlook.application?redirectedfrom=MSDN&view=outlook-pia), представляющего активный экземпляр приложения Microsoft Outlook (если таковой запущен на локальном компьютере), а также создание нового экземпляра Outlook с последующим входом в профиль по умолчанию и возвратом этого экземпляра Outlook.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенные ниже примеры кода создал Хельмут Обертаннер (Helmut Obertanner). Хельмут специализируется на Outlook и инструментах разработчика Office для Visual Studio. 

В следующем примере кода используется метод GetApplicationObject класса Sample, который реализован в рамках проекта надстройки Outlook. Каждый проект добавляет ссылку на основную сборку взаимодействия Outlook на основе пространства имен [Microsoft.Office.Interop.Outlook](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?redirectedfrom=MSDN&view=outlook-pia).

Метод GetApplicationObject использует классы из библиотеки классов .NET Framework для проверки и получения процесса Outlook, запущенного на локальном компьютере. При этом сначала используется метод [GetProcessesByName](https://docs.microsoft.com/dotnet/api/system.diagnostics.process.getprocessesbyname?redirectedfrom=MSDN&view=netframework-4.8#overloads) класса [Process](https://docs.microsoft.com/dotnet/api/system.diagnostics.process?redirectedfrom=MSDN&view=netframework-4.8) в пространстве имен [System.Diagnostics](https://docs.microsoft.com/dotnet/api/system.diagnostics?redirectedfrom=MSDN&view=netframework-4.8) для получения массива компонентов процесса на локальном компьютере, для которых используется общее имя процесса "OUTLOOK". Для проверки наличия в массиве как минимум одного процесса Outlook метод GetApplicationObject использует запрос Microsoft LINQ. В классе [Enumerable](https://msdn.microsoft.com/library/bb345746) пространства имен [System.Linq](https://msdn.microsoft.com/library/bb336768) представлен набор методов, в том числе метод [Count](https://msdn.microsoft.com/library/bb357758) , реализующий универсальный интерфейс [IEnumerable\<T\>](https://msdn.microsoft.com/library/9eekhta0) . Так как в классе [Array](https://msdn.microsoft.com/library/czz5hkty) реализован интерфейс **IEnumerable(T)**, метод GetApplicationObject может применять метод **Count** к массиву, возвращаемому методом **GetProcessesByName**, для проверки наличия запущенных процессов Outlook. В случае обнаружения запущенного процесса метод GetApplicationObject с помощью метода [GetActiveObject](https://msdn.microsoft.com/library/xt620x09) класса [Marshal](https://msdn.microsoft.com/library/asx0thw2) в пространстве имен [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) для получения соответствующего экземпляра приложения Outlook и обеспечивает приведение этого объекта к объекту Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)).

Если на локальном компьютере не запущено приложение Outlook, метод GetApplicationObject создает новый экземпляр приложения Outlook, использует метод [Logon(Object, Object, Object, Object)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._namespace.logon?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__NameSpace_Logon_System_Object_System_Object_System_Object_System_Object_) объекта [NameSpace](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.namespace?redirectedfrom=MSDN&view=outlook-pia) для входа в профиль по умолчанию, после чего возвращает новый экземпляр в приложение Outlook.

Ниже приведен пример кода на языке Visual Basic, за которым следует пример на языке C\#.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports System.Diagnostics
Imports System.Linq
Imports System.Reflection
Imports System.Runtime.InteropServices
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample

        Function GetApplicationObject() As Outlook.Application

            Dim application As Outlook.Application

            ' Check whether there is an Outlook process running.
            If Process.GetProcessesByName("OUTLOOK").Count() > 0 Then

                ' If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = DirectCast(Marshal.GetActiveObject("Outlook.Application"), Outlook.Application)
            Else

                ' If not, create a new instance of Outlook and sign in to the default profile.
                application = New Outlook.Application()
                Dim ns As Outlook.NameSpace = application.GetNamespace("MAPI")
                ns.Logon("", "", Missing.Value, Missing.Value)
                ns = Nothing
            End If

            ' Return the Outlook Application object.
            Return application
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Diagnostics;
using System.Linq;
using System.Reflection;
using System.Runtime.InteropServices;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.Application GetApplicationObject()
        {

            Outlook.Application application = null;

            // Check whether there is an Outlook process running.
            if (Process.GetProcessesByName("OUTLOOK").Count() > 0)
            {

                // If so, use the GetActiveObject method to obtain the process and cast it to an Application object.
                application = Marshal.GetActiveObject("Outlook.Application") as Outlook.Application;
            }
            else
            {

                // If not, create a new instance of Outlook and sign in to the default profile.
                application = new Outlook.Application();
                Outlook.NameSpace nameSpace = application.GetNamespace("MAPI");
                nameSpace.Logon("", "", Missing.Value, Missing.Value);
                nameSpace = null;
            }

            // Return the Outlook Application object.
            return application;
        }

    }
}
```

## <a name="see-also"></a>См. также

- [Сеансы](sessions.md)

