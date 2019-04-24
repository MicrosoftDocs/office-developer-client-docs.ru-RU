---
title: Создание почтового элемента с помощью шаблона сообщения
TOCTitle: Create a mail item by using a message template
ms:assetid: 7d1ffc3b-d1a7-46d1-adb9-ac41e67f626a
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623026(v=office.15)
ms:contentKeyID: 55119862
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cdd9654187685ceab1062fb4ae1882b2d48c68d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349541"
---
# <a name="create-a-mail-item-by-using-a-message-template"></a>Создание почтового элемента с помощью шаблона сообщения

В этом примере показано, как создать почтовый элемент с помощью метода [CreateItemFromTemplate](https://msdn.microsoft.com/library/bb611329\(v=office.15\)).

## <a name="example"></a>Пример

Код примера открывает файл шаблона Ivy.oft, назначает тему, а затем сохраняет сообщение в папке "Черновики".

Метод **CreateItemFromTemplate** полезен, если есть сохраненный на диске файл шаблона формы Outlook (.oft), который нужно использовать в качестве шаблона сообщения. Файл шаблона может содержать предварительно форматированный текст, бланк или изображения, которые нужно включить в сообщение. Но если файл шаблона содержит код для формы, код формы выполнен не будет.

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса. В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateItemFromTemplate()
    Dim folder As Outlook.Folder = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderDrafts), Outlook.Folder)
    Dim mail As Outlook.MailItem = _
        CType(Application.CreateItemFromTemplate( _
        "c:\ivy.oft", folder), Outlook.MailItem)
    mail.Subject = "Congratulations"
    mail.Save()
End Sub
```


```csharp
private void CreateItemFromTemplate()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderDrafts) as Outlook.Folder;
    Outlook.MailItem mail =
        Application.CreateItemFromTemplate(
        @"c:\ivy.oft", folder) as Outlook.MailItem;
    mail.Subject = "Congratulations";
    mail.Save();
}
```

## <a name="see-also"></a>См. также

- [Почта](mail.md)

