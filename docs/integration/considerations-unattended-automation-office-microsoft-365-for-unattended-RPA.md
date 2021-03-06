---
title: Соображения для незавещенной автоматизации Office в Microsoft 365 для неавтоматной среды RPA
ms.date: 03/30/2020
ms.audience: Developer
localization_priority: Normal
description: Соображения для незамещенной автоматизации Office в Microsoft 365 для неавтоматной среды RPA.
ms.openlocfilehash: 576217fc85f2980a6d2451e3f930296ea4c11a56
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "43103052"
---
# <a name="considerations-for-unattended-automation-of-office-in-the-microsoft-365-for-unattended-rpa-environment"></a>Соображения для незавещенной автоматизации Office в Microsoft 365 для неавтоматной среды RPA

Хотя Microsoft 365 для без присмотра RPA предоставляет лицензию, которая позволяет автоматизировать Office без пользователя, все текущие версии Office были разработаны и протестированы для запуска в качестве конечных продуктов на клиентской рабочей станции с пользователем, присутствующим для взаимодействия с интерфейсом приложения. Непредвиденное поведение, выявимое в результате использования приложений без участия пользователя, не является дефектом. Если вы хотите выполнить Office в этой конфигурации, необходимо быть готовым к учету этих неожиданных действий в логике приложения.

В этой статье описаны некоторые из соображений без присмотра автоматизации Office, которые помогут вам при использовании этого подхода. Однако обратите внимание, что использование Office в этой конфигурации строго "AS IS" и должно учитывать эти непредвиденные действия. Представленная здесь информация не является исчерпывающей и не гарантирует решение всех проблем для всех клиентов. Мы рекомендуем вам тщательно протестировать решение перед развертыванием.

## <a name="common-problems-in-unattended-automation"></a>Распространенные проблемы в автоматизации без присмотра

Если вы хотите использовать Office без пользователя, следует помнить о следующих областях, в которых Office вести себя иначе, чем ожидалось. Для успешного запуска решения необходимо решить эти проблемы и максимально минимизировать их последствия. При создании приложения внимательно рассмотрите эти проблемы.

### <a name="interactive-ui-elements"></a>Интерактивные элементы пользовательского интерфейса

