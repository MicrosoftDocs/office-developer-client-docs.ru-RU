---
title: Обеспечение поддержки настраиваемых свойств элемента в запросах на уровне папки
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 659919de8eeb17e675ed67f3b777f67b04f13b54
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406941"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a>Обеспечение поддержки настраиваемых свойств элемента в запросах на уровне папки

В этом примере показывается, как гарантировать добавление настраиваемого свойства для папки, когда это свойство добавляется для типа элемента, чтобы для настраиваемого свойства можно было выполнить запрос на уровне папки.

## <a name="example"></a>Пример

В приведенном примере кода показано, как использовать объекты [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) и [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)), чтобы гарантировать добавление настраиваемого свойства для папки, когда это свойство добавляется для типа элемента, чтобы для настраиваемого свойства можно было выполнить запрос на уровне папки.

При использовании метода [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) в коллекции [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)), чтобы добавить настраиваемое свойство для элемента, можно задать параметру *AddToFolderFields* значение **true** для добавления свойства в папку. Однако настраиваемое свойство может не добавиться в нужную папку из-за ошибки разработчика или действия пользователя, например при удалении настраиваемого свойства с помощью средства выбора полей Outlook или перемещении элемента в другую папку. Следовательно методы [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) и [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) объекта [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)), использующего это настраиваемое свойство, завершатся сбоем. С помощью объекта **UserDefinedProperties** можно проверить, существуют ли настраиваемые свойства в папке, и добавить настраиваемые свойства, если их нет или они были удалены.

Чтобы сохранить настраиваемое свойство, представленное объектом **UserDefinedProperty** в папке, необходимо сохранить настраиваемое свойство с тем же именем в элементе. Хранение значения в объекте **UserDefinedProperty** для папки не выполняет никаких действий. Нужно настроить коллекцию **UserProperties** элемента на доступ к объекту [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)), который нужно задать, а затем установить значение для объекта **UserProperty**. Убедитесь, что вызывается метод **Save** для элемента, чтобы сохранить изменения.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующих строках кода показано, как выполнить импорт и назначение в Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoUserDefinedProperty()
    Dim folder As Outlook.Folder = _
        CType(Application.ActiveExplorer().CurrentFolder(), _
        Outlook.Folder)
    Dim post As Outlook.PostItem = CType( _
        folder.Items.Add("IPM.Post"), Outlook.PostItem)
    ' Add UserProperty to PostItem
    post.UserProperties.Add("ColorID", _
        Outlook.OlUserPropertyType.olText, False)
    post.UserProperties("ColorID").Value = "Green"
    post.Subject = "UserProperty Example"
    post.Save()
    Dim findPost As Outlook.PostItem
    Try
        ' Items.Find will fail unless custom property
        ' is defined in the folder
        findPost = _
            CType(folder.Items.Find("[ColorID] = 'Green'"), _
            Outlook.PostItem)
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
        ' Add ColorID field to the folder
        folder.UserDefinedProperties.Add("ColorID", _
            Outlook.OlUserPropertyType.olText)
        ' Now the find works ok
        Dim findPostOK As Outlook.PostItem
        Try
            findPostOK = _
                CType(folder.Items.Find("[ColorID] = 'Green'"), _
                Outlook.PostItem)
            If Not (findPostOK Is Nothing) Then
                Debug.WriteLine("Found PostItem")
            End If
            ' Cleanup by deleting PostItem and ColorID
            findPostOK.Delete()
            Dim userProperty As Outlook.UserDefinedProperty = _
                folder.UserDefinedProperties("ColorID")
            userProperty.Delete()
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
End Sub
```


```csharp
private void DemoUserDefinedProperty()
{
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.PostItem post = folder.Items.Add("IPM.Post")
        as Outlook.PostItem;
    // Add UserProperty to PostItem
    post.UserProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        false, Type.Missing);
    post.UserProperties["ColorID"].Value = "Green";
    post.Subject = "UserProperty Example";
    post.Save();
    Outlook.PostItem findPost;
    try
    {
        // Items.Find will fail unless custom property
        // is defined in the folder
        findPost =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
     // Add ColorID field to the folder
    folder.UserDefinedProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        Type.Missing, Type.Missing);
    // Now the find works ok
    Outlook.PostItem findPostOK;
    try
    {
        findPostOK =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
        if (findPostOK != null)
        {
            Debug.WriteLine("Found PostItem");
        }
        // Cleanup by deleting PostItem and ColorID
        findPostOK.Delete();
        Outlook.UserDefinedProperty userProperty =
            folder.UserDefinedProperties["ColorID"];
        userProperty.Delete();
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>См. также

- [Папки](folders.md)

