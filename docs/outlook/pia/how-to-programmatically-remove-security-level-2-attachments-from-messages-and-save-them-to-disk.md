---
title: Программное удаление вложений уровня безопасности 2 из сообщений и их сохранение на диске
TOCTitle: Programmatically remove security level 2 attachments from messages and save them to disk
ms:assetid: fb63e505-a243-40a5-919d-e4fe914af3f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184657(v=office.15)
ms:contentKeyID: 55119822
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 588d1db8ad222462b2648d4fdb85207fd9bdb782
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539264"
---
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a>Программное удаление вложений уровня безопасности 2 из сообщений и сохранение их на диске

В этом примере показано, как удалять вложения уровня безопасности 2 из сообщений электронной почты и сохранять их на диске, где их можно открыть.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Outlook защищает пользователей от вредоносного кода, переносимого в коде вложений электронной почты с определенными расширениями файла (например, EXE или BAT). Эти определенные вложения блокируются по умолчанию и определяются как вложения уровня 1. Вероятность того, что вложения уровня 2 содержат вредоносный код, меньше, но пользователи не могут открыть вложение уровня 2 непосредственно из сообщения электронной почты. Вложение уровня 2 сначала нужно сохранить на диске.

С помощью метода [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) в объекте [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) можно сохранять вложения на диске. В следующем примере кода RemoveAttachmentsAndSaveToDisk сначала удаляет из почтовых элементов в папке все вложения уровня 2, размер которых больше заданной величины. Это происходит путем перечисления свойства [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) каждого объекта **Attachment** в коллекции [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) и удаления тех экземпляров, которые равны [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)). Затем RemoveAttachmentsAndSaveToDisk сохраняет удаленное вложение путем использования метода **SaveAsFile**.

> [!NOTE] 
> Коллекции в Outlook линейны. Воспользуйтесь оператором [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia), чтобы создать ссылку **Attachments**[1] на **Attachments**[n], где n  значение свойства [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).
> 
> Удалить элементы из коллекции не удается с помощью оператора **foreach**. Вместо этого воспользуйтесь оператором **Index** для получения первого элемента в коллекции, а затем удалите этот элемент. После этого примените оператор **while**, чтобы определить, когда вы удалили подходящее число элементов из коллекции. Это обеспечит итерацию правильного количества элементов в коллекции.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RemoveAttachmentsAndSaveToDisk(string path,
    Outlook.Folder folder, int size)
{
    Outlook.Items attachItems;
    Outlook.Attachment attachment;
    Outlook.Attachments attachments;
    int byValueCount;
    int removeCount;
    bool saveMessage;
    try
    {
        // The restriction will find all items that
        // have attachments and MessageClass = IPM.Note.
        string filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:hasattachment"
            + "\"" + " = True" + " AND " + "\""
            + "http://schemas.microsoft.com/mapi/proptag/0x001A001E"
            + "\"" + " = 'IPM.Note'";
        attachItems = folder.Items.Restrict(filter);
        foreach (Outlook.MailItem mail in attachItems)
        {
            saveMessage = false;
            byValueCount = 0;
            attachments = mail.Attachments;
            // Obtain the count of ByValue attachments.
            foreach (Outlook.Attachment attach in attachments)
            {
                if (attach.Size > size
                    & attach.Type ==
                    Outlook.OlAttachmentType.olByValue)
                {
                    byValueCount = byValueCount + 1;
                }
            }
            if (byValueCount > 0)
            {
                // removeCount is number of attachments to remove.
                removeCount = attachments.Count - byValueCount;
                while (mail.Attachments.Count != removeCount)
                {
                    // Use indexer to obtain 
                    // first attachment in collection.
                    attachment = mail.Attachments[1];
                    // You can refine this code to save 
                    // separate copies of attachments 
                    // with the same name.
                    attachment.SaveAsFile(path + @"\"
                        + attachment.FileName);
                    attachment.Delete();
                    if (saveMessage != true)
                    {
                        saveMessage = true;
                    }
                }
                if (saveMessage)
                {
                    mail.Save();
                }
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

- [Вложения](attachments.md)

