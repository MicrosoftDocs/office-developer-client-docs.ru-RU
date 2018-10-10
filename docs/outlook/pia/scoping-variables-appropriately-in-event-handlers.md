---
title: Правильное задание области применения в обработчиках событий
TOCTitle: Scoping variables appropriately in event handlers
ms:assetid: 95b71535-abfd-43f1-a471-2026b522eac1
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646475(v=office.15)
ms:contentKeyID: 55119788
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: ac26dfb245dd9b4621093a91ff36846c686f6e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407606"
---
# <a name="scoping-variables-appropriately-in-event-handlers"></a>Правильное задание области применения в обработчиках событий

Распространенной ошибкой при программировании обработчиков событий является подключение обработчика события к объекту, который был объявлен с областью применения, слишком ограниченной для целей обработки этого события. Время жизни объекта не должно ограничиваться только функцией, подключающей метод обратного вызова в качестве обработчика события для объекта, но распространяться и на сам метод обратного вызова, в котором фактически обрабатывается событие. В противном случае, если объект оказывается вне области применения и больше не определен в методе обратного вызова, метод обратного вызова не вызывается и событие не обрабатывается нужным образом.

В следующем примере предпринимается попытка подключить метод обратного вызова MyNewInspector к событию [NewInspector](https://msdn.microsoft.com/library/bb612750\(v=office.15\)). Но метод обратного вызова в примере кода подключается к событию NewInspector объекта [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)), область применения которого ограничена функцией Connect. В результате, когда вызывается метод обратного вызова, программа уже вышла из функции Connect, объект Inspectors уже уничтожен сборщиком мусора, и поэтому MyNewInspector никогда не вызывается.

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

В этом случае правильно будет сохранить объект Inspectors в более длительной переменной, чей срок жизни охватывает весь MyClass, включая метод обратного вызова MyNewInspector. В следующем примере область применения MyInspectors охватывает весь MyClass и обеспечивается подключение обратного вызова в течение времени жизни класса.

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

Благодаря синтаксическим различиям подключений обработчиков событий в различных языках эта проблема менее распространена в таких языках, как Visual Basic, где можно подключить событие, задавая экземпляр родительского объекта, и одновременно определить метод обратного вызова. В следующем примере на Visual Basic ключевое слово Handles используется для подключения метода обратного вызова Region\_Expanded к событию [Expanded](https://msdn.microsoft.com/library/bb609515\(v=office.15\)). Область применения экземпляра родительского объекта, Region, охватывает MyClass, включая метод обратного вызова Region\_Expanded.

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

В этом примере метод обратного вызова вызывается правильным образом, так как метод обратного вызова Region\_Expanded подключается к событию Expanded в течение времени жизни класса.

## <a name="see-also"></a>См. также

- [Подключение к настраиваемым обработчикам событий](connecting-to-custom-event-handlers.md)

