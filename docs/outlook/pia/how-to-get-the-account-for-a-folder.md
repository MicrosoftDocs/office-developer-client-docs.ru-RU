---
title: Получение учетной записи для папки
TOCTitle: Get the account for a folder
ms:assetid: 3706be15-f746-4d0d-9ffe-d6f46b2004dc
ms:contentKeyID: 55119793
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8f56f866e71b1080d5b7a6a33fb17e3e71ab9199
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708097"
---
# <a name="get-the-account-for-a-folder"></a>Получение учетной записи для папки

В этом примере показано получение учетной записи, которая связана с папкой в текущем сеансе.

## <a name="example"></a>Пример

В следующем примере кода функция DisplayAccountForCurrentFolder вызывает функцию GetAccountForFolder, чтобы определить учетную запись, хранилище доставки по умолчанию для которой содержит текущую папку, а затем отображает имя папки. GetAccountForFolder сопоставляет хранилище текущей папки (полученной из свойства [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) с хранилищем доставки по умолчанию каждой учетной записи (полученным с помощью свойства [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))), определенного в коллекции [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) для сеанса. GetAccountForFolder возвращает объект [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)), если соответствие найдено, в противном случае функция возвращает пустую ссылку (NULL).

В сеансе Microsoft Outlook, использующем несколько определенных в профиле учетных записей, папка, отображаемая в активном проводнике, не обязательно находится в хранилище по умолчанию для этого сеанса, напротив, она может находиться в одном из нескольких хранилищ, связанных с несколькими учетными записями. В этом разделе показано, как определить учетную запись, хранилище доставки которой по умолчанию является именно тем хранилищем, в котором находится папка.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

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

## <a name="see-also"></a>См. также

- [Учетные записи](accounts.md)

