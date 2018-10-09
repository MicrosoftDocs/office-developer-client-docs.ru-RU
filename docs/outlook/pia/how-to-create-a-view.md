---
title: Создание представления
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e9a68fc6220e1439e517b3d4e7e2ecb30b919ee0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406031"
---
# <a name="create-a-view"></a><span data-ttu-id="0e492-102">Создание представления</span><span class="sxs-lookup"><span data-stu-id="0e492-102">Create a map view programmatically</span></span>

<span data-ttu-id="0e492-103">В этом примере показано использование метода [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) коллекции [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) для создания представления для объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0e492-103">Uses the [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) method of the [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) collection to create a view for a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object.</span></span>

## <a name="example"></a><span data-ttu-id="0e492-104">Пример</span><span class="sxs-lookup"><span data-stu-id="0e492-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0e492-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0e492-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="0e492-p101">Можно создавать настраиваемые представления, которые позволяют упорядочивать, группировать и просматривать данные всех типов в области просмотра окна проводника Outlook. Кроме того, можно программным образом настраивать встроенные представления. В следующей таблице приведены объекты, олицетворяющие представления Outlook. </span><span class="sxs-lookup"><span data-stu-id="0e492-p101">You can create customizable views that allow you to sort, group, and view data of all different types within the View Pane of the Outlook explorer window. You can also customize built-in views programmatically. The following table lists objects that represent Outlook views.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e492-109">Имя объекта</span><span class="sxs-lookup"><span data-stu-id="0e492-109">Object Name</span></span></p></th>
<th><p><span data-ttu-id="0e492-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e492-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e492-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></span><span class="sxs-lookup"><span data-stu-id="0e492-111"><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="0e492-112">Данные отображаются как ряд образов электронной визитной карточки.</span><span class="sxs-lookup"><span data-stu-id="0e492-112">Data is viewed as a series of Electronic Business Card images.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e492-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span><span class="sxs-lookup"><span data-stu-id="0e492-113"><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></span></span></p></td>
<td><p><span data-ttu-id="0e492-114">Данные отображаются в формате календаря.</span><span class="sxs-lookup"><span data-stu-id="0e492-114">Data is viewed in a calendar format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e492-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></span><span class="sxs-lookup"><span data-stu-id="0e492-115"><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView Object</a></span></span></p></td>
<td><p><span data-ttu-id="0e492-116">Данные отображаются как ряд карточек.</span><span class="sxs-lookup"><span data-stu-id="0e492-116">Data is viewed in a series of cards.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e492-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></span><span class="sxs-lookup"><span data-stu-id="0e492-117"><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView Object</a></span></span></p></td>
<td><p><span data-ttu-id="0e492-118">Данные отображаются как значки папок Windows или значки проводника.</span><span class="sxs-lookup"><span data-stu-id="0e492-118">Data is viewed as Windows folder icons or explorer icons.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e492-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></span><span class="sxs-lookup"><span data-stu-id="0e492-119"><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView Object</a></span></span></p></td>
<td><p><span data-ttu-id="0e492-120">Данные отображаются в простой таблице на основе полей.</span><span class="sxs-lookup"><span data-stu-id="0e492-120">Data is viewed in a simple field-based table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e492-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></span><span class="sxs-lookup"><span data-stu-id="0e492-121"><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView Object</a></span></span></p></td>
<td><p><span data-ttu-id="0e492-122">Данные отображаются на настраиваемой линейной временной шкале.</span><span class="sxs-lookup"><span data-stu-id="0e492-122">Data is viewed in a customizable linear time line.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e492-123">Доступ к общим для всех представлений свойствам и методам можно получить с помощью объекта [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0e492-123">You can access properties and methods that are common to all views by using the [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)) object.</span></span> <span data-ttu-id="0e492-124">Однако для доступа к определенным свойствам, которые не являются общими для всех представлений, необходимо привести объект **View** к производному объекту **View**, которому принадлежит нужное свойство.</span><span class="sxs-lookup"><span data-stu-id="0e492-124">However, to access certain properties that are not common to all views, you must cast the **View** object to a derived **View** object that the property you want to access belongs to.</span></span> <span data-ttu-id="0e492-125">Например, чтобы получить доступ к свойству [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) объекта **Cardview** приведите объект **View** к объекту **Cardview**.</span><span class="sxs-lookup"><span data-stu-id="0e492-125">For example, to access the [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) property of the **Cardview** object, cast the **View** object to the **Cardview** object.</span></span> <span data-ttu-id="0e492-126">Если нужно определить, какой тип представления отображается определенным объектом **View**, используйте свойство [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0e492-126">If you want to determine which type of view is represented by a particular **View** object, use the [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)) property.</span></span>

<span data-ttu-id="0e492-127">Чтобы создать новое представление, используйте метод **Add** коллекции **Views** для объекта **Folder**.</span><span class="sxs-lookup"><span data-stu-id="0e492-127">To create a new view, use the **Add** method of the **Views** collection for a **Folder** object.</span></span> <span data-ttu-id="0e492-128">Затем установите параметры отображения для представления во время создания или в любой момент после создания представлении.</span><span class="sxs-lookup"><span data-stu-id="0e492-128">Then set the visibility for the view either at the time of creation, or at any time after the view is created.</span></span> <span data-ttu-id="0e492-129">Чтобы установить параметры отображения для представления во время создания, задайте константу [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) в параметре *SaveOption* метода **Add**.</span><span class="sxs-lookup"><span data-stu-id="0e492-129">To set the visibility for the view at the time of creation, specify an [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) constant in the *SaveOption* parameter of the **Add** method.</span></span> <span data-ttu-id="0e492-130">Чтобы установить параметры отображения в любой момент после создания представления, задайте константу **OlViewSaveOption** для свойства [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) объекта **View**.</span><span class="sxs-lookup"><span data-stu-id="0e492-130">To set the visibility at any time after the view is created, specify an **OlViewSaveOption** constant for the [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) property of the **View** object.</span></span> 

<span data-ttu-id="0e492-131">Добавление нового представления создает событие [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) в коллекции **Views**.</span><span class="sxs-lookup"><span data-stu-id="0e492-131">Adding a new view raises the [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) event of the **Views** collection.</span></span> <span data-ttu-id="0e492-132">После создания представления настройте его программным путем, приведя объект **View** к одному из производных объектов и сделав необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="0e492-132">Once the view is created, customize the view programmatically by casting the **View** object to one of the derived objects and then making necessary changes.</span></span> <span data-ttu-id="0e492-133">Используйте метод **Save** производного объекта **View** или объекта **View**, чтобы сохранить изменения в представлении.</span><span class="sxs-lookup"><span data-stu-id="0e492-133">Use the **Save** method of the derived **View** object or the **View** object to save any changes to the view.</span></span> <span data-ttu-id="0e492-134">В конце используйте метод **Apply** производного объекта **View** или объекта **View**, чтобы применить представление к текущему объекту [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0e492-134">Finally, use the **Apply** method of the derived **View** object or the **View** object to apply the view to the current [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="0e492-135">При этом создается событие [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) объекта **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="0e492-135">This raises the [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) event of the **Explorer** object.</span></span>

<span data-ttu-id="0e492-136">В представленном ниже примере кода CreateMeetingRequestsView добавляет новое представление с именем "Приглашения на собрания" в папку "Входящие" пользователя путем приведения объекта **View** к объекту **TableView**.</span><span class="sxs-lookup"><span data-stu-id="0e492-136">In the following code example, CreateMeetingRequestsView adds a new view named “Meeting Requests” to the user’s Inbox by casting the **View** object to a **TableView** object.</span></span> <span data-ttu-id="0e492-137">Затем CreateMeetingRequestsView вызывает метод **Add** объекта **Views** с параметром *Name*, заданным как "Приглашения на собрания", и параметром *ViewType*, заданным как **olTableView**.</span><span class="sxs-lookup"><span data-stu-id="0e492-137">CreateMeetingRequestsView then calls the **Add** method of the **Views** object with the *Name* parameter set to “Meeting Requests” and the *ViewType* parameter set to **olTableView**.</span></span> <span data-ttu-id="0e492-138">Свойство [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) объекта **TableView** задано соответствующим строке DASL, что приводит к отображению представления только в том случае, если в классе сообщений для элемента имеются элементы, содержащие "IPM.Schedule".</span><span class="sxs-lookup"><span data-stu-id="0e492-138">The [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) property of the **TableView** object is set to a DAV Searching and Locating (DASL) string that causes the view to display only when there are items that contain “IPM.Schedule” in the message class for the item.</span></span> <span data-ttu-id="0e492-139">Новое представление затем сохраняется и применяется.</span><span class="sxs-lookup"><span data-stu-id="0e492-139">The new view is then saved and applied.</span></span>

<span data-ttu-id="0e492-140">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0e492-140">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0e492-141">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="0e492-141">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0e492-142">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="0e492-142">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateMeetingRequestsView()
{
    const string PR_MESSAGE_CLASS =
        "https://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.Views views =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Views;
    Outlook.TableView tableView = (Outlook.TableView)
        views.Add("Meeting Requests",
        Outlook.OlViewType.olTableView,
        Outlook.OlViewSaveOption.olViewSaveOptionThisFolderEveryone);
    tableView.Filter = "\"" + PR_MESSAGE_CLASS + "\"" +
        " like 'IPM.Schedule%'";
    tableView.Save();
    tableView.Apply();
}
```

## <a name="see-also"></a><span data-ttu-id="0e492-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0e492-143">See also</span></span>

- [<span data-ttu-id="0e492-144">Представления</span><span class="sxs-lookup"><span data-stu-id="0e492-144">Views</span></span>](views.md)