Office приложения предполагают, что они запускаются в интерактивном режиме. Если возникает неожиданная ошибка, или если для выполнения функции необходим неустановленный параметр, Office для запроса пользователя с диалоговое окно, которое задает пользователю вопрос о том, как он хочет действовать. В незаконченной автоматизации это может привести к "висеть" приложению по мере остановки приложения до получения этого ввода. Если вы автоматизируете Office с помощью общедоступных API, можно подавить многие из этих оповещений, настроив соответствующие свойства, такие как [Application.DisplayAlerts](https://docs.microsoft.com/office/vba/api/word.application.displayalerts) и [Application.AutomationSecurity.](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) Код должен быть разработан для определения и обработки блокирующих оповещений в любое время.

### <a name="user-identity"></a>Идентификатор пользователя

Office приложениям требуется удостоверение пользователя при запуске приложений, даже если приложение запущено с помощью автоматизации. Это удостоверение пользователя может привести к любому из следующих ниже.

- Наличие дополнительного пользовательского интерфейса для входов, который необходимо обрабатывать.
- Файлы, которые не могут быть открыты и/или изменены на основе разрешений доступа к пользователю.
- Неожиданные изменения в метаданных файла (например, некоторые свойства файлов будут обновляться на основе удостоверения личности пользователя экземпляра автоматизированного приложения).

Различные подходы могут помочь устранить эти проблемы; например, запуск [инспектора документов для](https://docs.microsoft.com/office/vba/library-reference/concepts/using-the-document-inspector) удаления метаданных. Подумайте, подходят ли эти подходы в зависимости от сценария.

### <a name="server-side-security"></a>Безопасность на стороне сервера

При Office без присмотра и обработки произвольного контента файлов не доступны дополнительные средства защиты, определенные в этой среде, чтобы предотвратить загрузку и запуск макрос, хранимые в этих файлах. Office не защищает вас от непреднамеренно запуска макрос из кода или от запуска другого сервера, на который могут запускаться макрос. Для смягчения этого риска можно использовать такие свойства, как [Application.AutomationSecurity,](https://docs.microsoft.com/office/vba/api/word.application.automationsecurity) но следует обеспечить загрузку только доверенного контента.

Кроме того, Office использует множество компонентов (таких как Simple MAPI, WinInet и MSDAIPP), которые могут кэширование данных проверки подлинности клиента для ускорения обработки. Если Office автоматизирована серверная часть и обрабатывает несколько файлов, если сведения о проверке подлинности кэшировали для этого сеанса, один клиент может использовать кэширование учетных данных другого клиента. Таким образом, клиент может получить разрешения на доступ без предоставления, выдав себя за других пользователей.

### <a name="ui-changes"></a>Изменения пользовательского интерфейса

Элементы пользовательского интерфейса в Office в основном стабильны, но определенное расположение любого элемента пользовательского интерфейса не гарантируется и может изменяться по мере развития разработки продукта для включения отзывов пользователей и удовлетворения потребностей клиентов. Логика любой автоматизации должна учитывать это. Эти изменения могут привести к изменениям именования на вкладке кнопки или группы, движению команд между вкладками, добавлению новых вкладок или удалению команд в соответствии с нашими политиками амортизации функций. Эти изменения могут происходить в пользовательском интерфейсе, а также в сведениях о доступности, предоставляемых приложением, так как эта информация изменяется для повышения доступности и учета текущих отзывов клиентов и может быть отката для разных пользователей в разное время.

Даже без изменений продукта различия между системными средами (например, размер экрана/разрешение/DPI) могут привести к изменениям расположения элементов на экране. Любой подход, который опирается на координаты экрана для имитации ввода пользователя, должен учитывать эти изменения и соответствующим образом адаптироваться.

### <a name="single-threading"></a>Однопотоковая

Office приложения являются невозвратными, основанными на sta приложениях, которые предназначены для предоставления разнообразных, но ресурсоемких функций для одного клиента. В приложениях используются глобальные ресурсы, такие как файлы с картой памяти, глобальные надстройки или шаблоны, а также серверы общей автоматизации. Это может ограничить количество экземпляров, которые могут работать одновременно и могут привести к условиям гонки, если приложения настроены в многоуровневой среде. Если планируется запустить несколько экземпляров любого Office приложения, следует изолировать их на уровне виртуальной машины, чтобы обеспечить стабильность результатов решения.

### <a name="resiliency-and-stability"></a>Устойчивость и стабильность

Даже с учетом вышеперечисленных соображений, если приложения автоматизированы таким образом, чтобы имитировать вход пользователя или продолжительность сеанса, значительно превышающая интерактивный уровень, они могут столкнуться с проблемой, которая не присутствует при интерактивном запуске. Решения, Office в этом контексте, должны активно создавать механизмы мониторинга состояния приложения и перезапуска (и/или виртуальной машины, на которой они работают) если и по мере необходимости.

## <a name="suggested-alternatives"></a>Предлагаемые альтернативы

Корпорация Майкрософт настоятельно рекомендует несколько альтернатив, которые не требуют Office для установки и запуска серверной стороны и которые могут выполнять общие задачи более эффективно и быстрее, чем автоматизация в этой конфигурации. Прежде чем Office в проекте в качестве компонента на стороне сервера, рассмотрите альтернативные варианты.

### <a name="microsoft-graph"></a>Microsoft Graph

API microsoft Graph предоставляет доступ к службам, данным и аналитике, доступным пользователям и решениям в облаке Майкрософт, включая многие службы, поддерживающие потребности без присмотра автоматизации: доступ к почте и календарю пользователей / контактам / файлам, преобразованию документов, Excel расчету книг и т. д. Эти службы предназначены для неохваченного использования и широкомасштабного доступа, а также используют стандартный синтаксис API RESTful. Дополнительные сведения о microsoft Graph и о том, как использовать его для работы с данными пользователей, посетите следующие сведения:

- [Обзор Microsoft Graph](https://docs.microsoft.com/graph/overview) 
- [Начало работы с Microsoft Graph](https://developer.microsoft.com/graph/get-started)
- [Скачайте файл в другом формате](https://docs.microsoft.com/graph/api/driveitem-get-content-format?view=graph-rest-1.0&tabs=http) (преобразование файлов)
- [Работа с Excel в Microsoft Graph](https://docs.microsoft.com/graph/api/resources/excel?view=graph-rest-1.0) (сведения о книге)

### <a name="open-xml-file-formats"></a>Откройте форматы XML-файлов

Многие задачи автоматизации включают создание или редактирование документов. Office поддерживает форматы файлов Open XML, которые позволяют разработчикам создавать, редактировать, читать и изменять содержимое файлов с помощью стандартных технологий XML и ZIP, определенных в международном стандарте ISO 29500. Этими форматами файлов можно управлять с помощью любых средств ZIP/XML, в том числе System.IO.Package.IO пространства имен в Microsoft .NET 3.x Framework. Прямое редактирование форматов файлов — это рекомендуемый и поддерживаемый метод обработки изменений Office файлов из службы.

Корпорация Майкрософт предоставляет SDK для обработки форматов файлов Open XML из .NET 3.x Framework. Дополнительные сведения о SDK и о том, как использовать SDK для создания или редактирования файлов Open XML, посетите следующие сведения:

- [Общие сведения о форматах файлов Open XML](https://docs.microsoft.com/office/open-xml/understanding-the-open-xml-file-formats)
- [Добро пожаловать на страницу пакета SDK 2.5 Open XML для Office](https://docs.microsoft.com/office/open-xml/open-xml-sdk)
