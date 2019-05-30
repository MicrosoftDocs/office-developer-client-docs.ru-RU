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
# <a name="get-the-global-address-list-or-a-set-of-address-lists-for-a-store"></a><span data-ttu-id="b894c-102">Получение глобального списка адресов или набора списков адресов для хранилища</span><span class="sxs-lookup"><span data-stu-id="b894c-102">Get the Global Address List or a set of address lists for a store</span></span>

<span data-ttu-id="b894c-103">В этом разделе приведены два примера кода, в которых демонстрируется получение глобального списка адресов (GAL), связанного с хранилищем, а также способ получения всех списков адресов, которые с ним связаны.</span><span class="sxs-lookup"><span data-stu-id="b894c-103">This topic contains two code examples that show how to get the Global Address List (GAL) that is associated with a store, and how to get all of the address lists that are associated with a store.</span></span>

## <a name="example"></a><span data-ttu-id="b894c-104">Пример</span><span class="sxs-lookup"><span data-stu-id="b894c-104">Example</span></span>

<span data-ttu-id="b894c-105">Во время сеанса Outlook, где в профиле определены несколько учетных записей Exchange, с хранилищем может быть связано несколько списков адресов.</span><span class="sxs-lookup"><span data-stu-id="b894c-105">In an Outlook session where multiple Exchange accounts are defined in the profile, there can be multiple address lists associated with a store.</span></span> <span data-ttu-id="b894c-106">В каждом из следующих примеров кода хранилищем, о котором идет речь, является хранилище для текущей папки, показанное в активном окне проводника, но алгоритм получения глобального списка адресов или набора объектов [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) для хранилища применяется к любому хранилищу Exchange.</span><span class="sxs-lookup"><span data-stu-id="b894c-106">In each of the following code examples, the specific store of interest is the store for the current folder displayed in the active explorer, but the algorithm to get a Global Address List or a set of [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) objects for a store applies to any Exchange store.</span></span>

<span data-ttu-id="b894c-107">В первом примере кода используется метод DisplayGlobalAddressListForStore и функция GetGlobalAddressList.</span><span class="sxs-lookup"><span data-stu-id="b894c-107">The first code example contains the DisplayGlobalAddressListForStore method and the GetGlobalAddressList function.</span></span> <span data-ttu-id="b894c-108">Метод DisplayGlobalAddressListForStore отображает в диалоговом окне **Выбор имен** глобальный список адресов, связанный с текущим хранилищем.</span><span class="sxs-lookup"><span data-stu-id="b894c-108">The DisplayGlobalAddressListForStore method displays, in the **Select Names** dialog box, the Global Address List that is associated with the current store.</span></span> <span data-ttu-id="b894c-109">Метод DisplayGlobalAddressListForStore сначала получает текущее хранилище.</span><span class="sxs-lookup"><span data-stu-id="b894c-109">DisplayGlobalAddressListForStore first obtains the current store.</span></span> <span data-ttu-id="b894c-110">Если текущее хранилище является хранилищем Exchange, вызывается функция GetGlobalAddressList для получения глобального списка адресов, связанного с текущим хранилищем.</span><span class="sxs-lookup"><span data-stu-id="b894c-110">If the current store is an Exchange store, GetGlobalAddressList is called to obtain the Global Address List associated with the current store.</span></span> 

<span data-ttu-id="b894c-111">Функция GetGlobalAddressList использует объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) и свойство MAPI http://schemas.microsoft.com/mapi/proptag/0x3D150102 для получения свойства PR\_EMSMDB\_SECTION\_UID списка адресов и текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b894c-111">GetGlobalAddressList uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object and the MAPI property http://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list and the current store.</span></span> <span data-ttu-id="b894c-112">Функция GetGlobalAddressList определяет, что список адресов связан с хранилищем, если их свойства PR\_EMSMDB\_SECTION\_UID совпадают, и что это глобальный список адресов, если его свойство [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) имеет значение [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="b894c-112">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and the address list is the Global Address List if its [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) property is [olExchangeGlobalAddressList](https://msdn.microsoft.com/library/bb644009\(v=office.15\)).</span></span> <span data-ttu-id="b894c-113">Если вызов GetGlobalAddressList выполняется успешно, метод DisplayGlobalAddressListForStore использует объект [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) для отображения возвращаемого глобального списка адресов в диалоговом окне **Выбор имен**.</span><span class="sxs-lookup"><span data-stu-id="b894c-113">If the call to GetGlobalAddressList succeeds, DisplayGlobalAddressListForStore uses the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the returned Global Address List in the **Select Names** dialog box.</span></span>

<span data-ttu-id="b894c-114">Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b894c-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b894c-115">Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="b894c-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b894c-116">В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="b894c-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

<span data-ttu-id="b894c-117">Во втором примере кода используется метод EnumerateAddressListsForStore и функция GetAddressLists.</span><span class="sxs-lookup"><span data-stu-id="b894c-117">The second code example contains the EnumerateAddressListsForStore method and GetAddressLists function.</span></span> <span data-ttu-id="b894c-118">Метод EnumerateAddressListsForStore показывает тип и порядок разрешения каждого списка адресов, определенного для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b894c-118">The EnumerateAddressListsForStore method displays the type and resolution order of each address list defined for the current store.</span></span> <span data-ttu-id="b894c-119">EnumerateAddressListsForStore сначала получает сведения о текущем хранилище, а затем вызывает GetAddressLists, чтобы получить универсальный объект платформы .NET Framework [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19), который содержит объекты AddressList для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b894c-119">EnumerateAddressListsForStore first obtains the current store, and then calls GetAddressLists to obtain a .NET Framework generic [List\<T\>](https://msdn.microsoft.com/en-us/library/6sh2ey19) object that contains AddressList objects for the current store.</span></span> 

<span data-ttu-id="b894c-120">GetAddressLists перечисляет каждый список адресов, определенный для этого сеанса, использует объект PropertyAccessor и именованное свойство MAPI http://schemas.microsoft.com/mapi/proptag/0x3D150102 для получения свойства PR\_EMSMDB\_SECTION\_UID для списка адресов и свойства PR\_EMSMDB\_SECTION\_UID текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b894c-120">GetAddressLists enumerates each address list defined for the session, uses the PropertyAccessor object and the MAPI named property http://schemas.microsoft.com/mapi/proptag/0x3D150102 to obtain the PR\_EMSMDB\_SECTION\_UID property of an address list, and the PR\_EMSMDB\_SECTION\_UID property of a current store.</span></span> <span data-ttu-id="b894c-121">GetGlobalAddressList определяет, что список адресов связан с хранилищем, если их свойства PR\_EMSMDB\_SECTION\_UID совпадают, и выводит набор списков адресов для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b894c-121">GetGlobalAddressList identifies an address list as associated with a store if their PR\_EMSMDB\_SECTION\_UID properties match, and returns a set of address lists for the current store.</span></span> <span data-ttu-id="b894c-122">Затем EnumerateAddressListsForStore применяет свойства [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) и [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) объекта **AddressList**, чтобы показать тип и порядок разрешения для каждого возвращенного списка адресов.</span><span class="sxs-lookup"><span data-stu-id="b894c-122">EnumerateAddressListsForStore then uses the [AddressListType](https://msdn.microsoft.com/library/bb610942\(v=office.15\)) and [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)) properties of the **AddressList** object to display the type and resolution order for each returned address list.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b894c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b894c-123">See also</span></span>

- [<span data-ttu-id="b894c-124">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="b894c-124">Address book</span></span>](address-book.md)

