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
# <a name="get-information-about-stores-in-a-profile"></a><span data-ttu-id="99010-102">Получение сведений о магазинах в профиле</span><span class="sxs-lookup"><span data-stu-id="99010-102">Get information about stores in a profile</span></span>

<span data-ttu-id="99010-103">В этом примере показано, как получить магазины в профиле и выполнить их перечисление.</span><span class="sxs-lookup"><span data-stu-id="99010-103">This example shows how to get and enumerate stores in a profile.</span></span>

## <a name="example"></a><span data-ttu-id="99010-104">Пример</span><span class="sxs-lookup"><span data-stu-id="99010-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="99010-105">Приведенный ниже пример кода взят из книги [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) ("Программирование приложений для Microsoft Office Outlook 2007").</span><span class="sxs-lookup"><span data-stu-id="99010-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="99010-106">Вы можете использовать коллекцию [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)), чтобы выполнить перечисление магазинов в заданном профиле.</span><span class="sxs-lookup"><span data-stu-id="99010-106">You can use the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to enumerate the stores for a given profile.</span></span> <span data-ttu-id="99010-107">В коллекции **Stores** содержатся элементы, предоставляющие сведения о каждом объекте [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , например о дате добавления объекта **Store** или планируемой дате удаления объекта **Store** из текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="99010-107">The **Stores** collection provides members that expose information about each [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, such as when a **Store** object has been added or when a **Store** object is about to be removed in the current profile.</span></span> <span data-ttu-id="99010-108">В примере кода ниже метод EnumerateStores получает объект **Stores**, представляющий магазины в текущем профиле, и выполняет перечисление магазинов.</span><span class="sxs-lookup"><span data-stu-id="99010-108">In the following code example,   gets the Stores object that represents stores in the current profile, and enumerates the stores.</span></span> <span data-ttu-id="99010-109">Метод EnumerateStores проверяет каждый объект **Store** в коллекции **Stores**.</span><span class="sxs-lookup"><span data-stu-id="99010-109"> examines each Store object in the Stores collection.</span></span> <span data-ttu-id="99010-110">Если свойство [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) возвращает значение **true**, определяющее хранилище в формате PST или OST, свойства [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) и [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) записываются в прослушиватели трассировки в коллекции [Прослушиватели](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx).</span><span class="sxs-lookup"><span data-stu-id="99010-110">If the [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) property returns **true**, indicating that it is a .pst or .ost store, the [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) and [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) properties are written to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="99010-111">Если для тестирования этого примера кода вы используете Visual Studio, сначала добавьте ссылку на компонент библиотеки объектов Microsoft Outlook 15.0 и укажите переменную Outlook при импорте пространства имен **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="99010-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="99010-112">Не следует использовать инструкцию **using** непосредственно перед функциями в примере кода, но ее необходимо добавить перед объявлением общедоступного класса.</span><span class="sxs-lookup"><span data-stu-id="99010-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="99010-113">В строке кода ниже показано, как выполнить импорт и назначение на языке C\#.</span><span class="sxs-lookup"><span data-stu-id="99010-113">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="99010-114">См. также</span><span class="sxs-lookup"><span data-stu-id="99010-114">See also</span></span>

- [<span data-ttu-id="99010-115">Stores</span><span class="sxs-lookup"><span data-stu-id="99010-115">Stores</span></span>](stores.md)

