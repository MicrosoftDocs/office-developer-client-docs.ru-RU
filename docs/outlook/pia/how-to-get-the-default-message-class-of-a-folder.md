---
title: Получение класса сообщений по умолчанию для папки
TOCTitle: Get the default message class of a folder
ms:assetid: 1c5faefd-b180-4114-a955-3fc524210317
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184594(v=office.15)
ms:contentKeyID: 55119860
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bef6ebe051e669b831dfee752b1b17db0a9023b8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705276"
---
# <a name="get-the-default-message-class-of-a-folder"></a>Получение класса сообщений по умолчанию для папки

В этом примере показано, как использовать свойство [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)) для получения класса сообщений по умолчанию для папки.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода представляет собой фрагмент из книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Для получения класса сообщений по умолчанию для папки используйте свойство **DefaultMessageClass** объекта [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)). Например, наличие у объекта [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) свойства **DefaultMessageClass**, равного IPM.Contact, означает, что этот объект представляет папку контакта. Но если для папки в качестве формы по умолчанию задана настраиваемая форма или заменяющая форма, необходимо использовать объект [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) , чтобы определить класс сообщения формы по умолчанию. Свойство **DefaultMessageClass** не возвращает класс сообщения формы по умолчанию для папки.

В следующем примере кода процедура GetDefaultMessageClass использует **PropertyAccessor**, чтобы определить для папки форму по умолчанию. Если свойство папки **связей с Общественностью\_DEF\_POST\_MSGCLASS** [(PidTagDefaultPostMessageClass)](https://msdn.microsoft.com/library/cc815305\(v=office.15\)) не найден и Outlook вызывает ошибку, блок **try... catch** возвращает свойство **DefaultMessageClass** **Папка**.

Если вы используете Visual Studio для тестирования этого примера кода, сначала добавьте ссылку на компонент Microsoft Outlook 15.0 Object Library и задайте переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Инструкция **using** не должна идти непосредственно перед функциями в примере кода, но ее нужно добавить перед открытым объявлением Class. В следующей строке кода показано, как выполнить импорт и назначение в C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetDefaultMessageClass(Outlook.Folder folder)
{
    if (folder == null)
        throw new ArgumentNullException();
    try
    {
        const string PR_DEF_POST_MSGCLASS =
            @"https://schemas.microsoft.com/mapi/proptag/0x36E5001E";
        string messageClass =
            folder.PropertyAccessor.GetProperty(
            PR_DEF_POST_MSGCLASS).ToString();
        return messageClass;
    }
    catch
    {
        return folder.DefaultMessageClass;
    }
}
```

## <a name="see-also"></a>См. также

- [Папки](folders.md)

