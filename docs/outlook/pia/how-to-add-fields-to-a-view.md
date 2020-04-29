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
# <a name="add-fields-to-a-view"></a><span data-ttu-id="7a13d-102">Добавление полей в представление</span><span class="sxs-lookup"><span data-stu-id="7a13d-102">Add fields to a view</span></span>

<span data-ttu-id="7a13d-103">В этом примере показано, как с помощью метода [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) коллекции [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) добавить поля в представление.</span><span class="sxs-lookup"><span data-stu-id="7a13d-103">This example shows how to customize a view by using the [Add(String)](https://msdn.microsoft.com/library/bb646040\(v=office.15\)) method of the [ViewFields](https://msdn.microsoft.com/library/bb645950\(v=office.15\)) collection to add fields to a view.</span></span>

## <a name="example"></a><span data-ttu-id="7a13d-104">Пример</span><span class="sxs-lookup"><span data-stu-id="7a13d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="7a13d-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="7a13d-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="7a13d-106">Чтобы определить, какие свойства элемента Outlook будут отображаться в представлении, добавьте одно или несколько свойств в коллекцию **ViewFields** только для объектов [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) и [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="7a13d-106">You can specify which Outlook item properties are displayed in a view by adding one or more properties to the **ViewFields** collection for only the [CardView](https://msdn.microsoft.com/library/bb609216\(v=office.15\)) and [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) objects.</span></span> <span data-ttu-id="7a13d-107">Для других производных объектов **View**, таких как [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)) и [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)), следует использовать другие методы, позволяющие определить отображаемые в представлении свойства элемента Outlook.</span><span class="sxs-lookup"><span data-stu-id="7a13d-107">For other derived **View** objects such as [BusinessCardView](https://msdn.microsoft.com/library/bb646315\(v=office.15\)), [CalendarView](https://msdn.microsoft.com/library/bb622874\(v=office.15\)), [IconView](https://msdn.microsoft.com/library/bb612031\(v=office.15\)), and [TimelineView](https://msdn.microsoft.com/library/bb609455\(v=office.15\)) objects, use other methods of determining which Outlook item properties are displayed within the view.</span></span> <span data-ttu-id="7a13d-108">Например, поля, отображаемые для объекта **BusinessCardView**, определяются макетом электронной визитной карточки (EBC), связанным с каждым элементом Outlook.</span><span class="sxs-lookup"><span data-stu-id="7a13d-108">For example, the fields displayed for the **BusinessCardView** object are determined by the electronic business card (EBC) layout associated with each displayed Outlook item.</span></span>

<span data-ttu-id="7a13d-p102">Чтобы получить коллекцию **ViewFields** для представления, используйте свойство **ViewFields** связанного объекта **View** (например, объекты **CardView** или **TableView**). Метод **Add** коллекции **ViewFields** обеспечивает создание объекта [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) , представляющего свойство элемента Outlook, которое будет отображаться в представлении. Объект **ViewField** не только определяет отображаемые в представлении свойства элемента Outlook, но также описывает способ отображения значений соответствующего свойства. Чтобы изменить способ отображения отдельных свойств столбцов в представлении, измените значение свойства [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) объекта **ViewField**.</span><span class="sxs-lookup"><span data-stu-id="7a13d-p102">To get the **ViewFields** collection for a view, use the **ViewFields** property of the associated **View** object (for example, the **CardView** or **TableView** objects). The **Add** method of the **ViewFields** collection is used to create a [ViewField](https://msdn.microsoft.com/library/bb610583\(v=office.15\)) object that represents the Outlook item property to be displayed in the view. A **ViewField** object not only identifies an Outlook item property to display within the view, but it also describes how the values for that property should be displayed. You can change how individual column properties are displayed in a view by modifying the [ColumnFormat](https://msdn.microsoft.com/library/bb646462\(v=office.15\)) property of the **ViewField** object.</span></span>

<span data-ttu-id="7a13d-p103">В следующем примере кода в процедуре ModifyMeetingRequestsView получается объект **TableView**, который определяет все представления приглашений на собрание из папки "Входящие" пользователя. После этого с помощью метода **Add** в объект **ViewFields**, соответствующий объекту **TableView**, добавляются поля начала и окончания. Кроме того, название поля "От кого" изменяется на "Организатор". После этого в процедуре ModifyMeetingRequestsView сохраняется измененный объект **TableView**.</span><span class="sxs-lookup"><span data-stu-id="7a13d-p103">In the following code example, ModifyMeetingRequestsView gets the **TableView** object that represents all the views from the user’s Inbox that are “Meeting Requests” views. The example then uses the **Add** method to add the “Start” and “End” fields to the **ViewFields** object that corresponds to the **TableView** object. It also changes the label for the “From” field to “Organized By”. ModifyMeetingRequestsView then saves the modified **TableView** object.</span></span>

<span data-ttu-id="7a13d-117">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="7a13d-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7a13d-118">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="7a13d-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7a13d-119">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="7a13d-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="7a13d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7a13d-120">See also</span></span>

- [<span data-ttu-id="7a13d-121">Представления</span><span class="sxs-lookup"><span data-stu-id="7a13d-121">Views</span></span>](views.md)

