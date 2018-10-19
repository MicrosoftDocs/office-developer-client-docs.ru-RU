---
title: Отображение в диалоговом окне "Выбор имен" адресной книги, соответствующей папке "Контакты"
TOCTitle: Display in the Select Names dialog box the address book corresponding to a Contacts folder
ms:assetid: 6cbfc843-51b5-4841-bbb1-14b93a35ba78
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610437(v=office.15)
ms:contentKeyID: 55119799
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 8aa7093b26366f5aa47ce054b27eff04d48889b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405793"
---
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a>Отображение в диалоговом окне "Выбор имен" адресной книги, соответствующей папке "Контакты"

В этом примере показывается, как получить адресную книгу, соответствующую папке "Контакты" по умолчанию, а затем вывести эту адресную книгу в диалоговом окне **Выбор имен**.

## <a name="example"></a>Пример

Все адресные книги в Outlook представлены в виде коллекции свойством [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . В коде примера используется метод [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) объекта [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) , чтобы найти папку контактов, соответствующую каждому списку адресов. У каждой папки Outlook есть код записи. Сравните код записи папки "Контакты" по умолчанию с кодом записи папки "Контакты", чтобы создать AddressList, соответствующий папке "Контакты" по умолчанию.

Перед отображением в диалоговом окне **Выбор имен** списка адресов, соответствующих папке "Контакты" по умолчанию, код примера задает его как значение свойства [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) объекта [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) .

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ShowContactsFolderAsInitialAddressList()
    Dim addrLists As Outlook.AddressLists
    Dim contactsFolder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts), _
        Outlook.Folder)
    addrLists = Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        Dim testFolder As Outlook.Folder = _
        CType(addrList.GetContactsFolder(), Outlook.Folder)
        If Not (testFolder Is Nothing) Then
            ' Test to determine if Folder returned
            ' by GetContactsFolder has same EntryID
            ' as default Contacts folder.
            If (Application.Session.CompareEntryIDs( _
                contactsFolder.EntryID, testFolder.EntryID)) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.InitialAddressList = addrList
                snd.Display()
            End If
        End If
    Next
End Sub
```


```csharp
private void ShowContactsFolderAsInitialAddressList()
{
    Outlook.AddressLists addrLists;
    Outlook.Folder contactsFolder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    addrLists = Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        Outlook.Folder testFolder =
            addrList.GetContactsFolder() as Outlook.Folder;
        if (testFolder != null)
        {
            // Test to determine if Folder returned
            // by GetContactsFolder has same EntryID
            // as default Contacts folder.
            if (Application.Session.CompareEntryIDs(
                contactsFolder.EntryID, testFolder.EntryID))
            {
                Outlook.SelectNamesDialog snd =
                    Application.
                    Session.GetSelectNamesDialog();
                snd.InitialAddressList = addrList;
                snd.Display();
             }
         }
    }
}
```

## <a name="see-also"></a>См. также

- [Адресная книга](address-book.md)

