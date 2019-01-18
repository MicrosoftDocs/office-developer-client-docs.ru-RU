---
title: Создание представления
TOCTitle: Create a view
ms:assetid: 2f8ad187-1030-420a-bc74-c327e3521550
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424468(v=office.15)
ms:contentKeyID: 55119902
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c91f43001d6c56ad3b4c316aede9845a5e0a0064
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721873"
---
# <a name="create-a-view"></a>Создание представления

В этом примере показано использование метода [Add(String, OlViewType, OlViewSaveOption)](https://msdn.microsoft.com/library/bb643986\(v=office.15\)) коллекции [Views](https://msdn.microsoft.com/library/bb644226\(v=office.15\)) для создания представления для объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Можно создавать настраиваемые представления, которые позволяют упорядочивать, группировать и просматривать данные всех типов в области просмотра окна проводника Outlook. Кроме того, можно программным образом настраивать встроенные представления. В следующей таблице приведены объекты, олицетворяющие представления Outlook. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя объекта</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb646315(v=office.15)">BusinessCardView</a></p></td>
<td><p>Данные отображаются как ряд образов электронной визитной карточки.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb622874(v=office.15)">CalendarView</a></p></td>
<td><p>Данные отображаются в формате календаря.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb609216(v=office.15)">CardView</a></p></td>
<td><p>Данные отображаются как ряд карточек.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb612031(v=office.15)">IconView</a></p></td>
<td><p>Данные отображаются как значки папок Windows или значки проводника.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/bb608854(v=office.15)">TableView</a></p></td>
<td><p>Данные отображаются в простой таблице на основе полей.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/bb609455(v=office.15)">TimelineView</a></p></td>
<td><p>Данные отображаются на настраиваемой линейной временной шкале.</p></td>
</tr>
</tbody>
</table>


Доступ к общим для всех представлений свойствам и методам можно получить с помощью объекта [View](https://msdn.microsoft.com/library/bb647396\(v=office.15\)). Однако для доступа к определенным свойствам, которые не являются общими для всех представлений, необходимо привести объект **View** к производному объекту **View**, которому принадлежит нужное свойство. Например, чтобы получить доступ к свойству [HeadingsFont](https://msdn.microsoft.com/library/bb612522\(v=office.15\)) объекта **Cardview** приведите объект **View** к объекту **Cardview**. Если нужно определить, какой тип представления отображается определенным объектом **View**, используйте свойство [ViewType](https://msdn.microsoft.com/library/bb623693\(v=office.15\)).

Чтобы создать новое представление, используйте метод **Add** коллекции **Views** для объекта **Folder**. Затем установите параметры отображения для представления во время создания или в любой момент после создания представлении. Чтобы установить параметры отображения для представления во время создания, задайте константу [OlViewSaveOption](https://msdn.microsoft.com/library/bb647502\(v=office.15\)) в параметре *SaveOption* метода **Add**. Чтобы установить параметры отображения в любой момент после создания представления, задайте константу **OlViewSaveOption** для свойства [SaveOption](https://msdn.microsoft.com/library/bb646426\(v=office.15\)) объекта **View**. 

Добавление нового представления создает событие [ViewAdd](https://msdn.microsoft.com/library/bb647550\(v=office.15\)) в коллекции **Views**. После создания представления настройте его программным путем, приведя объект **View** к одному из производных объектов и сделав необходимые изменения. Используйте метод **Save** производного объекта **View** или объекта **View**, чтобы сохранить изменения в представлении. В конце используйте метод **Apply** производного объекта **View** или объекта **View**, чтобы применить представление к текущему объекту [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)). При этом создается событие [ViewSwitch](https://msdn.microsoft.com/library/bb644066\(v=office.15\)) объекта **Explorer**.

В представленном ниже примере кода CreateMeetingRequestsView добавляет новое представление с именем "Приглашения на собрания" в папку "Входящие" пользователя путем приведения объекта **View** к объекту **TableView**. Затем CreateMeetingRequestsView вызывает метод **Add** объекта **Views** с параметром *Name*, заданным как "Приглашения на собрания", и параметром *ViewType*, заданным как **olTableView**. Свойство [Filter](https://msdn.microsoft.com/library/bb610296\(v=office.15\)) объекта **TableView** задано соответствующим строке DASL, что приводит к отображению представления только в том случае, если в классе сообщений для элемента имеются элементы, содержащие "IPM.Schedule". Новое представление затем сохраняется и применяется.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Представления](views.md)

