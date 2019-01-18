---
title: Отправка почтового элемента с электронной визитной карточкой
TOCTitle: Send a mail item with an electronic business card
ms:assetid: f8aae7f2-85fc-4ed0-9f59-282ede702357
ms:mtpsurl: https://msdn.microsoft.com/library/Bb624312(v=office.15)
ms:contentKeyID: 55119839
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25809fc0d1726c9f56be417ae53fadecc831d62f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704548"
---
# <a name="send-a-mail-item-with-an-electronic-business-card"></a>Отправка почтового элемента с электронной визитной карточкой

В этом примере показано, как создать почтовый элемент, выполнить поиск электронной визитной карточки и, если она будет найдена, вставить ее в почтовый элемент.

## <a name="example"></a>Пример

Чтобы вставить электронную визитную карточку, можно вызвать метод [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) для объекта [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)). Этот метод получает строку, представляющую электронный адрес, и пытается найти элемент [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) с этим адресом в папке "Контакты", используемой по умолчанию. Элемент **ContactItem** может иметь до трех электронных адресов. Если удалось найти контакт, код в примере вызывает метод **AddBusinessCard**, а затем отображает сообщение для пользователя.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

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

## <a name="see-also"></a>См. также

- [Электронные визитные карточки](electronic-business-cards.md)

