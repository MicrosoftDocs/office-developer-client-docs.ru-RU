---
title: Отображение общего календаря получателя
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9230a63af66e8143a7da488ce41dadafe359429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356429"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a><span data-ttu-id="67ecc-102">Отображение общего календаря получателя</span><span class="sxs-lookup"><span data-stu-id="67ecc-102">Display a shared calendar of a recipient</span></span>

<span data-ttu-id="67ecc-103">В этом примере показано, как отобразить общий календарь получателя c помощью методов [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) и [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="67ecc-103">This example shows how to display a recipient's shared calendar by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) and [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) methods.</span></span>

## <a name="example"></a><span data-ttu-id="67ecc-104">Пример</span><span class="sxs-lookup"><span data-stu-id="67ecc-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="67ecc-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="67ecc-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="67ecc-p101">Отправляемые элементы, такие как объекты [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , всегда предоставляют свойство [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) , которое, в свою очередь, позволяет получать доступ к коллекции [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) для отправляемого элемента. Чтобы создать объект [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) , который не связан с коллекцией **Recipients** элемента, используется метод [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Затем этот несвязанный объект **Recipient** передается в метод [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) , который возвращает общую папку Exchange. Далее можно открыть общую папку Exchange и отобразить эту папку в окне проводника. GetSharedDefaultFolder используется при делегировании в Exchange, когда делегат обладает разрешением на доступ к папке представителя. Перед передачей объекта **Recipient** в метод GetSharedDefaultFolder необходимо разрешить его. Чтобы разрешить объект **Recipient**, вызовите его метод [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="67ecc-p101">Sendable items such as [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects always expose the [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) property which, in turn, enables you to access the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the sendable item. To create a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object that is not bound to the **Recipients** collection of an item, use the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object. Then pass this unbound **Recipient** object to the [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) method, which returns a shared Exchange folder. You can then open the shared Exchange folder and display that folder in an explorer window. GetSharedDefaultFolder is used in Exchange delegate scenarios where the delegate has permission to access the folder of the delegator. Before you pass the **Recipient** object to the GetSharedDefaultFolder method, you must resolve it. To resolve a **Recipient** object, call its [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) method.</span></span>

<span data-ttu-id="67ecc-p102">В следующем примере кода DisplayManagerCalendar открывает и отображает папку "Календарь" руководителя текущего пользователя, вызывая **CreateRecipient** и **GetSharedDefaultFolder**. Если у пользователя отсутствует разрешение на открытие папки "Календарь" руководителя или в случае ошибки, появляется диалоговое окно оповещения. </span><span class="sxs-lookup"><span data-stu-id="67ecc-p102">In the following code example, DisplayManagerCalendar opens and displays the Calendar folder of the current user’s manager by calling **CreateRecipient** and **GetSharedDefaultFolder**. An alert dialog box is displayed if the user does not have permission to open the manager’s Calendar folder or an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="67ecc-115">При создании объекта **Recipient** с помощью метода **CreateRecipient** объекта **Namespace** или метода [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) коллекции **Recipients** необходимо предоставить имя получателя.</span><span class="sxs-lookup"><span data-stu-id="67ecc-115">When you create a **Recipient** object by using the **CreateRecipient** method of the **Namespace** object or the [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) method of the **Recipients** collection, you must provide a recipient name.</span></span> <span data-ttu-id="67ecc-116">Затем объект **Recipient** разрешается по этому имени.</span><span class="sxs-lookup"><span data-stu-id="67ecc-116">The **Recipient** is then resolved against this name.</span></span> <span data-ttu-id="67ecc-117">Имя получателя может быть представлено в любом из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="67ecc-117">A recipient name can take any of the following formats:</span></span>
> - <span data-ttu-id="67ecc-118">Имя</span><span class="sxs-lookup"><span data-stu-id="67ecc-118">Display name</span></span>
> - <span data-ttu-id="67ecc-119">псевдоним;</span><span class="sxs-lookup"><span data-stu-id="67ecc-119">Alias</span></span>
> - <span data-ttu-id="67ecc-120">SMTP-адрес.</span><span class="sxs-lookup"><span data-stu-id="67ecc-120">Simple Mail Transfer Protocol (SMTP) address</span></span>

<span data-ttu-id="67ecc-121">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="67ecc-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="67ecc-122">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="67ecc-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="67ecc-123">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="67ecc-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="67ecc-124">См. также</span><span class="sxs-lookup"><span data-stu-id="67ecc-124">See also</span></span>

- [<span data-ttu-id="67ecc-125">Calendar</span><span class="sxs-lookup"><span data-stu-id="67ecc-125">Calendar</span></span>](calendar.md)

