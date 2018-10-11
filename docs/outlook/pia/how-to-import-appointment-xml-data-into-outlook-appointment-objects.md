---
title: Импорт XML-данных встреч в объекты встреч Outlook
TOCTitle: Import appointment XML data into Outlook appointment objects
ms:assetid: 166a648a-1c48-4984-8889-a7614cc277b1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462092(v=office.15)
ms:contentKeyID: 55119821
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 22d7e17e208aa67648e2fe785d58bc030b41e001
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405835"
---
# <a name="import-appointment-xml-data-into-outlook-appointment-objects"></a>Импорт XML-данных встреч в объекты встреч Outlook

В этом разделе показаны методы чтения данных о встрече в формате XML, сохранения этих данных в объектах [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) календаря Outlook по умолчанию и возврата объектов встреч в массиве.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенные ниже примеры кода создал Хельмут Обертаннер (Helmut Obertanner). Хельмут специализируется на Outlook и инструментах разработчика Office для Visual Studio. 


В следующем примере кода используется метод CreateAppointmentsFromXml класса Sample, который реализован в рамках проекта надстройки Outlook. Каждый проект добавляет ссылку на основную сборку взаимодействия Outlook на основе пространства имен [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).

Метод CreateAppointmentsFromXml принимает два входных параметра:

  - Параметр application — это надежный объект Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)).

  - Параметр xml — это либо строка XML, либо строка, представляющая путь к правильному XML-файлу. В контексте следующих примеров кода XML разграничивает данные о встречах с помощью следующих XML-тегов.
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Данные встречи</p></th>
    <th><p>Разграничивающий XML-тег</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Весь набор данных встречи</p></td>
    <td><p>appointments</p></td>
    </tr>
    <tr class="even">
    <td><p>Каждая встреча в наборе</p></td>
    <td><p>appointment</p></td>
    </tr>
    <tr class="odd">
    <td><p>Время начала встречи</p></td>
    <td><p>starttime</p></td>
    </tr>
    <tr class="even">
    <td><p>Время окончания встречи</p></td>
    <td><p>endtime</p></td>
    </tr>
    <tr class="odd">
    <td><p>Название встречи</p></td>
    <td><p>subject</p></td>
    </tr>
    <tr class="even">
    <td><p>Место встречи</p></td>
    <td><p>location</p></td>
    </tr>
    <tr class="odd">
    <td><p>Подробные сведения о встрече</p></td>
    <td><p>body</p></td>
    </tr>
    </tbody>
    </table>


В следующем примере показаны входные данные для параметра *xml*.

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

В методе CreateAppointmentsFromXml используется реализация COM Microsoft модели DOM XML для загрузки и обработки XML-данных, предоставляемых параметром xml. Метод CreateAppointmentsFromXml сначала проверяет, указывает ли xml правильный источник XML-данных. Если источник правильный, то этот метод загружает данные в XML-документ [DOMDocument](https://msdn.microsoft.com/library/ms756987\(v=office.15\)). В противном случае метод CreateAppointmentsFromXml создает исключение. Дополнительные сведения о модели DOM XML см. в разделе [DOM](https://msdn.microsoft.com/library/ms766487\(v=office.15\)).

Для каждого дочернего элемента встречи, разграниченного тегом встречи в XML-данных, метод CreateAppointmentsFromXml выполняет поиск конкретных тегов, извлекает данные с помощью DOM и назначает данные соответствующим свойствам объекта **AppointmentItem**: [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)), [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611653\(v=office.15\)), [Location](https://msdn.microsoft.com/library/bb608946\(v=office.15\)) и [Body](https://msdn.microsoft.com/library/bb644880\(v=office.15\)). Затем метод CreateAppointmentsFromXml сохраняет встречу в календарь по умолчанию.

CreateAppointmentsFromXml использует метод [Add](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.add?view=netframework-4.7.2) класса [List\<T\>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1?view=netframework-4.7.2) в пространстве имен [System.Collections.Generic](https://docs.microsoft.com/dotnet/api/system.collections.generic?view=netframework-4.7.2), чтобы собрать эти объекты AppointmentItem. После обработки всех встреч в XML-данных метод возвращает объекты AppointmentItem в массив.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

Ниже приведен пример кода на языке Visual Basic, за которым следует пример на языке C\#.



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

## <a name="see-also"></a>См. также

- [Встречи](appointments.md)

