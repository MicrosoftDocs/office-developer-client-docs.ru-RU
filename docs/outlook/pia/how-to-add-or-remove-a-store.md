---
title: Добавление и удаление хранилища
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b0c8184d5e062d560614a8703494b673485866e3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407039"
---
# <a name="add-or-remove-a-store"></a>Добавление и удаление хранилища

В этом примере показано, как добавлять и удалять хранилище в заданном профиле.

## <a name="example"></a>Пример

В этом образце кода показан метод добавления и удаления хранилища в указанном профиле путем вызова метода [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) и метода [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) соответственно по отношению к объекту [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) .

В Outlook можно добавить или удалить PST-хранилище только программным путем. Следующий образец кода служит для добавления хранилища Юникода и размещения PST-файла в местоположении, выбранном по умолчанию для пользовательских PST-файлов: Documents and Settings\\\<Имя_пользователя\>\\Local Settings\\Application Data\\Microsoft\\Outlook. В этом образце кода применяется Environment.SpecialFolder.LocalApplicationData для извлечения пути к папке Application Data в папке Local Settings. После добавления хранилища образец кода удаляет хранилище. Так как метод **RemoveStore** требует наличия объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) для удаления [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , он перечисляет коллекцию [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) для поиска только что добавленного объекта **Store**, исходя из свойства [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) объекта **Store**.

Метод **RemoveStore** удаляет только хранилище из текущего профиля. Он не удаляет PST-файл из файловой системы.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>См. также

- [Хранилища](stores.md)
