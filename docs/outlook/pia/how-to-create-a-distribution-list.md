---
title: Создание списка рассылки
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f37338209ea468d0143dfd1063c3c57216bc13ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359656"
---
# <a name="create-a-distribution-list"></a><span data-ttu-id="abdc9-102">Создание списка рассылки</span><span class="sxs-lookup"><span data-stu-id="abdc9-102">Create a distribution list</span></span>

<span data-ttu-id="abdc9-103">В этом примере показано, как создать список рассылки и отобразить его пользователю.</span><span class="sxs-lookup"><span data-stu-id="abdc9-103">This example shows how to create a distribution list and display it to the user.</span></span>

## <a name="example"></a><span data-ttu-id="abdc9-104">Пример</span><span class="sxs-lookup"><span data-stu-id="abdc9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="abdc9-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="abdc9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="abdc9-106">В следующем примере кода CreateDistributionList создает список рассылки путем вызова метода [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) для создания объекта [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="abdc9-106">In the following code example, CreateDistributionList creates a distribution list by calling the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method to create a [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="abdc9-107">Затем создается объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) и вызывается метод [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) для поиска всех контактов в выбранной по умолчанию папке "Контакты", свойство которой [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) имеет значение "Top Customer" (лучший клиент), а значение свойства [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) не является пустым.</span><span class="sxs-lookup"><span data-stu-id="abdc9-107">Next it creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and calls the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) method to find all contacts in the default Contacts folder for which the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property value is “Top Customer” and the [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) property value is not empty.</span></span> <span data-ttu-id="abdc9-108">После определения всех контактов имя **Email1Address** добавляется в качестве столбца в объект **Table**.</span><span class="sxs-lookup"><span data-stu-id="abdc9-108">Once all contacts are identified, the **Email1Address** name is added as a column to the **Table**.</span></span> <span data-ttu-id="abdc9-109">Затем с помощью CreateDistributionList создается объект [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) путем применения метода [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) из объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="abdc9-109">CreateDistributionList then creates a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method from the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="abdc9-110">Наконец, CreateDistributionList показывает пользователю список рассылки "Top Customers" (лучшие клиенты).</span><span class="sxs-lookup"><span data-stu-id="abdc9-110">CreateDistributionList finally displays the “Top Customers” distribution list to the user.</span></span>

> [!NOTE] 
> <span data-ttu-id="abdc9-111">Необходимо передать разрешенный объект **Recipient** в качестве параметра для метода [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) объекта [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="abdc9-111">You must pass a resolved **Recipient** object as a parameter to the [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) method of the [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)) object.</span></span> <span data-ttu-id="abdc9-112">Чтобы разрешить объект **Recipient**, используйте метод [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="abdc9-112">To resolve a **Recipient** object, use the [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) method.</span></span>

<span data-ttu-id="abdc9-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="abdc9-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="abdc9-114">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="abdc9-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="abdc9-115">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="abdc9-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="abdc9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="abdc9-116">See also</span></span>

- [<span data-ttu-id="abdc9-117">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="abdc9-117">Exchange users</span></span>](exchange-users.md)

