---
title: Создание элемента контакта
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 814885b209020fb37c84df2e88f04bb32ec5cd6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407130"
---
# <a name="create-a-contact-item"></a><span data-ttu-id="f6f4a-102">Создание элемента контакта</span><span class="sxs-lookup"><span data-stu-id="f6f4a-102">Create a Contact item</span></span>

<span data-ttu-id="f6f4a-103">В этом примере показано, как создать элемент контакта и настроить различные свойства для контакта.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-103">This example shows how to create a contact item and set various properties for the contact.</span></span>

## <a name="example"></a><span data-ttu-id="f6f4a-104">Пример</span><span class="sxs-lookup"><span data-stu-id="f6f4a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f6f4a-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="f6f4a-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="f6f4a-106">Объект Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) имеет более 100 встроенных свойств (например, [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) и [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\))).</span><span class="sxs-lookup"><span data-stu-id="f6f4a-106">A Microsoft Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object has more than 100 built-in properties such as [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)) , [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) , [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) , and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) .</span></span> <span data-ttu-id="f6f4a-107">Если встроенные свойства недоступны, можно добавить настраиваемые свойства с помощью коллекции [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="f6f4a-107">You can add custom properties, if a built-in property is not available, by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span> <span data-ttu-id="f6f4a-108">После создания объекта **ContactItem** можно настроить его свойства.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-108">Once you create a **ContactItem**, you can set its properties.</span></span>

<span data-ttu-id="f6f4a-109">В следующем примере кода CreateContactExample создает объект **ContactItem** и задает для него широко используемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-109">In the following code example,   creates a ContactItem and sets commonly used properties for that object.</span></span> <span data-ttu-id="f6f4a-110">Затем вызывается метод [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) для объекта **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-110">It then calls the [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) method on the **ContactItem** object.</span></span> <span data-ttu-id="f6f4a-111">Метод **ShowCheckPhoneDialog** позволяет пользователю сопоставлять номер телефона с учетом местных правил набора номера.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-111">The **ShowCheckPhoneDialog** method allows the user to resolve a phone number based on local dialing conventions.</span></span>

<span data-ttu-id="f6f4a-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f6f4a-113">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f6f4a-114">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="f6f4a-114">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateContactExample()
{
    Outlook.ContactItem contact = Application.CreateItem(
        Outlook.OlItemType.olContactItem) as Outlook.ContactItem;
    contact.FirstName = "Mellissa";
    contact.LastName = "MacBeth";
    contact.JobTitle = "Account Representative";
    contact.CompanyName = "Contoso Ltd.";
    contact.OfficeLocation = "36/2529";
    contact.BusinessTelephoneNumber = "4255551212 x432";
    contact.WebPage = "https://www.contoso.com";
    contact.BusinessAddressStreet = "1 Microsoft Way";
    contact.BusinessAddressCity = "Redmond";
    contact.BusinessAddressState = "WA";
    contact.BusinessAddressPostalCode = "98052";
    contact.BusinessAddressCountry =
        "United States of America";
    contact.Email1Address = "melissa@contoso.com";
    contact.Email1AddressType = "SMTP";
    contact.Email1DisplayName =
        "Melissa MacBeth (mellissa@contoso.com)";
    contact.Display(false);
    contact.ShowCheckPhoneDialog(
        Outlook.OlContactPhoneNumber.
        olContactPhoneBusiness);
}
```

## <a name="see-also"></a><span data-ttu-id="f6f4a-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f6f4a-115">See also</span></span>

- [<span data-ttu-id="f6f4a-116">Контакты</span><span class="sxs-lookup"><span data-stu-id="f6f4a-116">Contacts</span></span>](contacts.md)

