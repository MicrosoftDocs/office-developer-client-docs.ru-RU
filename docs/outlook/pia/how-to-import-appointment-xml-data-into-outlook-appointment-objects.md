---
title: Импорт XML-данных встреч в объекты встреч Outlook
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0af86772fced3e69d1d28cf8d98a544e3b4d90d2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705388"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a><span data-ttu-id="95b65-102">Импорт XML-данных встреч в объекты встреч Outlook</span><span class="sxs-lookup"><span data-stu-id="95b65-102">Import appointment XML data into Outlook appointment objects</span></span>

<span data-ttu-id="95b65-103">В этом разделе показаны методы чтения данных о встрече в формате XML, сохранения этих данных в объектах [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) календаря Outlook по умолчанию и возврата объектов встреч в массиве.</span><span class="sxs-lookup"><span data-stu-id="95b65-103">This topic shows how to read appointment data formatted in XML, save the data to Outlook [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) objects in the default calendar, and return the appointment objects in an array.</span></span>

## <a name="example"></a><span data-ttu-id="95b65-104">Пример</span><span class="sxs-lookup"><span data-stu-id="95b65-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="95b65-105">Приведенные ниже примеры кода создал Хельмут Обертаннер (Helmut Obertanner).</span><span class="sxs-lookup"><span data-stu-id="95b65-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="95b65-106">Хельмут специализируется на Outlook и инструментах разработчика Office для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="95b65-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="95b65-107">В следующем примере кода используется метод CreateAppointmentsFromXml класса Sample, который реализован в рамках проекта надстройки Outlook.</span><span class="sxs-lookup"><span data-stu-id="95b65-107">The following code examples contain the CreateAppointmentsFromXml method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="95b65-108">Каждый проект добавляет ссылку на основную сборку взаимодействия Outlook на основе пространства имен [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="95b65-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="95b65-109">Метод CreateAppointmentsFromXml принимает два входных параметра:</span><span class="sxs-lookup"><span data-stu-id="95b65-109">The CreateAppointmentsFromXml method accepts two input parameters:</span></span>

  - <span data-ttu-id="95b65-110">Параметр application — это надежный объект Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="95b65-110">application is a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object.</span></span>

  - <span data-ttu-id="95b65-p103">Параметр xml — это либо строка XML, либо строка, представляющая путь к правильному XML-файлу. В контексте следующих примеров кода XML разграничивает данные о встречах с помощью следующих XML-тегов.</span><span class="sxs-lookup"><span data-stu-id="95b65-p103">xml is either an XML string, or a string that represents a path to a valid XML file. For the purpose of the following code examples, the XML delimits appointment data by using the following XML tags:</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="95b65-113">Данные встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-113">Appointment data</span></span></p></th>
    <th><p><span data-ttu-id="95b65-114">Разграничивающий XML-тег</span><span class="sxs-lookup"><span data-stu-id="95b65-114">Delimiting XML tag</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="95b65-115">Весь набор данных встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-115">Entire set of appointment data</span></span></p></td>
    <td><p><span data-ttu-id="95b65-116">appointments</span><span class="sxs-lookup"><span data-stu-id="95b65-116">appointments</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="95b65-117">Каждая встреча в наборе</span><span class="sxs-lookup"><span data-stu-id="95b65-117">Each appointment in the set</span></span></p></td>
    <td><p><span data-ttu-id="95b65-118">appointment</span><span class="sxs-lookup"><span data-stu-id="95b65-118">appointment</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="95b65-119">Время начала встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-119">Start time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="95b65-120">starttime</span><span class="sxs-lookup"><span data-stu-id="95b65-120">starttime</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="95b65-121">Время окончания встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-121">End time of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="95b65-122">endtime</span><span class="sxs-lookup"><span data-stu-id="95b65-122">endtime</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="95b65-123">Название встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-123">Title of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="95b65-124">subject</span><span class="sxs-lookup"><span data-stu-id="95b65-124">subject</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="95b65-125">Место встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-125">Location of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="95b65-126">location</span><span class="sxs-lookup"><span data-stu-id="95b65-126">location</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="95b65-127">Подробные сведения о встрече</span><span class="sxs-lookup"><span data-stu-id="95b65-127">Details of an appointment</span></span></p></td>
    <td><p><span data-ttu-id="95b65-128">body</span><span class="sxs-lookup"><span data-stu-id="95b65-128">body</span></span></p></td>
    </tr>
    </tbody>
    </table>


