---
title: Подключение к настраиваемым обработчикам событий
TOCTitle: Connecting to custom event handlers
ms:assetid: 6e894c16-0fe9-4b86-b798-547b86f44cd8
ms:mtpsurl: https://msdn.microsoft.com/library/Bb610520(v=office.15)
ms:contentKeyID: 55119783
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 31e9a5453bbfbd4a51132fa6af71b86889b4b32e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406108"
---
# <a name="connecting-to-custom-event-handlers"></a>Подключение к настраиваемым обработчикам событий

Outlook создает события, чтобы уведомить надстройки о том, что что-то произошло, например что в папку "Входящие" получен новый почтовый элемент. Надстройки могут указывать Outlook, что в случае конкретного события следует выполнить определенные действия. Этот механизм оповещения и обратного вызова поддерживается делегатами .NET Framework. Основная сборка взаимодействия Outlook (PIA) определяет делегаты, к которым можно подключить методы обратного вызова для обработки соответствующих событий. В этом разделе описывается процесс определения метода обратного вызова и его подключение к объекту Outlook в качестве обработчика события.

## <a name="creating-a-callback-method"></a>Создание метода обратного вызова

Обратный вызов  это метод, реализуемый для обработки конкретного события и выполняемый источником уведомления. В Outlook надстройки могут реализовать методы обратного вызова, чтобы реагировать на определенные события, создаваемые Outlook. Этот метод обратного вызова должен соответствовать сигнатуре делегата этого события. Например, чтобы реализовать обработчик для события [ItemSend](https://msdn.microsoft.com/library/bb647198\(v=office.15\)), необходимо объявить метод обратного вызова, соответствующий сигнатуре нужного делегата:

```csharp
public delegate void ApplicationEvents_11_ItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Delegate Sub ApplicationEvents_11_ItemSendEventHandler(_
    ByVal Item As Object, ByRef Cancel As Boolean)
```

При определении метода обратного вызова проигнорируйте ключевое слово **Delegate**, которое в противном случае определит другого делегата. Ниже показан пример метода обратного вызова **MyItemSendEventHandler**.

```csharp
public void MyItemSendEventHandler(object Item, ref bool Cancel)
```


```vb
Public Sub MyItemSendEventHandler (_
    ByVal Item As Object, ByRef Cancel As Boolean)
…
End Sub
```

## <a name="connecting-a-callback-method"></a>Подключение метода обратного вызова

Реализованный метод обратного вызова для события можно подключить к объекту Outlook, чтобы Outlook вызывал этот метод в качестве обработчика этого события. Обратите внимание, что событие может обрабатываться несколькими обработчиками события, и именно тут играют свою роль делегаты, назначающие обработку событий обработчикам.

В продолжение последнего примера, в котором показано, как задать обработчик событий **ItemSend** объекта **Application** для подключения обработчика событий **MyItemSendEventHandler** к объекту **Application** на языке C\#, создайте экземпляр объекта delegate, передайте обработчик событий **MyItemSendEventHandler** в конструктор объекта delegate, а затем добавьте этот объект delegate в событие **ItemSend** с помощью оператора +=.

```csharp
app.ItemSend += new ApplicationEvents_11_ItemSendEventHandler(MyItemSendEventHandler)
```

В Visual Basic с помощью оператора **AddHandler** сопоставьте событие **ItemSend** с обработчиком событий **MyItemSendEventHandler**:

```vb
AddHandler app.ItemSend, AddressOf MyItemSendEventHandler
```

## <a name="see-also"></a>См. также

- [События в основной сборке взаимодействия Outlook](events-in-the-outlook-pia.md)
- [Объекты в Outlook PIA](objects-in-the-outlook-pia.md)

