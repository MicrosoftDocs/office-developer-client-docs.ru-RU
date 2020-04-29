---
title: Обеспечение поддержки настраиваемых свойств элемента в запросах на уровне папки
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcba2648988d2de3c208079d2845e2cb4c2f549
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319091"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a><span data-ttu-id="f9904-102">Обеспечение поддержки настраиваемых свойств элемента в запросах на уровне папки</span><span class="sxs-lookup"><span data-stu-id="f9904-102">Ensure that custom item properties are supported in folder-level queries</span></span>

<span data-ttu-id="f9904-103">В этом примере показывается, как гарантировать добавление настраиваемого свойства для папки, когда это свойство добавляется для типа элемента, чтобы для настраиваемого свойства можно было выполнить запрос на уровне папки.</span><span class="sxs-lookup"><span data-stu-id="f9904-103">This example shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

## <a name="example"></a><span data-ttu-id="f9904-104">Пример</span><span class="sxs-lookup"><span data-stu-id="f9904-104">Example</span></span>

<span data-ttu-id="f9904-105">В приведенном примере кода показано, как использовать объекты [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) и [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)), чтобы гарантировать добавление настраиваемого свойства для папки, когда это свойство добавляется для типа элемента, чтобы для настраиваемого свойства можно было выполнить запрос на уровне папки.</span><span class="sxs-lookup"><span data-stu-id="f9904-105">This code sample shows how to use the [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) object and the [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) object to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

<span data-ttu-id="f9904-106">Если вы используете метод [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) в коллекции [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)), чтобы добавить настраиваемое свойство для элемента, можно присвоить параметру *AddToFolderFields* значение **true** для добавления свойства в папку.</span><span class="sxs-lookup"><span data-stu-id="f9904-106">When you use the [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) method on the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection to add a custom property to an item, you can specify the *AddToFolderFields* parameter as **true** to add the property to the folder.</span></span> <span data-ttu-id="f9904-107">Однако настраиваемое свойство может не добавиться в нужную папку из-за ошибки разработчика или действия пользователя, например при удалении настраиваемого свойства с помощью средства выбора полей Outlook или перемещении элемента в другую папку.</span><span class="sxs-lookup"><span data-stu-id="f9904-107">However, the custom property might not get added to the desired folderbecause of developer error or a user action, such as removing the custom property through the Outlook Field Chooser or moving the item to another folder.</span></span> <span data-ttu-id="f9904-108">Следовательно, методы [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) и [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) объекта [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)), использующего это настраиваемое свойство, завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="f9904-108">Consequently, the [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) method and the [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) object that uses that custom property will fail.</span></span> <span data-ttu-id="f9904-109">С помощью объекта **UserDefinedProperties** можно проверить, существуют ли настраиваемые свойства в папке, и добавить настраиваемые свойства, если их нет или они были удалены.</span><span class="sxs-lookup"><span data-stu-id="f9904-109">By using the **UserDefinedProperties** object, you can test whether your custom properties exist in the folder, and add the custom properties if they do not exist or if they have been removed.</span></span>

<span data-ttu-id="f9904-110">Чтобы сохранить настраиваемое свойство, представленное объектом **UserDefinedProperty** в папке, необходимо сохранить настраиваемое свойство с тем же именем в элементе.</span><span class="sxs-lookup"><span data-stu-id="f9904-110">To persist a custom property represented by a **UserDefinedProperty** object in a folder, you must save the custom property with the same name in the item.</span></span> <span data-ttu-id="f9904-111">Хранение значения в объекте **UserDefinedProperty** для папки не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="f9904-111">Storing a value in the **UserDefinedProperty** object for the folder has no effect.</span></span> <span data-ttu-id="f9904-112">Нужно настроить коллекцию **UserProperties** элемента на доступ к объекту [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)), который нужно задать, а затем установить значение для объекта **UserProperty**.</span><span class="sxs-lookup"><span data-stu-id="f9904-112">You must se the item's **UserProperties** collection to access the [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) object that you want to set, and then set the value on the **UserProperty** object.</span></span> <span data-ttu-id="f9904-113">Убедитесь, что вызывается метод **Save** для элемента, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="f9904-113">Be sure to call the **Save** method on the item to persist your changes.</span></span>

<span data-ttu-id="f9904-114">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f9904-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f9904-115">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="f9904-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f9904-116">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="f9904-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f9904-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f9904-117">See also</span></span>

- [<span data-ttu-id="f9904-118">Folders</span><span class="sxs-lookup"><span data-stu-id="f9904-118">Folders</span></span>](folders.md)