<span data-ttu-id="95b65-129">В следующем примере показаны входные данные для параметра *xml*.</span><span class="sxs-lookup"><span data-stu-id="95b65-129">The following example shows input data for the *xml* parameter.</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?> 
<appointments>
    <appointment>
        <starttime>2009-06-01T15:00:00</starttime>
        <endtime>2009-06-01T16:15:00</endtime>
        <subject>This is a Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T17:15:00</endtime>
        <subject>This is a second Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
    <appointment>
        <starttime>2009-06-01T17:00:00</starttime>
        <endtime>2009-06-01T18:15:00</endtime>
        <subject>This is a third Test-Appointment</subject>
        <location>At your Desk</location>
        <body>Here is the Bodytext</body>
    </appointment>
</appointments>
```

<span data-ttu-id="95b65-p104">В методе CreateAppointmentsFromXml используется реализация COM Microsoft модели DOM XML для загрузки и обработки XML-данных, предоставляемых параметром xml. Метод CreateAppointmentsFromXml сначала проверяет, указывает ли xml правильный источник XML-данных. Если источник правильный, то этот метод загружает данные в XML-документ [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). В противном случае метод CreateAppointmentsFromXml создает исключение. Дополнительные сведения о модели DOM XML см. в разделе [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="95b65-p104">The CreateAppointmentsFromXml method uses the Microsoft COM implementation of the XML Document Object Model (DOM) to load and process the XML data that xml provides. CreateAppointmentsFromXml first checks whether xml specifies a valid source of XML data. If so, it loads the data into an XML document, [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). Otherwise, CreateAppointmentsFromXml throws an exception. For more information about the XML DOM, see [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).</span></span>

<span data-ttu-id="95b65-135">Для каждого дочернего элемента встречи, разграниченного тегом встречи в XML-данных, метод CreateAppointmentsFromXml выполняет поиск конкретных тегов, извлекает данные с помощью DOM и назначает их соответствующим свойствам объекта **AppointmentItem**: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) и [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="95b65-135">For each appointment child node delimited by the appointment tag in the XML data, CreateAppointmentsFromXml looks for specific tags, uses the DOM to extract the data, and assigns the data to corresponding properties of an **AppointmentItem** object: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)).</span></span> <span data-ttu-id="95b65-136">Затем метод CreateAppointmentsFromXml сохраняет встречу в календарь, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95b65-136">CreateAppointmentsFromXml then saves the appointment to the default calendar.</span></span>

<span data-ttu-id="95b65-137">CreateAppointmentsFromXml использует метод [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) класса [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) в пространстве имен [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2), чтобы собрать эти объекты AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="95b65-137">CreateAppointmentsFromXml uses the [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) method of the [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) class in the [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2) namespace to aggregate these AppointmentItem objects.</span></span> <span data-ttu-id="95b65-138">После обработки всех встреч в XML-данных метод возвращает объекты AppointmentItem в массив.</span><span class="sxs-lookup"><span data-stu-id="95b65-138">When the method has processed all the appointments in the XML data, it returns the AppointmentItem objects in an array.</span></span>

<span data-ttu-id="95b65-139">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="95b65-139">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="95b65-140">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением public Class.</span><span class="sxs-lookup"><span data-stu-id="95b65-140">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="95b65-141">В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="95b65-141">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="95b65-142">Ниже приведен пример кода на языке Visual Basic, за которым следует пример на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="95b65-142">The following is the Visual Basic code example, followed by the C\# code example.</span></span>



```vb
Imports System.IO
Imports System.Xml
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Function CreateAppointmentsFromXml(ByVal application As Outlook.Application, _
            ByVal xml As String) As Outlook.AppointmentItem()

            Dim appointments As New List(Of Outlook.AppointmentItem)
            Dim xmlDoc As New XmlDocument()

            ' If xml is an XML string, create the XML document directly.
            If xml.StartsWith("<?xml") Then
                xmlDoc.LoadXml(xml)
            ElseIf (File.Exists(xml)) Then
                xmlDoc.Load(xml)
            Else
                Throw New Exception("The input string is not valid XML data or the specified file doesn't exist.")
            End If


            ' Select all appointment nodes under the root appointments node.
            Dim appointmentNodes As XmlNodeList = xmlDoc.SelectNodes("appointments/appointment")

            For Each appointmentNode As XmlNode In appointmentNodes

                ' Create a new AppointmentItem object.
                Dim newAppointment As Outlook.AppointmentItem = _
                    DirectCast(application.CreateItem(Outlook.OlItemType.olAppointmentItem), _
                    Outlook.AppointmentItem)

                ' Loop over all child nodes, check the node name, and import the data into the appointment fields.

                For Each node As XmlNode In appointmentNode.ChildNodes
                    Select Case (node.Name)

                        Case "starttime"
                            newAppointment.Start = DateTime.Parse(node.InnerText)


                        Case "endtime"
                            newAppointment.End = DateTime.Parse(node.InnerText)


                        Case "subject"
                            newAppointment.Subject = node.InnerText


                        Case "location"
                            newAppointment.Location = node.InnerText


                        Case "body"
                            newAppointment.Body = node.InnerText


                    End Select
                Next

                ' Save the item in the default calendar.
                newAppointment.Save()
                appointments.Add(newAppointment)
            Next

            ' Return an array of new appointments.
            Return appointments.ToArray()
        End Function


    End Class
