---
title: Отображение диалогового окна "Выбор имен" для сопоставления получателей
TOCTitle: Display the Select Names dialog box to resolve recipients
ms:assetid: 841dd4cd-6d69-46d5-8c83-e28c95b631a9
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646055(v=office.15)
ms:contentKeyID: 55119876
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f92891188e7c317465ce70fede1dedca7f6344fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316067"
---
# <a name="display-the-select-names-dialog-box-to-resolve-recipients"></a><span data-ttu-id="719b4-102">Отображение диалогового окна "Выбор имен" для сопоставления получателей</span><span class="sxs-lookup"><span data-stu-id="719b4-102">Display the Select Names dialog box to resolve recipients</span></span>

<span data-ttu-id="719b4-103">В этом примере предпринимается попытка разрешить получателей, предоставленных параметром *recips*, и выводится диалоговое окно Outlook **Выбор имен** для каждого неоднозначного получателя, которого не удалось разрешить.</span><span class="sxs-lookup"><span data-stu-id="719b4-103">This example attempts to resolve the recipients provided by the *recips* parameter, and displays the Outlook **Select Names** dialog box for each recipient that is ambiguous and cannot be resolved.</span></span>

## <a name="example"></a><span data-ttu-id="719b4-104">Пример</span><span class="sxs-lookup"><span data-stu-id="719b4-104">Example</span></span>

<span data-ttu-id="719b4-105">Код этого примера вызывает объект [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) , чтобы отобразить диалоговое окно **Выбор имен**, показывающее адресную книгу Outlook.</span><span class="sxs-lookup"><span data-stu-id="719b4-105">This code sample calls the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the **Select Names** dialog box which shows the Outlook address book.</span></span> <span data-ttu-id="719b4-106">В этом диалоговом окне пользователь может выбрать имя адресной книги.</span><span class="sxs-lookup"><span data-stu-id="719b4-106">Through this dialog box, the user can select a name from the address book.</span></span> <span data-ttu-id="719b4-107">Если имя не удается разрешить, получатель будет удален из recips.</span><span class="sxs-lookup"><span data-stu-id="719b4-107">If the name is not resolved, the recipient will be removed from recips.</span></span> <span data-ttu-id="719b4-108">Если имя разрешается, то пример кода возвращает в recips объект [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) получателя.</span><span class="sxs-lookup"><span data-stu-id="719b4-108">If the name is resolved, then the code sample will return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object of the recipient to recips.</span></span>

<span data-ttu-id="719b4-109">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="719b4-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="719b4-110">Инструкция **Imports** или **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="719b4-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="719b4-111">В строках кода ниже показано, как выполнить импорт и назначение на Visual Basic и C\#.</span><span class="sxs-lookup"><span data-stu-id="719b4-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ResolveRecipients(ByVal recips As Outlook.Recipients)
    If recips Is Nothing Then
        Throw New ArgumentNullException()
    End If
    If recips.ResolveAll() Then
        Return
    Else
        For i As Integer = recips.Count To 1 Step -1
            If Not (recips(i).Resolve()) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.Recipients.Add(recips(i).Name)
                snd.NumberOfRecipientSelectors = _
                    Outlook.OlRecipientSelectors.olShowTo
                snd.AllowMultipleSelection = False
                snd.Display()
                If Not (snd.Recipients.ResolveAll()) Then
                    recips.Remove(i)
                Else
                    recips.Remove(i)
                    recips.Add(snd.Recipients(1).Address)
                End If
                snd = Nothing
            End If
        Next
    End If
End Sub
```


```csharp
private void ResolveRecipients(Outlook.Recipients recips)
{
    if (recips == null)
    {
        throw new ArgumentNullException();
    }
    if (recips.ResolveAll())
    {
        return;
    }
    else
    {
        for (int i = recips.Count; i > 0; i--)
        {
            if (!recips[i].Resolve())
            {
                Outlook.SelectNamesDialog snd =
                    Application.Session.
                    GetSelectNamesDialog();
                snd.Recipients.Add(recips[i].Name);
                snd.NumberOfRecipientSelectors =
                    Outlook.OlRecipientSelectors.olShowTo;
                snd.AllowMultipleSelection = false;
                snd.Display();
                if (!snd.Recipients.ResolveAll())
                {
                    recips.Remove(i);
                }
                else
                {
                    recips.Remove(i);
                    recips.Add(snd.Recipients[1].Address);
                }
                snd = null;
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="719b4-112">См. также</span><span class="sxs-lookup"><span data-stu-id="719b4-112">See also</span></span>

- [<span data-ttu-id="719b4-113">Получатели</span><span class="sxs-lookup"><span data-stu-id="719b4-113">Recipients</span></span>](recipients.md)

