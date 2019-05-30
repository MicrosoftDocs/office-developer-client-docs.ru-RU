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
# <a name="programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk"></a><span data-ttu-id="c3be1-102">Программное удаление вложений уровня безопасности 2 из сообщений и сохранение их на диске</span><span class="sxs-lookup"><span data-stu-id="c3be1-102">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>

<span data-ttu-id="c3be1-103">В этом примере показано, как удалять вложения уровня безопасности 2 из сообщений электронной почты и сохранять их на диске, где их можно открыть.</span><span class="sxs-lookup"><span data-stu-id="c3be1-103">This example shows how to remove security level 2 attachments from email messages and save them to a disk, from where they can be opened.</span></span>

## <a name="example"></a><span data-ttu-id="c3be1-104">Пример</span><span class="sxs-lookup"><span data-stu-id="c3be1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c3be1-105">Приведенный ниже пример кода взят из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c3be1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="c3be1-106">Outlook защищает пользователей от вредоносного кода, переносимого в коде вложений электронной почты с определенными расширениями файла (например, EXE или BAT).</span><span class="sxs-lookup"><span data-stu-id="c3be1-106">Outlook protects users from malicious code transported via email attachments that have certain file extensions such as .exe or .bat.</span></span> <span data-ttu-id="c3be1-107">Эти определенные вложения блокируются по умолчанию и определяются как вложения уровня 1.</span><span class="sxs-lookup"><span data-stu-id="c3be1-107">Those particular attachments are blocked by default and identified as Level 1 attachments.</span></span> <span data-ttu-id="c3be1-108">Вероятность того, что вложения уровня 2 содержат вредоносный код, меньше, но пользователи не могут открыть вложение уровня 2 непосредственно из сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c3be1-108">Level 2 attachments have a lesser chance of containing malicious code, but users cannot open a Level 2 attachment directly from an email message.</span></span> <span data-ttu-id="c3be1-109">Вложение уровня 2 сначала нужно сохранить на диске.</span><span class="sxs-lookup"><span data-stu-id="c3be1-109">A Level 2 attachment must first be saved to a disk.</span></span>

<span data-ttu-id="c3be1-110">С помощью метода [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) в объекте [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) можно сохранять вложения на диске.</span><span class="sxs-lookup"><span data-stu-id="c3be1-110">By using the [SaveAsFile(String)](https://msdn.microsoft.com/library/bb624311\(v=office.15\)) method in the [Attachment](https://msdn.microsoft.com/library/bb609285\(v=office.15\)) object, you can save attachments to a disk.</span></span> <span data-ttu-id="c3be1-111">В следующем примере кода RemoveAttachmentsAndSaveToDisk сначала удаляет из почтовых элементов в папке все вложения уровня 2, размер которых больше заданной величины.</span><span class="sxs-lookup"><span data-stu-id="c3be1-111">In the following code example, RemoveAttachmentsAndSaveToDisk first removes from mail items in a folder all Level 2 attachments that are greater than a specified size.</span></span> <span data-ttu-id="c3be1-112">Это происходит путем перечисления свойства [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) каждого объекта **Attachment** в коллекции [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) и удаления тех экземпляров, которые равны [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c3be1-112">This is done by enumerating the [Type](https://msdn.microsoft.com/library/bb609277\(v=office.15\)) property of each **Attachment** object in the [Attachments](https://msdn.microsoft.com/library/bb646211\(v=office.15\)) collection and removing the ones that are equal to [olByValue](https://msdn.microsoft.com/library/bb623448\(v=office.15\)).</span></span> <span data-ttu-id="c3be1-113">Затем RemoveAttachmentsAndSaveToDisk сохраняет удаленное вложение путем использования метода **SaveAsFile**.</span><span class="sxs-lookup"><span data-stu-id="c3be1-113">RemoveAttachmentsAndSaveToDisk then saves the removed attachment by using the **SaveAsFile** method.</span></span>

> [!NOTE] 
> <span data-ttu-id="c3be1-114">Коллекции в Outlook линейны.</span><span class="sxs-lookup"><span data-stu-id="c3be1-114">Collections in Outlook are linear.</span></span> <span data-ttu-id="c3be1-115">Воспользуйтесь оператором [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia), чтобы создать ссылку **Attachments**[1] на **Attachments**[n], где n  значение свойства [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia).</span><span class="sxs-lookup"><span data-stu-id="c3be1-115">Use the [Index](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachment.index?view=outlook-pia) operator to reference **Attachments**[1] to **Attachments**[n], where n represents the value of the [Count](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.attachments.count?view=outlook-pia) property.</span></span>
> 
> <span data-ttu-id="c3be1-p104">Удалить элементы из коллекции не удается с помощью оператора **foreach**. Вместо этого воспользуйтесь оператором **Index** для получения первого элемента в коллекции, а затем удалите этот элемент. После этого примените оператор **while**, чтобы определить, когда вы удалили подходящее число элементов из коллекции. Это обеспечит итерацию правильного количества элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c3be1-p104">You cannot use a **foreach** statement to remove items in a collection. Instead, use an **Index** operator to obtain the first item in the collection, and then delete the item. Then use a **while** statement to determine when you have deleted the appropriate number of items in the collection. This will ensure that you have iterated over the correct number of items in the collection.</span></span>

<span data-ttu-id="c3be1-120">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c3be1-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c3be1-121">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="c3be1-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c3be1-122">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="c3be1-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c3be1-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c3be1-123">See also</span></span>

- [<span data-ttu-id="c3be1-124">Вложения</span><span class="sxs-lookup"><span data-stu-id="c3be1-124">Attachments</span></span>](attachments.md)

