---
title: Создание элемента Contact из файла vCard и сохранение этого элемента в папке
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 667278b290e32bc5115a468b1c038d6aa63a5aff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407396"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a><span data-ttu-id="6ff64-102">Создание элемента Contact из файла vCard и сохранение этого элемента в папке</span><span class="sxs-lookup"><span data-stu-id="6ff64-102">Create a Contact item from a vCard file and save the item in a folder</span></span>

<span data-ttu-id="6ff64-103">В этом примере показано, как импортировать все файлы vCard в папку файловой системы и сохранить контакты в папке, указанной в параметре *targetFolder*.</span><span class="sxs-lookup"><span data-stu-id="6ff64-103">This example imports all the vCard files in a file system folder and saves the contacts into the folder specified by the  *targetFolder* parameter.</span></span>

## <a name="example"></a><span data-ttu-id="6ff64-104">Пример</span><span class="sxs-lookup"><span data-stu-id="6ff64-104">Example</span></span>

<span data-ttu-id="6ff64-p101">Здесь применяется метод [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)). Метод **OpenSharedItem** открывает сообщения, сохраненные в виде файлов с форматом сообщений Outlook (MSG), файлов встреч в формате iCalendar (ICS) или файлов vCard (VCF). Обязательно отнесите возвращенный объект к подходящему типу элемента и вызовите соответствующий метод **Save** для сохранения этого элемента. Элемент, возвращаемый **OpenSharedItem**, по умолчанию сохраняется в стандартной папке, которая выбрана для определенного типа элемента. Чтобы переместить элемент в другую папку, воспользуйтесь методом **Move**.</span><span class="sxs-lookup"><span data-stu-id="6ff64-p101">This example uses the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method. The **OpenSharedItem** method opens messages stored as Outlook message format (.msg) files, iCalendar appointment (.ics) files, or vCard (.vcf) files. Be sure to cast the returned object to the appropriate item type and call the corresponding **Save** method to persist the item. By default, the item returned by **OpenSharedItem** is saved in the default folder for the specific item type. You can use the corresponding **Move** method to move the item to a different folder.</span></span>

<span data-ttu-id="6ff64-110">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6ff64-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="6ff64-111">Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="6ff64-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="6ff64-112">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="6ff64-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ImportContacts( _
    ByVal path As String, ByVal targetFolder As Outlook.Folder)
    Dim contact As Outlook.ContactItem
    Dim moveContact As Outlook.ContactItem
    If (Directory.Exists(path)) Then
        Dim files As String() = Directory.GetFiles(path, "*.vcf")
        For Each file As String In files
            contact = CType(Application.Session.OpenSharedItem(file), _
                Outlook.ContactItem)
            If (targetFolder Is _
                CType(Application.Session.GetDefaultFolder( _
                    Outlook.OlDefaultFolders.olFolderContacts) _
                    , Outlook.Folder)) Then
                contact.Save()
            Else
                moveContact = CType(contact.Move(targetFolder), _
                    Outlook.ContactItem)
                moveContact.Save()
            End If
        Next
    End If
End Sub
```


```csharp
private void ImportContacts(string path, Outlook.Folder targetFolder)
{
    Outlook.ContactItem contact;
    Outlook.ContactItem moveContact;
    if (Directory.Exists(path))
    {
        string[] files = Directory.GetFiles(path, "*.vcf");
        foreach (string file in files)
        {
            contact = Application.Session.OpenSharedItem(file)
                as Outlook.ContactItem;
            if (targetFolder ==
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderContacts)
                as Outlook.Folder)
            {
                contact.Save();
            }
            else
            {
                moveContact = contact.Move(targetFolder)
                    as Outlook.ContactItem;
                moveContact.Save();
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="6ff64-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6ff64-113">See also</span></span>

- [<span data-ttu-id="6ff64-114">Contacts</span><span class="sxs-lookup"><span data-stu-id="6ff64-114">Contacts</span></span>](contacts.md)

