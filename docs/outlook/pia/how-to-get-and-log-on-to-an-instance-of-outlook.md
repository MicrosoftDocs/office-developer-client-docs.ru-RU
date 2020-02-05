---
title: Получение экземпляра Outlook и вход в него
TOCTitle: Get and sign in to an instance of Outlook
ms:assetid: 7f5057dc-4232-4dc7-b597-16ff5f7bcd7d
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-and-log-on-to-an-instance-of-outlook?redirectedfrom=MSDN
ms:contentKeyID: 55119926
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bae79531e7d2be39610194e0b59477fcee28c15
ms.sourcegitcommit: 31b0a7373ff74fe1d6383c30bc67d7675b73d283
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "41773703"
---
# <a name="get-and-sign-in-to-an-instance-of-outlook"></a><span data-ttu-id="9b020-102">Получение экземпляра Outlook и вход в него</span><span class="sxs-lookup"><span data-stu-id="9b020-102">Get and sign in to an instance of Outlook</span></span>

<span data-ttu-id="9b020-103">В этом разделе показано получение объекта [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?redirectedfrom=MSDN&view=outlook-pia), представляющего активный экземпляр приложения Microsoft Outlook (если таковой запущен на локальном компьютере), а также создание нового экземпляра Outlook с последующим входом в профиль по умолчанию и возвратом этого экземпляра Outlook.</span><span class="sxs-lookup"><span data-stu-id="9b020-103">This topic shows how to obtain an [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?redirectedfrom=MSDN&view=outlook-pia) object that represents an active instance of Microsoft Outlook, if there is one running on the local computer, or to create a new instance of Outlook, sign in to the default profile, and return that instance of Outlook.</span></span>

## <a name="example"></a><span data-ttu-id="9b020-104">Пример</span><span class="sxs-lookup"><span data-stu-id="9b020-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9b020-105">Приведенные ниже примеры кода создал Хельмут Обертаннер (Helmut Obertanner).</span><span class="sxs-lookup"><span data-stu-id="9b020-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="9b020-106">Хельмут специализируется на Outlook и инструментах разработчика Office для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9b020-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="9b020-107">В следующем примере кода используется метод GetApplicationObject класса Sample, который реализован в рамках проекта надстройки Outlook.</span><span class="sxs-lookup"><span data-stu-id="9b020-107">The following code examples contain the GetApplicationObject method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="9b020-108">Каждый проект добавляет ссылку на основную сборку взаимодействия Outlook на основе пространства имен [Microsoft.Office.Interop.Outlook](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?redirectedfrom=MSDN&view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="9b020-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook?redirectedfrom=MSDN&view=outlook-pia) namespace.</span></span>