End Namespace
```



```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Text;
using System.Xml;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        Outlook.AppointmentItem[] CreateAppointmentsFromXml(Outlook.Application application, 
            string xml)
        {
            // Create a list of appointment objects.
            List<Outlook.AppointmentItem> appointments = new 
                List<Microsoft.Office.Interop.Outlook.AppointmentItem>();
            XmlDocument xmlDoc = new XmlDocument();

            // If xml is an XML string, create the document directly. 
            if (xml.StartsWith("<?xml"))
            {
                xmlDoc.LoadXml(xml);
            }
            else if (File.Exists(xml))
            {
                xmlDoc.Load(xml);
            }
            else
            {
                throw new Exception(
                    "The input string is not valid XML data or the specified file doesn't exist.");
            }

            // Select all appointment nodes under the root appointments node.
            XmlNodeList appointmentNodes = xmlDoc.SelectNodes("appointments/appointment");
            foreach (XmlNode appointmentNode in appointmentNodes)
            {

                // Create a new AppointmentItem object.
                Outlook.AppointmentItem newAppointment = 
                    (Outlook.AppointmentItem)application.CreateItem(Outlook.OlItemType.olAppointmentItem);

                // Loop over all child nodes, check the node name, and import the data into the 
                // appointment fields.
                foreach (XmlNode node in appointmentNode.ChildNodes)
                {
                    switch (node.Name)
                    {

                        case "starttime":
                            newAppointment.Start = DateTime.Parse(node.InnerText);
                            break;

                        case "endtime":
                            newAppointment.End = DateTime.Parse(node.InnerText);
                            break;

                        case "subject":
                            newAppointment.Subject = node.InnerText;
                            break;

                        case "location":
                            newAppointment.Location = node.InnerText;
                            break;

                        case "body":
                            newAppointment.Body = node.InnerText;
                            break;

                    }
                }

                // Save the item in the default calendar.
                newAppointment.Save();
                appointments.Add(newAppointment);
            }

            // Return an array of new appointments.
            return appointments.ToArray();
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="95b65-143">См. также</span><span class="sxs-lookup"><span data-stu-id="95b65-143">See also</span></span>

- [<span data-ttu-id="95b65-144">Встречи</span><span class="sxs-lookup"><span data-stu-id="95b65-144">Appointments</span></span>](appointments.md)

