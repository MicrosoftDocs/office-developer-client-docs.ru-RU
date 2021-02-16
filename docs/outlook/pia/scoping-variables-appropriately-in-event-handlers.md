---
title: Правильное задание области применения в обработчиках событий
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c8a1a418a315167cc96be5b9b5f65a0f4cd9ce44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342254"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a><span data-ttu-id="39ac0-102">Правильное задание области применения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="39ac0-102">Scoping variables appropriately in event handlers</span></span>

<span data-ttu-id="39ac0-p101">Распространенной ошибкой при программировании обработчиков событий является подключение обработчика события к объекту, который был объявлен с областью применения, слишком ограниченной для целей обработки этого события. Время жизни объекта не должно ограничиваться только функцией, подключающей метод обратного вызова в качестве обработчика события для объекта, но распространяться и на сам метод обратного вызова, в котором фактически обрабатывается событие. В противном случае, если объект оказывается вне области применения и больше не определен в методе обратного вызова, метод обратного вызова не вызывается и событие не обрабатывается нужным образом.</span><span class="sxs-lookup"><span data-stu-id="39ac0-p101">A common mistake in programming event handlers is connecting the event handler to an object that has been declared with a scope too limited for the purpose of handling the event. The object must have a life that spans not just over the function that connects the callback method as an event handler of the object, but also over the callback method itself where the event is actually handled. Otherwise, if the object is out of scope and is no longer defined in the callback method, the callback method is not called and the event is not handled as desired.</span></span>

<span data-ttu-id="39ac0-106">В следующем примере предпринимается попытка подключить метод обратного вызова MyNewInspector к событию [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="39ac0-106">The following example attempts to connect the MyNewInspector callback method to the [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)) event.</span></span> <span data-ttu-id="39ac0-107">Но метод обратного вызова в примере кода подключается к событию NewInspector объекта [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)), область применения которого ограничена функцией Connect.</span><span class="sxs-lookup"><span data-stu-id="39ac0-107">However, the callback method is hooked up in the code sample to the NewInspector event of an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) object that has a scope limited to the Connect function.</span></span> <span data-ttu-id="39ac0-108">В результате, когда вызывается метод обратного вызова, программа уже вышла из функции Connect, объект Inspectors уже уничтожен сборщиком мусора, и поэтому MyNewInspector никогда не вызывается.</span><span class="sxs-lookup"><span data-stu-id="39ac0-108">When the callback method is eventually called, the Connect function has already exited, the Inspectors object has already been garbage collected, and so MyNewInspector is never called.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyApp.Inspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

<span data-ttu-id="39ac0-p103">В этом случае правильно будет сохранить объект Inspectors в более длительной переменной, чей срок жизни охватывает весь MyClass, включая метод обратного вызова MyNewInspector. В следующем примере область применения MyInspectors охватывает весь MyClass и обеспечивается подключение обратного вызова в течение времени жизни класса.</span><span class="sxs-lookup"><span data-stu-id="39ac0-p103">The correct thing to do in this case is to store the Inspectors object in a more permanent variable whose lifetime spans over the entire MyClass, including the MyNewInspector callback method. In the following example, MyInspectors has a scope of the entire MyClass and ensures that the callback method is connected for the lifetime of the class.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

class MyClass
{
    private Outlook.Application MyApp;
    private Outlook.Inspectors MyInspectors;

    public MyClass(Outlook.Application appOutlook)
    {
        MyApp = appOutlook;
    }

    // Connects the NewInspector event to my callback method
    public void Connect()
    {
        MyInspectors = MyApp.Inspectors;
        MyInspectors.NewInspector += new Outlook.
            InspectorsEvents_NewInspectorEventHandler(
            MyNewInspector);
    }

    public void MyNewInspector(Outlook.Inspector inspector)
    {
        MessageBox.Show("
            My event handler caught a NewInspector event");
    }
}
```

<br/>

<span data-ttu-id="39ac0-111">Благодаря синтаксическим различиям подключений обработчиков событий в различных языках эта проблема менее распространена в таких языках, как Visual Basic, где можно подключить событие, задавая экземпляр родительского объекта, и одновременно определить метод обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="39ac0-111">By virtue of the syntactic differences in how various languages connect event handlers, this issue is less common in languages such as Visual Basic where you can connect an event specifying an instance of the parent object, and define the callback method at the same time.</span></span> <span data-ttu-id="39ac0-112">В следующем примере на Visual Basic ключевое слово Handles используется для подключения метода обратного вызова Region\_Expanded к событию [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="39ac0-112">The following example in Visual Basic uses the Handles keyword to connect the Region\_Expanded callback method to the [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)) event.</span></span> <span data-ttu-id="39ac0-113">Область применения экземпляра родительского объекта, Region, охватывает MyClass, включая метод обратного вызова Region\_Expanded.</span><span class="sxs-lookup"><span data-stu-id="39ac0-113">An instance of the parent object, Region, has a scope that spans MyClass including the Region\_Expanded callback method.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Public Class MyClass
    ' The Region object has a lifetime spanning the class 
    ' including the callback method Region_Expanded
    Private WithEvents Region As Outlook.FormRegion
    ...
    Private Sub Region_Expanded() Handles Region.Expanded
        MsgBox("My EventHandler caught an Expanded event.")
    End Sub
End Class
```

<span data-ttu-id="39ac0-114">В этом примере метод обратного вызова вызывается правильным образом, так как метод обратного вызова Region\_Expanded подключается к событию Expanded в течение времени жизни класса.</span><span class="sxs-lookup"><span data-stu-id="39ac0-114">In this example, because the Region\_Expanded callback method is connected to the Expanded event for the lifetime of the class, the callback method is called as appropriate.</span></span>

## <a name="see-also"></a><span data-ttu-id="39ac0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="39ac0-115">See also</span></span>

- [<span data-ttu-id="39ac0-116">Подключение к настраиваемым обработчикам событий</span><span class="sxs-lookup"><span data-stu-id="39ac0-116">Connecting to custom event handlers</span></span>](connecting-to-custom-event-handlers.md)

