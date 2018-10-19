---
title: Доступ к данным решений, хранящимся в скрытом сообщении в папке
TOCTitle: Access solution-specific data stored as a hidden message in a folder
ms:assetid: bacf0562-1026-4c3b-87b0-4eaad5033592
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623414(v=office.15)
ms:contentKeyID: 55119861
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 5134cc2b3a71f8fe93970f040a44d16291dbbb0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405548"
---
# <a name="access-solution-specific-data-stored-as-a-hidden-message-in-a-folder"></a><span data-ttu-id="12f0c-102">Доступ к данным решений, хранящимся в скрытом сообщении в папке</span><span class="sxs-lookup"><span data-stu-id="12f0c-102">Access solution-specific data stored as a hidden message in a folder</span></span>

<span data-ttu-id="12f0c-103">В этом примере показан способ применения объекта [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) для извлечения данных, хранящихся в папке в виде скрытого сообщения определенного класса.</span><span class="sxs-lookup"><span data-stu-id="12f0c-103">This example shows how to use the [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\)) object to retrieve data that is stored as a hidden message of a specific message class in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="12f0c-104">Пример</span><span class="sxs-lookup"><span data-stu-id="12f0c-104">Example</span></span>

<span data-ttu-id="12f0c-p101">Объект **StorageItem** обычно используется для скрытия данных решения, которые не удается отобразить программным методом. В среде Exchange объект **StorageItem** служит для роуминга параметров решения и обеспечения доступности этих настроек в Интернете и в автономном режиме. Настраиваемый класс сообщений можно присвоить объекту **StorageItem**, либо идентифицировать объект по теме.</span><span class="sxs-lookup"><span data-stu-id="12f0c-p101">The **StorageItem** object is typically used to hide solution-specific data that cannot be displayed programmatically. In an Exchange environment, the **StorageItem** object is used to roam solution settings and ensure that these settings are available online and offline. You can assign a custom message class to the **StorageItem** object, or identify the object by subject.</span></span>

<span data-ttu-id="12f0c-108">В следующем примере кода извлекаются данные XML, сохраненные в виде скрытого сообщения класса IPM.Configuration.WorkHours в папке "Календарь".</span><span class="sxs-lookup"><span data-stu-id="12f0c-108">The following code sample retrieves the XML data that is stored as a hidden message in the Calendar folder with the message class equal to IPM.Configuration.WorkHours.</span></span>

<span data-ttu-id="12f0c-p102">Объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) возвращает XML в виде объекта, содержащего поток байт, а не строковое представление XML. Для преобразования потока байт в строку в примере кода применяется **System.Text.Encoding.Ascii.GetString**.</span><span class="sxs-lookup"><span data-stu-id="12f0c-p102">The [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object returns the XML as an object that contains a byte stream rather than a string representation of the XML. The code sample uses **System.Text.Encoding.Ascii.GetString** to convert the byte stream to a string.</span></span>

<span data-ttu-id="12f0c-111">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="12f0c-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="12f0c-112">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="12f0c-112">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="12f0c-113">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="12f0c-113">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Function GetWorkHoursXML() As String
    Try
        Dim storage As Outlook.StorageItem = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage( _
            "IPM.Configuration.WorkHours", _
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass)
        Dim pa As Outlook.PropertyAccessor = storage.PropertyAccessor
        ' PropertyAccessor will return a byte array for this property
        Dim rawXmlBytes As Byte() = CType(pa.GetProperty( _
            "https://schemas.microsoft.com/mapi/proptag/0x7C080102"), _
            Byte())
        ' Use Encoding to convert the array to a string
        Return System.Text.Encoding.ASCII.GetString(rawXmlBytes)
    Catch
        Return String.Empty
    End Try
End Function
```

```csharp
private string GetWorkHoursXML()
{
    try
    {
        Outlook.StorageItem storage =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderCalendar).GetStorage(
            "IPM.Configuration.WorkHours",
            Outlook.OlStorageIdentifierType.olIdentifyByMessageClass);
        Outlook.PropertyAccessor pa = storage.PropertyAccessor;
        // PropertyAccessor will return a byte array for this property
        byte[] rawXmlBytes = (byte[])pa.GetProperty(
            "https://schemas.microsoft.com/mapi/proptag/0x7C080102");
        // Use Encoding to convert the array to a string
        return System.Text.Encoding.ASCII.GetString(rawXmlBytes);
    }
    catch
    {
        return string.Empty;
    }
}
```


## <a name="see-also"></a><span data-ttu-id="12f0c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="12f0c-114">See also</span></span>

- [<span data-ttu-id="12f0c-115">Папки</span><span class="sxs-lookup"><span data-stu-id="12f0c-115">Folders</span></span>](folders.md)

