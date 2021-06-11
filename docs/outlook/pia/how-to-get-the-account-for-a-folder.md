---
title: Получение учетной записи для папки
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8f56f866e71b1080d5b7a6a33fb17e3e71ab9199
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320218"
---
# <a name="get-the-account-for-a-folder"></a><span data-ttu-id="135a9-102">Получение учетной записи для папки</span><span class="sxs-lookup"><span data-stu-id="135a9-102">Get the account for a folder</span></span>

<span data-ttu-id="135a9-103">В этом примере показано получение учетной записи, которая связана с папкой в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="135a9-103">This example gets the account that is associated with a folder in the current session.</span></span>

## <a name="example"></a><span data-ttu-id="135a9-104">Пример</span><span class="sxs-lookup"><span data-stu-id="135a9-104">Example</span></span>

<span data-ttu-id="135a9-105">В следующем примере кода функция DisplayAccountForCurrentFolder вызывает функцию GetAccountForFolder, чтобы определить учетную запись, хранилище доставки по умолчанию для которой содержит текущую папку, а затем отображает имя папки.</span><span class="sxs-lookup"><span data-stu-id="135a9-105">In the following code example, the DisplayAccountForCurrentFolder function calls the GetAccountForFolder function to identify the account whose default delivery store hosts the current folder, and then displays the name of the folder.</span></span> <span data-ttu-id="135a9-106">GetAccountForFolder сопоставляет хранилище текущей папки (полученной из свойства [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) с хранилищем доставки по умолчанию каждой учетной записи (полученным с помощью свойства [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))), определенного в коллекции [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) для сеанса.</span><span class="sxs-lookup"><span data-stu-id="135a9-106">GetAccountForFolder matches the store of the current folder (obtained from the [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) property) with the default delivery store of each account (obtained with the [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) property) that is defined in the [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) collection for the session.</span></span> <span data-ttu-id="135a9-107">GetAccountForFolder возвращает объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), если соответствие найдено, в противном случае функция возвращает пустую ссылку (NULL).</span><span class="sxs-lookup"><span data-stu-id="135a9-107">GetAccountForFolder returns the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object if a match is found; otherwise, it returns a null reference.</span></span>

<span data-ttu-id="135a9-p102">В сеансе Microsoft Outlook, использующем несколько определенных в профиле учетных записей, папка, отображаемая в активном проводнике, не обязательно находится в хранилище по умолчанию для этого сеанса, напротив, она может находиться в одном из нескольких хранилищ, связанных с несколькими учетными записями. В этом разделе показано, как определить учетную запись, хранилище доставки которой по умолчанию является именно тем хранилищем, в котором находится папка.</span><span class="sxs-lookup"><span data-stu-id="135a9-p102">In a Microsoft Outlook session that has multiple accounts defined in the profile, the folder that is displayed in the active explorer does not necessarily reside on the default store for that session; instead, it can reside on one of the multiple stores associated with the multiple accounts. This topic shows how to identify the account whose default delivery store is the same store that hosts the folder.</span></span>

<span data-ttu-id="135a9-110">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="135a9-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="135a9-111">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="135a9-111">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="135a9-112">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="135a9-112">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayAccountForCurrentFolder()
{
    Outlook.Folder myFolder = Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    string msg = "Account for Current Folder:" + "\n" +
        GetAccountForFolder(myFolder).DisplayName;
    MessageBox.Show(msg,
        "GetAccountForFolder",
        MessageBoxButtons.OK,
        MessageBoxIcon.Information);
}

Outlook.Account GetAccountForFolder(Outlook.Folder folder)
{
    // Obtain the store on which the folder resides.
    Outlook.Store store = folder.Store;

    // Enumerate the accounts defined for the session.
    foreach (Outlook.Account account in Application.Session.Accounts)
    {
        // Match the DefaultStore.StoreID of the account
        // with the Store.StoreID for the currect folder.
        if (account.DeliveryStore.StoreID  == store.StoreID)
        {
            // Return the account whose default delivery store
            // matches the store of the given folder.
            return account;
        }
     }
     // No account matches, so return null.
     return null;
}
```

## <a name="see-also"></a><span data-ttu-id="135a9-113">См. также</span><span class="sxs-lookup"><span data-stu-id="135a9-113">See also</span></span>

- [<span data-ttu-id="135a9-114">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="135a9-114">Accounts</span></span>](accounts.md)

