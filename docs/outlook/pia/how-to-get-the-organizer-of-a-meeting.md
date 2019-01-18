---
title: Получение организатора собрания
TOCTitle: Get the organizer of a meeting
ms:assetid: 6a33db84-573b-4d1b-a91a-903f30630ec9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184615(v=office.15)
ms:contentKeyID: 55119872
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b34b79ac05530ec30e611c50bce8e81ce0470f02
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699557"
---
# <a name="get-the-organizer-of-a-meeting"></a>Получение организатора собрания

В этом примере показано, как программным способом вернуть организатора собрания.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

В следующем примере кода метод GetMeetingOrganizer принимает параметр типа [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)), который представляет собрание, и использует объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) и метод [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) для получения элемента [EntryID](https://msdn.microsoft.com/library/bb645980\(v=office.15\)) для объекта **AppointmentItem**. После получения элемента **EntryID** в примере используется метод [GetAddressEntryFromID(String)](https://msdn.microsoft.com/library/ff185034\(v=office.15\)), чтобы вернуть объект [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)), представляющий организатора собрания.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private Outlook.AddressEntry GetMeetingOrganizer(Outlook.AppointmentItem appt)
{
    if (appt == null)
    {
        throw new ArgumentNullException();
    }
    string PR_SENT_REPRESENTING_ENTRYID =
        @"https://schemas.microsoft.com/mapi/proptag/0x00410102";
    string organizerEntryID =
        appt.PropertyAccessor.BinaryToString(
            appt.PropertyAccessor.GetProperty(
            PR_SENT_REPRESENTING_ENTRYID));
    Outlook.AddressEntry organizer =
        Application.Session.
        GetAddressEntryFromID(organizerEntryID);
    if (organizer != null)
    {
        return organizer; 
    }
    else
    {
        return null;
    }
}
```

## <a name="see-also"></a>См. также

- [Приглашения на собрания](meeting-requests.md)

