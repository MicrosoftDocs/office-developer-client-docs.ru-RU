---
title: Отображение общего календаря получателя
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9230a63af66e8143a7da488ce41dadafe359429
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709217"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a>Отображение общего календаря получателя

В этом примере показано, как отобразить общий календарь получателя c помощью методов [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) и [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

Отправляемые элементы, такие как объекты [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) , всегда предоставляют свойство [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) , которое, в свою очередь, позволяет получать доступ к коллекции [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) для отправляемого элемента. Чтобы создать объект [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) , который не связан с коллекцией **Recipients** элемента, используется метод [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) объекта [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) . Затем этот несвязанный объект **Recipient** передается в метод [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) , который возвращает общую папку Exchange. Далее можно открыть общую папку Exchange и отобразить эту папку в окне проводника. GetSharedDefaultFolder используется при делегировании в Exchange, когда делегат обладает разрешением на доступ к папке представителя. Перед передачей объекта **Recipient** в метод GetSharedDefaultFolder необходимо разрешить его. Чтобы разрешить объект **Recipient**, вызовите его метод [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) .

В следующем примере кода DisplayManagerCalendar открывает и отображает папку "Календарь" руководителя текущего пользователя, вызывая **CreateRecipient** и **GetSharedDefaultFolder**. Если у пользователя отсутствует разрешение на открытие папки "Календарь" руководителя или в случае ошибки, появляется диалоговое окно оповещения. 


> [!NOTE]
> При создании объекта **Recipient** с помощью метода **CreateRecipient** объекта **Namespace** или метода [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) коллекции **Recipients** необходимо предоставить имя получателя. Затем объект **Recipient** разрешается по этому имени. Имя получателя может быть представлено в любом из следующих форматов:
> - отображаемое имя;
> - псевдоним;
> - SMTP-адрес.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна находиться непосредственно перед функциями в примере кода, но ее нужно добавить перед объявлением общедоступного класса. В приведенной ниже строке кода показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Календарь](calendar.md)

