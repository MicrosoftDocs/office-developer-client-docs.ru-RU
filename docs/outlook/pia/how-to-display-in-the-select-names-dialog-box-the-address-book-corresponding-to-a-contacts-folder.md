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
# <a name="display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder"></a><span data-ttu-id="5cc8d-102">Отображение в диалоговом окне "Выбор имен" адресной книги, соответствующей папке "Контакты"</span><span class="sxs-lookup"><span data-stu-id="5cc8d-102">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>

<span data-ttu-id="5cc8d-103">В этом примере показывается, как получить адресную книгу, соответствующую папке "Контакты" по умолчанию, а затем вывести эту адресную книгу в диалоговом окне **Выбор имен**.</span><span class="sxs-lookup"><span data-stu-id="5cc8d-103">This example shows how to obtain the address book that corresponds to the default Contacts folder, and then displays the address book in the **Select Names** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="5cc8d-104">Пример</span><span class="sxs-lookup"><span data-stu-id="5cc8d-104">Example</span></span>

<span data-ttu-id="5cc8d-p101">Все адресные книги в Outlook представлены в виде коллекции свойством [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . В коде примера используется метод [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) объекта [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) , чтобы найти папку контактов, соответствующую каждому списку адресов. У каждой папки Outlook есть код записи. Сравните код записи папки "Контакты" по умолчанию с кодом записи папки "Контакты", чтобы создать AddressList, соответствующий папке "Контакты" по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5cc8d-p101">All address books in Outlook are represented as a collection by the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object. The code sample uses the [GetContactsFolder](https://msdn.microsoft.com/library/bb609225\(v=office.15\)) method of the [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object to find the contact folder that corresponds to each address list. Each Outlook folder has an Entry ID. Compare the Entry ID of the default Contacts folder with the Entry ID of a Contacts folder to produce the AddressList that corresponds to the default Contacts folder.</span></span>

<span data-ttu-id="5cc8d-109">Перед отображением в диалоговом окне **Выбор имен** списка адресов, соответствующих папке "Контакты" по умолчанию, код примера задает его как значение свойства [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) объекта [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="5cc8d-109">Before displaying the address list corresponding to the default Contacts folder in the **Select Names** dialog box, the code sample sets it as the value of the [InitialAddressList](https://msdn.microsoft.com/library/bb646633\(v=office.15\)) property of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object.</span></span>

<span data-ttu-id="5cc8d-110">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5cc8d-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="5cc8d-111">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="5cc8d-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="5cc8d-112">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="5cc8d-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="5cc8d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="5cc8d-113">See also</span></span>

- [<span data-ttu-id="5cc8d-114">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="5cc8d-114">Address Book</span></span>](address-book.md)

