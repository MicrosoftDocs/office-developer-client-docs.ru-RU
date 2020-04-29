---
title: Создание настраиваемого элемента Contact
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4261fffef0934e01cbfbcc7068377cc392af178c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361056"
---
# <a name="create-a-custom-contact-item"></a><span data-ttu-id="b2067-102">Создание настраиваемого элемента контакта</span><span class="sxs-lookup"><span data-stu-id="b2067-102">Create a custom Contact item</span></span>

<span data-ttu-id="b2067-103">В этом примере показано, как создать настраиваемый элемент контакта и настроить предопределенные и пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="b2067-103">This example shows how to create a custom contact item and set both predefined and user-defined properties.</span></span>

## <a name="example"></a><span data-ttu-id="b2067-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b2067-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b2067-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="b2067-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="b2067-106">Объект [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) представляет контакт в папке контактов и имеет более 100 встроенных свойств, таких как [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) и [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b2067-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object represents a contact in the Contacts folder, and has more than 100 built-in properties such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) and [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span></span> <span data-ttu-id="b2067-107">Иногда встроенных свойств недостаточно и нужно добавить настраиваемые свойства, что можно сделать с помощью коллекции [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b2067-107">Sometimes, the built-in properties are not sufficient and you need to add custom properties, which you can do by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span>

<span data-ttu-id="b2067-108">В представленном ниже примере кода CreateCustomItem создает настраиваемый объект **ContactItem**, называет его "Shoe Store" и вызывает метод [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)), чтобы добавить его в папку с именем "Shoe Store".</span><span class="sxs-lookup"><span data-stu-id="b2067-108">In the following code example, CreateCustomItem creates a custom **ContactItem** object, names it "Shoe Store", and calls the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add it to a folder named "Shoe Store".</span></span> <span data-ttu-id="b2067-109">CreateCustomItem сначала получает папку "Shoe Store" с помощью метода [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b2067-109">CreateCustomItem first gets the "Shoe Store" folder by using the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method.</span></span> <span data-ttu-id="b2067-110">Папка "Shoe Store" вложена в папку контактов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b2067-110">The "Shoe Store" folder is a subfolder of the default Contacts folder.</span></span> <span data-ttu-id="b2067-111">Затем CreateCustomItem устанавливает свойства **FirstName** и **LastName** и создает пользовательское свойство ("Shoe Size") с помощью коллекции **UserProperties**.</span><span class="sxs-lookup"><span data-stu-id="b2067-111">CreateCustomItem then sets the **FirstName** and **LastName** properties, and creates a user-defined property ("Shoe Size") by using the **UserProperties** collection.</span></span>

<span data-ttu-id="b2067-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b2067-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b2067-113">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="b2067-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b2067-114">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="b2067-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="b2067-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b2067-115">See also</span></span>

- [<span data-ttu-id="b2067-116">Контакты</span><span class="sxs-lookup"><span data-stu-id="b2067-116">Contacts</span></span>](contacts.md)

