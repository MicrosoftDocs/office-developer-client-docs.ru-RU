---
title: Изменение макета электронной визитной карточки
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0b95621df2e021f52587d5a40d0de43e5505b80c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406437"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a><span data-ttu-id="4926f-102">Изменение макета электронной визитной карточки</span><span class="sxs-lookup"><span data-stu-id="4926f-102">Modify the layout of an electronic business card</span></span>

<span data-ttu-id="4926f-103">В этом примере показано, как изменить макет электронной визитной карточки с помощью свойства [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) интерфейса [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4926f-103">This example shows how to modify the layout of an Electronic Business Card by using the [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) property of the [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) interface.</span></span>

## <a name="example"></a><span data-ttu-id="4926f-104">Пример</span><span class="sxs-lookup"><span data-stu-id="4926f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="4926f-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="4926f-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="4926f-106">Электронная визитная карточка  это представление контакта, содержащее конкретную информацию о нем.</span><span class="sxs-lookup"><span data-stu-id="4926f-106">An Electronic Business Card provides a contact view that captures specific information from that contact.</span></span> <span data-ttu-id="4926f-107">Интерфейс **ContactItem** предоставляет определенные элементы, относящиеся к электронным визитным карточкам.</span><span class="sxs-lookup"><span data-stu-id="4926f-107">The **ContactItem** interface provides specific members that pertain to Electronic Business Cards.</span></span> <span data-ttu-id="4926f-108">Ими являются **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) и [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="4926f-108">These members are **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)) , [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)) , [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)) , [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)) , [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) , and [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)) .</span></span>

<span data-ttu-id="4926f-109">В представленном ниже примере кода BusinessCardLayoutExample изменяет макет электронной визитной карточки путем первоначального получения заданного объекта **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="4926f-109">In the following code example, BusinessCardLayoutExample modifies the layout of an electronic business card by first obtaining a specified **ContactItem** object.</span></span> <span data-ttu-id="4926f-110">В этом случае объект **ContactItem** является контактом со значением свойства [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) равным "Melissa MacBeth".</span><span class="sxs-lookup"><span data-stu-id="4926f-110">In this case, the **ContactItem** is a contact with the value of the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property equal to “Melissa MacBeth”.</span></span> <span data-ttu-id="4926f-111">Затем BusinessCardLayoutExample создает класс XML-документа [XmlDocument](https://msdn.microsoft.com/ru-RU/library/6kza7w4k) и получает атрибут структуры этого класса в строке с помощью значения **BusinessCardLayoutXML** для объекта **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="4926f-111">Next, BusinessCardLayoutExample creates an XML document class [XmlDocument](https://msdn.microsoft.com/ru-RU/library/6kza7w4k), and then gets the layout attribute of this class in a string by using the **BusinessCardLayoutXML** value for the **ContactItem** object.</span></span> <span data-ttu-id="4926f-112">После этого макет карточки изменяется с выравнивания по левому краю на выравнивание по правому.</span><span class="sxs-lookup"><span data-stu-id="4926f-112">The card layout is then changed from left-aligned to right-aligned.</span></span>

<span data-ttu-id="4926f-113">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="4926f-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="4926f-114">Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class.</span><span class="sxs-lookup"><span data-stu-id="4926f-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="4926f-115">В следующей строке кода показано, как выполнить импорт и назначение в C\#.</span><span class="sxs-lookup"><span data-stu-id="4926f-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="4926f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4926f-116">See also</span></span>

- [<span data-ttu-id="4926f-117">Электронные визитные карточки</span><span class="sxs-lookup"><span data-stu-id="4926f-117">Electronic Business Cards</span></span>](electronic-business-cards.md)

