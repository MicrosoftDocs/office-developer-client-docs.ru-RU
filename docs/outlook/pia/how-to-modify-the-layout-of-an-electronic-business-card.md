---
title: Изменение макета электронной визитной карточки
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0b95621df2e021f52587d5a40d0de43e5505b80c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406437"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Изменение макета электронной визитной карточки

В этом примере показано, как изменить макет электронной визитной карточки с помощью свойства [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) интерфейса [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Электронная визитная карточка  это представление контакта, содержащее конкретную информацию о нем. Интерфейс **ContactItem** предоставляет определенные элементы, относящиеся к электронным визитным карточкам. Ими являются **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) и [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).

В представленном ниже примере кода BusinessCardLayoutExample изменяет макет электронной визитной карточки путем первоначального получения заданного объекта **ContactItem**. В этом случае объект **ContactItem** является контактом со значением свойства [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) равным "Melissa MacBeth". Затем BusinessCardLayoutExample создает класс XML-документа [XmlDocument](https://msdn.microsoft.com/ru-RU/library/6kza7w4k) и получает атрибут структуры этого класса в строке с помощью значения **BusinessCardLayoutXML** для объекта **ContactItem**. После этого макет карточки изменяется с выравнивания по левому краю на выравнивание по правому.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Электронные визитные карточки](electronic-business-cards.md)

