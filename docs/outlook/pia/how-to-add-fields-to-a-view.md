---
title: Добавление полей в представление
TOCTitle: Add fields to a view
ms:assetid: ea371f27-ea65-47ef-ae44-ef843a78ab6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424481(v=office.15)
ms:contentKeyID: 55119934
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4b850bf87be4024152ee808624ad93836b904897
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359698"
---
# <a name="add-fields-to-a-view"></a>Добавление полей в представление

В этом примере показано, как с помощью метода [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) коллекции [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) добавить поля в представление.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").


Чтобы определить, какие свойства элемента Outlook будут отображаться в представлении, добавьте одно или несколько свойств в коллекцию **ViewFields** только для объектов [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) и [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) . Для других производных объектов **View**, таких как [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) и [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)), следует использовать другие методы, позволяющие определить отображаемые в представлении свойства элемента Outlook. Например, поля, отображаемые для объекта **BusinessCardView**, определяются макетом электронной визитной карточки (EBC), связанным с каждым элементом Outlook.

Чтобы получить коллекцию **ViewFields** для представления, используйте свойство **ViewFields** связанного объекта **View** (например, объекты **CardView** или **TableView**). Метод **Add** коллекции **ViewFields** обеспечивает создание объекта [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) , представляющего свойство элемента Outlook, которое будет отображаться в представлении. Объект **ViewField** не только определяет отображаемые в представлении свойства элемента Outlook, но также описывает способ отображения значений соответствующего свойства. Чтобы изменить способ отображения отдельных свойств столбцов в представлении, измените значение свойства [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) объекта **ViewField**.

В следующем примере кода в процедуре ModifyMeetingRequestsView получается объект **TableView**, который определяет все представления приглашений на собрание из папки "Входящие" пользователя. После этого с помощью метода **Add** в объект **ViewFields**, соответствующий объекту **TableView**, добавляются поля начала и окончания. Кроме того, название поля "От кого" изменяется на "Организатор". После этого в процедуре ModifyMeetingRequestsView сохраняется измененный объект **TableView**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ModifyMeetingRequestsView()
{
    Outlook.TableView tableView = null;
    Outlook.ViewField startField = null;
    Outlook.ViewField endField = null;
    Outlook.ViewField fromField = null;
    try
    {
        tableView =
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            .Views["Meeting Requests"] as Outlook.TableView;
    }
    catch { }
    if (tableView != null)
    {
        try
        {
            startField = tableView.ViewFields["Start"];
        }
        catch{}
        if (startField == null)
        {
            startField = tableView.ViewFields.Add("Start");
        }
        try
        {
            endField = tableView.ViewFields["End"];
        }
        catch{}
        if (endField == null)
        {
            endField = tableView.ViewFields.Add("End");
        }
        try
        {
            fromField = tableView.ViewFields["From"];
        }
        catch{}
        if (fromField != null)
        {
            fromField.ColumnFormat.Label = "Organized By";
        }
        try
        {
            tableView.Save();
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Представления](views.md)

