---
title: Создание списка рассылки
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 19b282a3b3e756814aa2add07cda4be7609206ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407137"
---
# <a name="create-a-distribution-list"></a>Создание списка рассылки

В этом примере показано, как создать список рассылки и отобразить его пользователю.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


В следующем примере кода CreateDistributionList создает список рассылки путем вызова метода [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) для создания объекта [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)). Затем создается объект [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) и вызывается метод [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) для поиска всех контактов в выбранной по умолчанию папке "Контакты", свойство которой [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) имеет значение "Top Customer" (лучший клиент), а значение свойства [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) не является пустым. После определения всех контактов имя **Email1Address** добавляется в качестве столбца в объект **Table**. Затем с помощью CreateDistributionList создается объект [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) путем применения метода [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) из объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). Наконец, CreateDistributionList показывает пользователю список рассылки "Top Customers" (лучшие клиенты).

> [!NOTE] 
> Необходимо передать разрешенный объект **Recipient** в качестве параметра для метода [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) объекта [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)). Чтобы разрешить объект **Recipient**, используйте метод [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a>См. также

- [Пользователи Exchange](exchange-users.md)

