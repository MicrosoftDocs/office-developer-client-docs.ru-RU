---
title: Методы и свойства в Outlook PIA
TOCTitle: Methods and properties in the Outlook PIA
ms:assetid: ec7742de-ead6-41dd-90a3-1280fdf09d54
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612528(v=office.15)
ms:contentKeyID: 55119780
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b1bee381e6f53b4d8a63e69a920e4f4a6e9e302a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407375"
---
# <a name="methods-and-properties-in-the-outlook-pia"></a>Методы и свойства в Outlook PIA

В этой статье описано, как получить доступ к методам и свойствам объекта в управляемом коде с помощью основной сборки взаимодействия Outlook (PIA).

## <a name="where-helper-objects-come-from"></a>Откуда поступают объекты модуля поддержки

При создании PIA в Outlook применяется программа импорта библиотек типов (TLBIMP) в .NET Framework, преобразующая определения типов в библиотеке типа COM в эквивалентные определения из сборки среды CLR. В рамках COM объект фактически является компонентным классом, который состоит из следующих компонентов:

- основной интерфейс (например, интерфейс [\_FormRegion](https://msdn.microsoft.com/library/bb645761\(v=office.15\)));

- интерфейс события (например, интерфейс [FormRegionEvents](https://msdn.microsoft.com/library/bb611940\(v=office.15\))).

TLBIMP импортирует основной интерфейс и интерфейс события для каждого объекта и создает ряд интерфейсов, делегатов и классов, среди которых встречаются следующие:

- интерфейс события .NET (например, интерфейс [FormRegionEvents\_Event](https://msdn.microsoft.com/library/bb647619\(v=office.15\)));

- класс .NET (например, класс [FormRegionClass](https://msdn.microsoft.com/library/bb624204\(v=office.15\)));

- интерфейс .NET (например, интерфейс [FormRegion](https://msdn.microsoft.com/library/bb652633\(v=office.15\))).

## <a name="what-the-helper-objects-are-for"></a>Для чего предназначены объекты модуля поддержки

В следующем списке проверяется содержимое каждого перечисленного ранее интерфейса и класса (объект **FormRegion** продолжает использоваться в качестве примера).

- Интерфейс \_FormRegion определяет все методы и свойства FormRegion. Этот интерфейс обычно не используется в коде, кроме условия, рассматриваемого ниже.

- Интерфейс **FormRegionEvents** определяет методы, которые соответствуют событиям FormRegion. Этот интерфейс не используется в коде.

- Далее TLBIMP обрабатывает интерфейс **FormRegionEvents**, чтобы создать интерфейс **FormRegionEvents**\_Event, определяющий все события FormRegion. Этот интерфейс обычно не используется в коде, кроме условия, рассматриваемого ниже.

- Класс FormRegionClass определяет все методы, свойства и элементы событий FormRegion. Это тот класс, с которым интерфейсу FormRegion приписывается скрытая связь, позволяющая написать код для создания экземпляра интерфейса FormRegion. Однако непосредственно в коде этот интерфейс не используется.

- Интерфейс FormRegion наследует интерфейс \_FormRegion и интерфейс **FormRegionEvents**\_Event. На рисунке 1 показана эта связь наследования.
    
  **Рисунок 1. Интерфейс FormRegion наследует методы и свойства интерфейса \_FormRegion, наследуя события из интерфейса FormRegionEvents\_Event**

  ![Интерфейс FormRegion наследует методы и свойства интерфейса _FormRegion, наследуя события из интерфейса FormRegionEvents_Event](media/pia-form-region-interface.gif)
    
  Обычно FormRegion — этот интерфейс, используемый в управляемом коде для доступа к объекту, методу, свойству и элементам события объекта **FormRegion**.

Взяв объект **Application** в качестве еще одного примера, вы имеете доступ к объекту **Application**, методам, свойствам и событиям посредством интерфейса [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)). Однако существует три исключения, требующих применения другого интерфейса. Кроме того, выбор другого интерфейса может зависеть от языка.

- При доступе к методу, который назван так же, как и событие, рекомендуется привести к основному интерфейсу для вызова метода. Например, у объекта **Application** есть метод [Quit](https://msdn.microsoft.com/library/bb646614\(v=office.15\)) и событие [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)). В Visual Basic .NET можно получить доступ к методу Quit с помощью интерфейса Application. В C\# избежать предупреждения компилятора можно, приведя метод Quit к основному интерфейсу, как показано в следующем образце кода:
    
   ```csharp
      void DemoApp()
      {
          Outlook.Application myApp = new Outlook.Application();
          // Other application code here
          ((Outlook._Application)myApp).Quit();
      }
   ```

- При доступе к событию, названному так же, как и метод объекта, необходимо привести к соответствующему интерфейсу события, чтобы подключиться к событию. Как и в указанном выше примере, для подключения к событию Quit необходимо привести к интерфейсу [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)).

- При подключении к более ранней версии события, которое было впоследствии продлено в позднейшей версии Outlook, необходимо подключиться к версии события в ранней версии интерфейса. Например, если требуется подключиться к версии события Quit для объекта **Application**, реализованного для Outlook 2002 вместо последней версии программы, подключитесь к событию [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)), определенному в интерфейсе [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\)) вместо того, чтобы подключаться к событию Quit, определенному в интерфейсе ApplicationEvents\_11\_Event.

## <a name="see-also"></a>См. также

- [Связывание Outlook PIA с объектной моделью](relating-the-outlook-pia-with-the-object-model.md)
- [Объекты в Outlook PIA](objects-in-the-outlook-pia.md)
- [События в Outlook PIA](events-in-the-outlook-pia.md)

