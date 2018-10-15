---
title: Получение участников списка рассылки Exchange
TOCTitle: Get members of an Exchange distribution list
ms:assetid: 75b38e40-772c-400b-8df9-e3e385b87f9c
ms:mtpsurl: https://msdn.microsoft.com/library/Bb645998(v=office.15)
ms:contentKeyID: 55119837
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 730ef62b6bff9cbfc2bf4aaae51116d2fe026131
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406563"
---
# <a name="get-members-of-an-exchange-distribution-list"></a><span data-ttu-id="2b54b-102">Получение участников списка рассылки Exchange</span><span class="sxs-lookup"><span data-stu-id="2b54b-102">Get members of an Exchange distribution list</span></span>

<span data-ttu-id="2b54b-103">В этом примере пользователю отображается запрос на выбор списка рассылки Exchange в диалоговом окне **Выбор имен**, после чего этот список рассылки развертывается для отображения его членов.</span><span class="sxs-lookup"><span data-stu-id="2b54b-103">This example prompts the user to select an Exchange distribution list from the **Select Names** dialog box and expands the distribution list to display its members.</span></span>

## <a name="example"></a><span data-ttu-id="2b54b-104">Пример</span><span class="sxs-lookup"><span data-stu-id="2b54b-104">Example</span></span>

<span data-ttu-id="2b54b-p101">В коде этого примера вызывается метод [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) объекта [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) , чтобы получить коллекцию [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) , содержащую все члены списка. Так как списки рассылки могут быть вложены в другой список рассылки, возвращенная коллекция **AddressEntries** может представлять любой тип объекта Exchange [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="2b54b-p101">This code sample calls the [GetExchangeDistributionListMembers](https://msdn.microsoft.com/library/bb647622\(v=office.15\)) method of the [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that contains all the members of the list. Because distribution lists can be nested inside another distribution list, the returned **AddressEntries** collection can represent any type of Exchange [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span>


> [!NOTE]
> <span data-ttu-id="2b54b-p102">Развертывание списков рассылки может повысить нагрузку на сервер Exchange, поэтому используйте метод **GetExchangeDistributionListMembers** осторожно. Надо учитывать, что при развертывании больших списков рассылки выполнение кода может занять продолжительное время.</span><span class="sxs-lookup"><span data-stu-id="2b54b-p102">Expanding distribution lists can create a performance burden on an Exchange server, so use the **GetExchangeDistributionListMembers** method cautiously. Expect that your code will be slow when it expands large distribution lists.</span></span>

<span data-ttu-id="2b54b-109">Чтобы получить участников списка рассылки, пользователь должен быть подключен к серверу Exchange и находиться в сети.</span><span class="sxs-lookup"><span data-stu-id="2b54b-109">To obtain the members of a distribution list, the user must be connected to an Exchange server and online.</span></span>

<span data-ttu-id="2b54b-110">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="2b54b-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="2b54b-111">Не следует использовать инструкции **Imports** и **using** непосредственно перед функциями в примере кода, но их необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="2b54b-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="2b54b-112">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="2b54b-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub GetDistributionListMembers()
    Dim snd As Outlook.SelectNamesDialog = _
        Application.Session.GetSelectNamesDialog()
    Dim addrLists As Outlook.AddressLists = _
        Application.Session.AddressLists
    For Each addrList As Outlook.AddressList In addrLists
        If addrList.Name = "All Groups" Then
            snd.InitialAddressList = addrList
            Exit For
        End If
    Next
    snd.NumberOfRecipientSelectors = _
        Outlook.OlRecipientSelectors.olShowTo
    snd.ToLabel = "D/L"
    snd.ShowOnlyInitialAddressList = True
    snd.AllowMultipleSelection = False
    snd.Display()
    If (snd.Recipients.Count > 0) Then
        Dim addrEntry As Outlook.AddressEntry = _
            snd.Recipients(1).AddressEntry
        If (addrEntry.AddressEntryUserType = _
            Outlook.OlAddressEntryUserType. _
            olExchangeDistributionListAddressEntry) Then
            Dim exchDL As Outlook.ExchangeDistributionList = _
                addrEntry.GetExchangeDistributionList()
            Dim addrEntries As Outlook.AddressEntries = _
                exchDL.GetExchangeDistributionListMembers()
            If Not (addrEntries Is Nothing) Then
                For Each exchDLMember As _
                    Outlook.AddressEntry In addrEntries
                    Debug.WriteLine(exchDLMember.Name)
                Next
            End If
         End If
    End If
End Sub
```


```csharp
private void GetDistributionListMembers()
{
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    Outlook.AddressLists addrLists =
        Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        if (addrList.Name == "All Groups")
        {
            snd.InitialAddressList = addrList;
            break;
        }
    }
    snd.NumberOfRecipientSelectors =
        Outlook.OlRecipientSelectors.olShowTo;
    snd.ToLabel = "D/L";
    snd.ShowOnlyInitialAddressList = true;
    snd.AllowMultipleSelection = false;
    snd.Display();
    if (snd.Recipients.Count > 0)
    {
        Outlook.AddressEntry addrEntry =
            snd.Recipients[1].AddressEntry;
        if (addrEntry.AddressEntryUserType ==
            Outlook.OlAddressEntryUserType.
            olExchangeDistributionListAddressEntry)
        {
            Outlook.ExchangeDistributionList exchDL =
                addrEntry.GetExchangeDistributionList();
            Outlook.AddressEntries addrEntries =
                exchDL.GetExchangeDistributionListMembers();
            if (addrEntries != null)
                foreach (Outlook.AddressEntry exchDLMember
                    in addrEntries)
                {
                    Debug.WriteLine(exchDLMember.Name);
                }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2b54b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2b54b-113">See also</span></span>

- [<span data-ttu-id="2b54b-114">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="2b54b-114">Exchange Users</span></span>](exchange-users.md)

