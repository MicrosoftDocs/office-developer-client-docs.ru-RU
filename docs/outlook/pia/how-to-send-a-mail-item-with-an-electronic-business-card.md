---
title: Отправка почтового элемента с электронной визитной карточкой
TOCTitle: Send a mail item with an electronic business card
ms:assetid: f8aae7f2-85fc-4ed0-9f59-282ede702357
ms:mtpsurl: https://msdn.microsoft.com/library/Bb624312(v=office.15)
ms:contentKeyID: 55119839
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 22d931832b0b12a7baa2e8d04789db03f89ac0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406220"
---
# <a name="send-a-mail-item-with-an-electronic-business-card"></a><span data-ttu-id="5ccc6-102">Отправка почтового элемента с электронной визитной карточкой</span><span class="sxs-lookup"><span data-stu-id="5ccc6-102">Send a mail item with an electronic business card</span></span>

<span data-ttu-id="5ccc6-103">В этом примере показано, как создать почтовый элемент, выполнить поиск электронной визитной карточки и, если она будет найдена, вставить ее в почтовый элемент.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-103">This example creates a mail item, looks for an Electronic Business Card, and if it finds one, inserts the Electronic Business Card into the mail item.</span></span>

## <a name="example"></a><span data-ttu-id="5ccc6-104">Пример</span><span class="sxs-lookup"><span data-stu-id="5ccc6-104">Example</span></span>

<span data-ttu-id="5ccc6-105">Чтобы вставить электронную визитную карточку, можно вызвать метод [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) для объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5ccc6-105">To insert an Electronic Business Card, you can call [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) on the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="5ccc6-106">Этот метод получает строку, представляющую электронный адрес, и пытается найти элемент [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) с этим адресом в папке "Контакты", используемой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-106">This method takes a string representing an e-mail address and attempts to find a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) with that address in the default Contacts folder.</span></span> <span data-ttu-id="5ccc6-107">Элемент **ContactItem** может иметь до трех электронных адресов.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-107">A **ContactItem** can have as many as three e-mail addresses.</span></span> <span data-ttu-id="5ccc6-108">Если удалось найти контакт, код в примере вызывает метод **AddBusinessCard**, а затем отображает сообщение для пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-108">If the contact is found, the example calls the **AddBusinessCard** method, and then displays the message to the user.</span></span>

<span data-ttu-id="5ccc6-109">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="5ccc6-110">Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-110">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="5ccc6-111">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="5ccc6-111">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub AddBusinessCard(ByVal eMailAddress As String)
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML
    Dim contact As Outlook.ContactItem = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find( _
        "[Email1Address]='" & eMailAddress & "'" & " OR " & _
        "[Email2Address]='" & eMailAddress & "'" + " OR " & _
        "[Email3Address]='" & eMailAddress & "'") _
        , Outlook.ContactItem)
    If (contact Is Nothing) Then
        Return
    End If
    mail.AddBusinessCard(contact)
    mail.Display(False)
End Sub
```


```csharp
private void AddBusinessCard(string eMailAddress)
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML;
    Outlook.ContactItem contact = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Email1Address]='" + eMailAddress + "'" + " OR " +
        "[Email2Address]='" + eMailAddress + "'" + " OR " +
        "[Email3Address]='" + eMailAddress + "'")
        as Outlook.ContactItem;
    if (contact == null)
    {
        return;
    }
    mail.AddBusinessCard(contact);
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="5ccc6-112">См. также</span><span class="sxs-lookup"><span data-stu-id="5ccc6-112">See also</span></span>

- [<span data-ttu-id="5ccc6-113">Электронные визитные карточки</span><span class="sxs-lookup"><span data-stu-id="5ccc6-113">Electronic Business Cards</span></span>](electronic-business-cards.md)

