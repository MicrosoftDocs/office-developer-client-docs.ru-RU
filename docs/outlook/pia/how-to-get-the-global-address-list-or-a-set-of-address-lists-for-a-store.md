---
title: Получение глобального списка адресов или набора списков адресов для хранилища
TOCTitle: Get the Global Address List or a set of address lists for a store
ms:assetid: a361ac58-25c6-4ce1-97b0-403ad67ee7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184631(v=office.15)
ms:contentKeyID: 55119800
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 677325df863e5b5a52856abb01f55bdb8884bbe8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542529"
---
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a>Получение глобального списка адресов или набора списков адресов для хранилища

В этом разделе приведены два примера кода, в которых демонстрируется получение глобального списка адресов (GAL), связанного с хранилищем, а также способ получения всех списков адресов, которые с ним связаны.

## <a name="example"></a>Пример

Во время сеанса Outlook, где в профиле определены несколько учетных записей Exchange, с хранилищем может быть связано несколько списков адресов. В каждом из следующих примеров кода хранилищем, о котором идет речь, является хранилище для текущей папки, показанное в активном окне проводника, но алгоритм получения глобального списка адресов или набора объектов [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) для хранилища применяется к любому хранилищу Exchange.

В первом примере кода используется метод DisplayGlobalAddressListForStore и функция GetGlobalAddressList. Метод DisplayGlobalAddressListForStore отображает в диалоговом окне **Выбор имен** глобальный список адресов, связанный с текущим хранилищем. Метод DisplayGlobalAddressListForStore сначала получает текущее хранилище. Если текущее хранилище является хранилищем Exchange, вызывается функция GetGlobalAddressList для получения глобального списка адресов, связанного с текущим хранилищем. 

Функция GetGlobalAddressList использует объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) и свойство MAPI http://schemas.microsoft.com/mapi/proptag/0x3D150102 для получения свойства PR\_EMSMDB\_SECTION\_UID списка адресов и текущего хранилища. Функция GetGlobalAddressList определяет, что список адресов связан с хранилищем, если их свойства PR\_EMSMDB\_SECTION\_UID совпадают, и что это глобальный список адресов, если его свойство [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) имеет значение [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)). Если вызов GetGlobalAddressList выполняется успешно, метод DisplayGlobalAddressListForStore использует объект [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) для отображения возвращаемого глобального списка адресов в диалоговом окне **Выбор имен**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
void DisplayGlobalAddressListForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    if (currentStore.ExchangeStoreType !=
        Outlook.OlExchangeStoreType.olNotExchange)
    {
        Outlook.SelectNamesDialog snd = 
            Application.Session.GetSelectNamesDialog();
        Outlook.AddressList addrList = 
            GetGlobalAddressList(currentStore);
        if (addrList != null)
        {
            snd.InitialAddressList = addrList;
            snd.Display();
        }
    }
}

public Outlook.AddressList GetGlobalAddressList(Outlook.Store store)
{
    string  PR_EMSMDB_SECTION_UID = 
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList 
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList = 
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID && addrList.AddressListType ==
            Outlook.OlAddressListType.olExchangeGlobalAddressList)
        {
            return addrList;
        }
    }
    return null;
}
```

Во втором примере кода используется метод EnumerateAddressListsForStore и функция GetAddressLists. Метод EnumerateAddressListsForStore показывает тип и порядок разрешения каждого списка адресов, определенного для текущего хранилища. EnumerateAddressListsForStore сначала получает сведения о текущем хранилище, а затем вызывает GetAddressLists, чтобы получить универсальный объект платформы .NET Framework [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19), который содержит объекты AddressList для текущего хранилища. 

GetAddressLists перечисляет каждый список адресов, определенный для этого сеанса, использует объект PropertyAccessor и именованное свойство MAPI http://schemas.microsoft.com/mapi/proptag/0x3D150102 для получения свойства PR\_EMSMDB\_SECTION\_UID для списка адресов и свойства PR\_EMSMDB\_SECTION\_UID текущего хранилища. GetGlobalAddressList определяет, что список адресов связан с хранилищем, если их свойства PR\_EMSMDB\_SECTION\_UID совпадают, и выводит набор списков адресов для текущего хранилища. Затем EnumerateAddressListsForStore применяет свойства [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) и [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) объекта **AddressList**, чтобы показать тип и порядок разрешения для каждого возвращенного списка адресов.

```csharp
private void EnumerateAddressListsForStore()
{
    Outlook.Folder currentFolder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store currentStore = currentFolder.Store;
    List<Outlook.AddressList> addrListsForStore = 
        GetAddressLists(currentStore);
    foreach (Outlook.AddressList addrList in addrListsForStore)
    {
        Debug.WriteLine(addrList.Name 
            + " " + addrList.AddressListType.ToString()
            + " Resolution Order: " +
            addrList.ResolutionOrder);
    }
}
public List<Outlook.AddressList> GetAddressLists(Outlook.Store store)
{
    List<Outlook.AddressList> addrLists = 
        new List<Microsoft.Office.Interop.Outlook.AddressList>();
    string PR_EMSMDB_SECTION_UID =
        @"http://schemas.microsoft.com/mapi/proptag/0x3D150102";
    if (store == null)
    {
        throw new ArgumentNullException();
    }
    Outlook.PropertyAccessor oPAStore = store.PropertyAccessor;
    string storeUID = oPAStore.BinaryToString(
        oPAStore.GetProperty(PR_EMSMDB_SECTION_UID));
    foreach (Outlook.AddressList addrList
        in Application.Session.AddressLists)
    {
        Outlook.PropertyAccessor oPAAddrList =
            addrList.PropertyAccessor;
        string addrListUID = oPAAddrList.BinaryToString(
            oPAAddrList.GetProperty(PR_EMSMDB_SECTION_UID));
        // Return addrList if match on storeUID
        // and type is olExchangeGlobalAddressList.
        if (addrListUID == storeUID)
        {
            addrLists.Add(addrList);
        }
    }
    return addrLists;
}
```

## <a name="see-also"></a>См. также

- [Адресная книга](address-book.md)

