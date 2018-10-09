---
title: События в Outlook PIA
TOCTitle: Events in the Outlook PIA
ms:assetid: 1f9eafb3-6645-4e27-81fa-5d73bf94ae40
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb644571(v=office.15)
ms:contentKeyID: 55119782
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 0433d1915008bf9317790c1ba86a9bb028161c48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407543"
---
# <a name="events-in-the-outlook-pia"></a>События в Outlook PIA

При просмотре основной сборки взаимодействия Outlook (PIA) можно заметить, что многие интерфейсы и делегаты событий названы в соответствии со знакомыми именами объектов и событий в объектной модели Outlook. В отличие от событий в библиотеке типов COM события в Outlook PIA не определены в том же самом интерфейсе как методы и свойства этого же объекта. Связанные с событием интерфейсы, делегаты и классы модуля поддержки приемника либо импортируются, либо создаются для поддержки событий в Outlook PIA. В этом разделе описываются эти связанные с событиями интерфейсы, делегаты и классы модуля поддержки приемника.

## <a name="where-do-the-event-interfaces-delegates-and-sink-helper-classes-come-from"></a>Откуда появляются интерфейсы событий, делегаты и классы модуля поддержки приемника

Для создания Outlook PIA в Outlook используется программа импорта библиотек типов (TLBIMP) в среде .NET Framework, позволяющая преобразовывать определения типов в библиотеке типов COM в эквивалентные определения в сборке среды CLR. Для каждого объекта TLBIMP импортирует следующие два типа интерфейсов.

  - Основной интерфейс (например, интерфейс [\_Application](https://msdn.microsoft.com/library/bb611255\(v=office.15\)))

  - Интерфейс события (например, интерфейс [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\)))

TLBIMP обрабатывает импортированные интерфейсы и создает ряд интерфейсов, делегатов и классов, включая интерфейс .NET (например, интерфейс [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) ). Если у объекта есть события, создаются следующие сущности:

  - Интерфейс события .NET (например, интерфейс [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\)))

  - Делегат для каждого события (например, делегат [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\)))

  - Класс модуля поддержки приемника (например, класс [ApplicationEvents\_11\_SinkHelper](https://msdn.microsoft.com/library/bb609842\(v=office.15\)))

### <a name="multiple-versions-of-events"></a>Несколько версий событий

У ряда объектов, существующих для нескольких версий Outlook, есть различные реализации событий для этих версий и дополнительные события, добавленные по мере выхода новых версий. Для поддержки событий, зависящих от различных версий, Outlook отличает эти связанные с событиями интерфейсы, делегаты и классы, добавляя к их именам номер версии. Например:

  - В число импортированных интерфейсов событий для объекта **Application** входят:
    
      - Самая ранняя версия для Outlook 98 и Outlook 2000: интерфейс [ApplicationEvents](https://msdn.microsoft.com/library/bb644093\(v=office.15\))
    
      - Версия для Outlook 2002: интерфейс [ApplicationEvents\_10](https://msdn.microsoft.com/library/bb647702\(v=office.15\)) 
    
      - Версия для Outlook 2003 и более поздних версий: интерфейс [ApplicationEvents\_11](https://msdn.microsoft.com/library/bb609229\(v=office.15\))

  - В интерфейсы события .NET, созданные TLBIMP для объекта **Application**, входят:
    
      - Самая ранняя версия для Outlook 98 и Outlook 2000: интерфейс [ApplicationEvents\_Event](https://msdn.microsoft.com/library/bb609380\(v=office.15\))
    
      - Версия для Outlook 2002: интерфейс [ApplicationEvents\_10\_Event](https://msdn.microsoft.com/library/bb610098\(v=office.15\))
    
      - Версия для Outlook 2003 и более поздних версий: интерфейс [ApplicationEvents\_11\_Event](https://msdn.microsoft.com/library/bb622725\(v=office.15\))

  - Делегаты, создаваемые программой TLBIMP для каждого события в каждой версии объекта **Application**, например делегат для каждой версии события ItemSend:
    
      - Самая ранняя версия для Outlook 98 и Outlook 2000: делегат [ApplicationEvents\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb622515\(v=office.15\))
    
      - Версия для Outlook 2002: делегат [ApplicationEvents\_10\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb646436\(v=office.15\))
    
      - Версия для Outlook 2003 и более поздних версий: делегат [ApplicationEvents\_11\_ItemSendEventHandler](https://msdn.microsoft.com/library/bb610818\(v=office.15\))

Логически рассуждая, события, добавленные в более позднюю версию, не появляются в интерфейсах событий более ранних версий, и соответствующие делегаты в более ранних версиях для них отсутствуют. Например, событие [AttachmentSelectionChange](https://msdn.microsoft.com/library/ff184926\(v=office.15\)) было добавлено в объект [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) в Outlook 2010, следовательно, оно не является частью следующих более ранних интерфейсов события для объекта Explorer:

  - Интерфейс ExplorerEvents

  - Интерфейс ExplorerEvents\_Event

С другой стороны, можно найти это событие в самом недавнем интерфейсе события .NET, ExplorerEvents\_10\_Event, и его делегат для версии Outlook 2010, [ExplorerEvents\_10\_AttachmentSelectionChangeEventHandler](https://msdn.microsoft.com/library/ff185177\(v=office.15\)).

## <a name="what-the-event-interfaces-delegates-and-sink-helper-classes-are-for"></a>Для чего нужны интерфейсы событий, делегаты и классы модуля поддержки приемника

С помощью объекта **Application** в качестве примера в этом разделе описывается содержание перечисленных выше интерфейсов и классов.

  - Основной интерфейс, \_Application, определяет все методы и свойства Application. Кроме условия, рассматриваемого ниже, этот интерфейс обычно не используется в коде.

  - Интерфейсы событий, импортированные программой TLBIMP, такие как ApplicationEvents\_11 и ApplicationEvents\_10, определяют сопоставление методов событиям Application в соответствующей версии Outlook. Этот интерфейс не используется в коде.

  - Интерфейсы событий, созданные программой TLBIMP, такие как ApplicationEvents\_11\_Event и ApplicationEvents\_10\_Event, определяют все события Application в соответствующей версии Outlook. Обработчик события, разрабатываемый для конкретной версии, реализуется как метод, который связывается с событием, определенным в соответствующей версии интерфейса событий .NET. Кроме условия, рассматриваемого ниже, обычно не применяется ссылка на интерфейс событий в коде.

  - Интерфейс .NET, Application, наследует интерфейсы \_Application и ApplicationEvents\_11\_Event. Обычно это и есть интерфейс, используемый в управляемом коде для доступа к объектам, методам, свойствам и новейшим членам события объекта **Application**. Но есть два исключения, в которых для связи с событием используется не интерфейс .NET, а другой интерфейс:
    
      - При доступе к событию, носящему то же имя, что и метод этого объекта, для связи с событием обращайтесь к соответствующему интерфейсу события. Например, для связи с событием [Quit](https://msdn.microsoft.com/library/bb622595\(v=office.15\)) обращайтесь к интерфейсу ApplicationEvents\_11\_Event.
    
      - При подключении к более ранней версии события, которое затем было расширено в более поздней версии Outlook, подключайтесь к более ранней версии. Например, если требуется подключиться к версии события Quit для объекта **Application**, реализованного для Outlook 2002 вместо последней версии программы, подключитесь к событию [Quit](https://msdn.microsoft.com/library/bb609660\(v=office.15\)), определенному в интерфейсе ApplicationEvents\_10\_Event вместо того, чтобы подключаться к событию Quit, определенному в интерфейсе ApplicationEvents\_11\_Event.

  - Делегаты предоставляют платформу для создания настраиваемых обработчиков событий для определенных события в определенной версии Outlook. Например, если нужно добавить проверку наличия строки темы в элементе Outlook непосредственно перед отправкой, реализуйте метод проверки в обратном вызове с такой же подписью, как у делегата ApplicationEvents\_11\_ItemSendEventHandler. Затем подключите метод обратного вызова в качестве обработчика события для события ItemSend, которое определено в интерфейсе ApplicationEvents\_11\_Event. Дополнительные сведения о подключении метода обратного вызова в качестве обработчика события для объекта см. в статье [Подключение к настраиваемым обработчикам событий](connecting-to-custom-event-handlers.md).

  - Классы модуля поддержки приемника, созданные программой TLBIMP, например ApplicationEvents\_11\_SinkHelper и [ApplicationEvents\_10\_SinkHelper](https://msdn.microsoft.com/library/bb644070\(v=office.15\)), являются объектами обработчика события для событий Application в соответствующей версии Outlook. Не используйте эти классы в коде.

## <a name="see-also"></a>См. также

- [Связывание Outlook PIA с объектной моделью](relating-the-outlook-pia-with-the-object-model.md)
- [Объекты в Outlook PIA](objects-in-the-outlook-pia.md)
- [Методы и свойства в Outlook PIA](methods-and-properties-in-the-outlook-pia.md)
- [Разработка управляемых надстроек для Outlook с помощью Outlook PIA](developing-managed-outlook-add-ins-using-the-outlook-pia.md)