<span data-ttu-id="9b020-109">Метод GetApplicationObject использует классы из библиотеки классов .NET Framework для проверки и получения процесса Outlook, запущенного на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9b020-109">The GetApplicationObject method uses classes in the .NET Framework class library to check and obtain any Outlook process running on the local computer.</span></span> <span data-ttu-id="9b020-110">При этом сначала используется метод [GetProcessesByName](https://docs.microsoft.com/dotnet/api/system.diagnostics.process.getprocessesbyname?redirectedfrom=MSDN&view=netframework-4.8#overloads) класса [Process](https://docs.microsoft.com/dotnet/api/system.diagnostics.process?redirectedfrom=MSDN&view=netframework-4.8) в пространстве имен [System.Diagnostics](https://docs.microsoft.com/dotnet/api/system.diagnostics?redirectedfrom=MSDN&view=netframework-4.8) для получения массива компонентов процесса на локальном компьютере, для которых используется общее имя процесса "OUTLOOK".</span><span class="sxs-lookup"><span data-stu-id="9b020-110">It first uses the [GetProcessesByName](https://docs.microsoft.com/dotnet/api/system.diagnostics.process.getprocessesbyname?redirectedfrom=MSDN&view=netframework-4.8#overloads) method of the [Process](https://docs.microsoft.com/dotnet/api/system.diagnostics.process?redirectedfrom=MSDN&view=netframework-4.8) class in the [System.Diagnostics](https://docs.microsoft.com/dotnet/api/system.diagnostics?redirectedfrom=MSDN&view=netframework-4.8) namespace to obtain an array of process components on the local computer that share the process name "OUTLOOK".</span></span> <span data-ttu-id="9b020-111">Для проверки наличия в массиве как минимум одного процесса Outlook метод GetApplicationObject использует запрос Microsoft LINQ.</span><span class="sxs-lookup"><span data-stu-id="9b020-111">To check whether the array does contain at least one Outlook process, GetApplicationObject uses Microsoft Language Integrated Query (LINQ).</span></span> <span data-ttu-id="9b020-112">В классе [Enumerable](https://msdn.microsoft.com/library/bb345746) пространства имен [System.Linq](https://msdn.microsoft.com/library/bb336768) представлен набор методов, в том числе метод [Count](https://msdn.microsoft.com/library/bb357758) , реализующий универсальный интерфейс [IEnumerable\<T\>](https://msdn.microsoft.com/library/9eekhta0) .</span><span class="sxs-lookup"><span data-stu-id="9b020-112">The [Enumerable](https://msdn.microsoft.com/library/bb345746) class in the [System.Linq](https://msdn.microsoft.com/library/bb336768) namespace provides a set of methods, including the [Count](https://msdn.microsoft.com/library/bb357758) method, that implement the [IEnumerable\<T\>](https://msdn.microsoft.com/library/9eekhta0) generic interface.</span></span> <span data-ttu-id="9b020-113">Так как в классе [Array](https://msdn.microsoft.com/library/czz5hkty) реализован интерфейс **IEnumerable(T)**, метод GetApplicationObject может применять метод **Count** к массиву, возвращаемому методом **GetProcessesByName**, для проверки наличия запущенных процессов Outlook.</span><span class="sxs-lookup"><span data-stu-id="9b020-113">Because the [Array](https://msdn.microsoft.com/library/czz5hkty) class implements the **IEnumerable(T)** interface, GetApplicationObject can apply the **Count** method to the array returned by **GetProcessesByName** to see whether there is an Outlook process running.</span></span> <span data-ttu-id="9b020-114">В случае обнаружения запущенного процесса метод GetApplicationObject с помощью метода [GetActiveObject](https://msdn.microsoft.com/library/xt620x09) класса [Marshal](https://msdn.microsoft.com/library/asx0thw2) в пространстве имен [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) для получения соответствующего экземпляра приложения Outlook и обеспечивает приведение этого объекта к объекту Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9b020-114">If there is, GetApplicationObject uses the [GetActiveObject](https://msdn.microsoft.com/library/xt620x09) method of the [Marshal](https://msdn.microsoft.com/library/asx0thw2) class in the [System.Runtime.InteropServices](https://msdn.microsoft.com/library/9esea608\(v=office.15\)) namespace to obtain that instance of Outlook, and casts that object to an Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

<span data-ttu-id="9b020-115">Если на локальном компьютере не запущено приложение Outlook, метод GetApplicationObject создает новый экземпляр приложения Outlook, использует метод [Logon(Object, Object, Object, Object)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._namespace.logon?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__NameSpace_Logon_System_Object_System_Object_System_Object_System_Object_) объекта [NameSpace](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.namespace?redirectedfrom=MSDN&view=outlook-pia) для входа в профиль по умолчанию, после чего возвращает новый экземпляр в приложение Outlook.</span><span class="sxs-lookup"><span data-stu-id="9b020-115">If Outlook is not running on the local computer, GetApplicationObject creates a new instance of Outlook, uses the [Logon(Object, Object, Object, Object)](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._namespace.logon?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook__NameSpace_Logon_System_Object_System_Object_System_Object_System_Object_) method of the [NameSpace](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.namespace?redirectedfrom=MSDN&view=outlook-pia) object to sign in to the default profile, and returns that new instance of Outlook.</span></span>

<span data-ttu-id="9b020-116">Ниже приведен пример кода на языке Visual Basic, за которым следует пример на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="9b020-116">The following is the Visual Basic code example, followed by the C\# code example.</span></span>

<span data-ttu-id="9b020-117">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9b020-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9b020-118">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="9b020-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9b020-119">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="9b020-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9b020-120">См. также</span><span class="sxs-lookup"><span data-stu-id="9b020-120">See also</span></span>

- [<span data-ttu-id="9b020-121">Сеансы</span><span class="sxs-lookup"><span data-stu-id="9b020-121">Sessions</span></span>](sessions.md)

