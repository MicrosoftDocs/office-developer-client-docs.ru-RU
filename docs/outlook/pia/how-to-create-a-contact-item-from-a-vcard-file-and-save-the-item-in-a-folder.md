---
title: Создание элемента Contact из файла vCard и сохранение этого элемента в папке
TOCTitle: Create a Contact item from a vCard file and save the item in a folder
ms:assetid: b207b584-ffcf-4ac5-ab1f-4f91d43000e1
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646856(v=office.15)
ms:contentKeyID: 55119826
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a048d090c946ff5a86fddf4b1ac8c6818e061b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321261"
---
# <a name="create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder"></a>Создание элемента Contact из файла vCard и сохранение этого элемента в папке

В этом примере показано, как импортировать все файлы vCard в папку файловой системы и сохранить контакты в папке, указанной в параметре *targetFolder*.

## <a name="example"></a>Пример

Здесь применяется метод [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)). Метод **OpenSharedItem** открывает сообщения, сохраненные в виде файлов с форматом сообщений Outlook (MSG), файлов встреч в формате iCalendar (ICS) или файлов vCard (VCF). Обязательно отнесите возвращенный объект к подходящему типу элемента и вызовите соответствующий метод **Save** для сохранения этого элемента. Элемент, возвращаемый **OpenSharedItem**, по умолчанию сохраняется в стандартной папке, которая выбрана для определенного типа элемента. Чтобы переместить элемент в другую папку, воспользуйтесь методом **Move**.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

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

## <a name="see-also"></a>См. также

- [Контакты](contacts.md)

