---
title: Подключение к настраиваемым обработчикам событий
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58722b8b140f89f0fe29a3e52db578a423a0160a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351424"
---
# <a name="connecting-to-custom-event-handlers"></a><span data-ttu-id="be5aa-102">Подключение к настраиваемым обработчикам событий</span><span class="sxs-lookup"><span data-stu-id="be5aa-102">Connecting to custom event handlers</span></span>

<span data-ttu-id="be5aa-p101">Outlook создает события, чтобы уведомить надстройки о том, что что-то произошло, например что в папку "Входящие" получен новый почтовый элемент. Надстройки могут указывать Outlook, что в случае конкретного события следует выполнить определенные действия. Этот механизм оповещения и обратного вызова поддерживается делегатами .NET Framework. Основная сборка взаимодействия Outlook (PIA) определяет делегаты, к которым можно подключить методы обратного вызова для обработки соответствующих событий. В этом разделе описывается процесс определения метода обратного вызова и его подключение к объекту Outlook в качестве обработчика события.</span><span class="sxs-lookup"><span data-stu-id="be5aa-p101">Outlook raises events to notify add-ins about something happening, such as the Inbox receiving a new mail item. Add-ins can specify to Outlook that upon the occurrence of a specific event, certain actions should take place. This alert and callback mechanism is supported by delegates of the .NET Framework. The Outlook Primary Interop Assembly (PIA) defines delegates to which you can connect callback methods to handle corresponding events. This topic describes this process of defining a callback method and connecting it as an event handler to the Outlook object.</span></span>

## <a name="creating-a-callback-method"></a><span data-ttu-id="be5aa-108">Создание метода обратного вызова</span><span class="sxs-lookup"><span data-stu-id="be5aa-108">Creating a Callback method</span></span>

<span data-ttu-id="be5aa-p102">Обратный вызов  это метод, реализуемый для обработки конкретного события и выполняемый источником уведомления. В Outlook надстройки могут реализовать методы обратного вызова, чтобы реагировать на определенные события, создаваемые Outlook. Этот метод обратного вызова должен соответствовать сигнатуре делегата этого события. Например, чтобы реализовать обработчик для события [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), необходимо объявить метод обратного вызова, соответствующий сигнатуре нужного делегата:</span><span class="sxs-lookup"><span data-stu-id="be5aa-p102">A callback is a method that is implemented to handle the occurrence of a specific event and is executed by a notification source. In Outlook, add-ins can implement callback methods to respond to certain events raised by Outlook. This callback method must match the signature of the delegate of that event. For example, to implement an event handler for the [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)) event, you must declare the callback method that matches the signature of the corresponding delegate:</span></span>

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

<span data-ttu-id="be5aa-p103">При определении метода обратного вызова проигнорируйте ключевое слово **Delegate**, которое в противном случае определит другого делегата. Ниже показан пример метода обратного вызова **MyItemSendEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="be5aa-p103">When defining the callback method, ignore the **Delegate** keyword which otherwise would define another delegate. A sample callback method, **MyItemSendEventHandler**, is shown below:</span></span>

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a><span data-ttu-id="be5aa-115">Подключение метода обратного вызова</span><span class="sxs-lookup"><span data-stu-id="be5aa-115">Connecting a Callback method</span></span>

<span data-ttu-id="be5aa-p104">Реализованный метод обратного вызова для события можно подключить к объекту Outlook, чтобы Outlook вызывал этот метод в качестве обработчика этого события. Обратите внимание, что событие может обрабатываться несколькими обработчиками события, и именно тут играют свою роль делегаты, назначающие обработку событий обработчикам.</span><span class="sxs-lookup"><span data-stu-id="be5aa-p104">After implementing a callback method for an event, you can connect it to the Outlook object so that Outlook knows to call the method as an event handler of that event. Note that an event can be handled by more than one event handler, and this is where delegates that assign event handling to event handlers come into play.</span></span>

<span data-ttu-id="be5aa-118">В продолжение последнего примера, в котором показано, как задать обработчик событий **ItemSend** объекта **Application** для подключения обработчика событий **MyItemSendEventHandler** к объекту **Application** на языке C\#, создайте экземпляр объекта delegate, передайте обработчик событий **MyItemSendEventHandler** в конструктор объекта delegate, а затем добавьте этот объект delegate в событие **ItemSend** с помощью оператора +=.</span><span class="sxs-lookup"><span data-stu-id="be5aa-118">Continuing with the last example of specifying a event handler for the **ItemSend** event of the **Application** object, to connect **MyItemSendEventHandler** to the **Application** object in C\#, create an instance of the delegate object, pass **MyItemSendEventHandler** to the constructor of the delegate object, and then add this delegate object to the **ItemSend** event using the += operator:</span></span>

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

<span data-ttu-id="be5aa-119">В Visual Basic с помощью оператора **AddHandler** сопоставьте событие **ItemSend** с обработчиком событий **MyItemSendEventHandler**:</span><span class="sxs-lookup"><span data-stu-id="be5aa-119">In Visual Basic, you use the **AddHandler** statement to associate the **ItemSend** event with the **MyItemSendEventHandler** event handler:</span></span>

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a><span data-ttu-id="be5aa-120">См. также</span><span class="sxs-lookup"><span data-stu-id="be5aa-120">See also</span></span>

- [<span data-ttu-id="be5aa-121">События в основной сборке взаимодействия Outlook</span><span class="sxs-lookup"><span data-stu-id="be5aa-121">Events in the Outlook PIA</span></span>](events-in-the-outlook-pia.md)
- [<span data-ttu-id="be5aa-122">Объекты в Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="be5aa-122">Objects in the Outlook PIA</span></span>](objects-in-the-outlook-pia.md)

