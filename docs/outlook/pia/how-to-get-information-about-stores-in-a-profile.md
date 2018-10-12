---
title: Получение сведений о магазинах в профиле
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0229294cd6655f9017780ee0d9a7a23de76f2362
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406570"
---
# <a name="get-information-about-stores-in-a-profile"></a>Получение сведений о магазинах в профиле

В этом примере показано, как получить магазины в профиле и выполнить их перечисление.

## <a name="example"></a>Пример

> [!NOTE] 
> Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").

Вы можете использовать коллекцию [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)), чтобы выполнить перечисление магазинов в заданном профиле. В коллекции **Stores** содержатся элементы, предоставляющие сведения о каждом объекте [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , например о дате добавления объекта **Store** или планируемой дате удаления объекта **Store** из текущего профиля. В примере кода ниже метод EnumerateStores получает объект **Stores**, представляющий магазины в текущем профиле, и выполняет перечисление магазинов. Метод EnumerateStores проверяет каждый объект **Store** в коллекции **Stores**. Если свойство [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) возвращает значение **true**, определяющее хранилище в формате PST или OST, свойства [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) и [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) записываются в прослушиватели трассировки в коллекции [Прослушиватели](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).

Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**. Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса. В строке кода ниже показано, как выполнить импорт и назначение на языке C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a>См. также

- [Stores](stores.md)

