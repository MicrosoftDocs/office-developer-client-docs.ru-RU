---
title: Получение класса сообщений по умолчанию для папки
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 031b7736ed397b9218ea677442f80595da2aa919
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542564"
---
# <a name="get-the-default-message-class-of-a-folder"></a><span data-ttu-id="37015-102">Получение класса сообщений по умолчанию для папки</span><span class="sxs-lookup"><span data-stu-id="37015-102">Get the default message class of a folder</span></span>

<span data-ttu-id="37015-103">В этом примере показано, как использовать свойство [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) для получения класса сообщений по умолчанию для папки.</span><span class="sxs-lookup"><span data-stu-id="37015-103">This example shows how to use the [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) property to obtain the default message class of a folder.</span></span>

## <a name="example"></a><span data-ttu-id="37015-104">Пример</span><span class="sxs-lookup"><span data-stu-id="37015-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="37015-105">Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="37015-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="37015-106">Для получения класса сообщений по умолчанию для папки используйте свойство **DefaultMessageClass** объекта [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="37015-106">To obtain the default message class for a folder, use the **DefaultMessageClass** property of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object.</span></span> <span data-ttu-id="37015-107">Например, наличие у объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) свойства **DefaultMessageClass**, равного IPM.Contact, означает, что этот объект представляет папку контакта.</span><span class="sxs-lookup"><span data-stu-id="37015-107">For example, a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object that has a **DefaultMessageClass** of IPM.Contact means that it represents a Contact folder.</span></span> <span data-ttu-id="37015-108">Но если для папки в качестве формы по умолчанию задана настраиваемая форма или заменяющая форма, необходимо использовать объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , чтобы определить класс сообщения формы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37015-108">However, if the folder has a custom form or a replacement form as a default form, you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to determine the message class of the default form.</span></span> <span data-ttu-id="37015-109">Свойство **DefaultMessageClass** не возвращает класс сообщения формы по умолчанию для папки.</span><span class="sxs-lookup"><span data-stu-id="37015-109">The **DefaultMessageClass** property does not return the message class of the default form for the folder.</span></span>

<span data-ttu-id="37015-110">В следующем примере кода процедура GetDefaultMessageClass использует **PropertyAccessor**, чтобы определить для папки форму по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37015-110">In the following code example, the GetDefaultMessageClass procedure uses the **PropertyAccessor** to determine the default form of a folder.</span></span> <span data-ttu-id="37015-111">Если свойство **\_Folder мсгкласс\_Post\_** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) не найдено, а Outlook вызывает ошибку, то **try... Catch** возвращает свойство **DefaultMessageClass** для **папки**.</span><span class="sxs-lookup"><span data-stu-id="37015-111">If the folder property **PR\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) is not found and Outlook raises an error, the **try…catch** block returns the **DefaultMessageClass** property for the **Folder**.</span></span>

<span data-ttu-id="37015-112">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="37015-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="37015-113">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="37015-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="37015-114">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="37015-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"http://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="37015-115">См. также</span><span class="sxs-lookup"><span data-stu-id="37015-115">See also</span></span>

- [<span data-ttu-id="37015-116">Folders</span><span class="sxs-lookup"><span data-stu-id="37015-116">Folders</span></span>](folders.md)

