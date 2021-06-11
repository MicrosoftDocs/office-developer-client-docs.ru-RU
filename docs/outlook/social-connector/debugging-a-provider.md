---
title: Отладка поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Существует несколько способов отключении поставщика Outlook social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281071"
---
# <a name="debugging-a-provider"></a>Отладка поставщика

Существует несколько способов отключении поставщика Outlook social Connector (OSC): 
  
- Использование команд отлаговки в компоненте ленты пользовательского интерфейса Office Fluent в Outlook или поддерживающей Office клиентского приложения вызывает у OSC различные действия.
    
- С помощью Fiddler отслеживаются вызовы API и XML, отправленные между социальной сетью и ее поставщиком OSC
    
## <a name="debug-buttons"></a>Кнопки отлаговка

Размягчаемость поставщика OSC предоставляет возможность отладки поставщика OSC. Чтобы отчудить поставщика, создайте значение типа DWORD в реестре Windows под ключом (как показано в следующей строке) и задайте значение `DebugProviders` `SocialConnector` `DebugProviders` 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
По умолчанию отладка поставщика отключена. Если значение не присутствует или имеет значение 0, отладка поставщика  `DebugProviders` отключена. 
  
Если отладка поставщика включена, OSC отображает диалоговое окно оповещений с подробными сведениями об ошибках при ошибке и проверяет XML-адрес поставщика OSC на схему XML поставщика OSC. На основе пространства имен, указанного для строки XML, поставщик OSC, разработанный с помощью OSC 1.0, проверяется в файле схемы OSC 1.0 OutlookSocialProvider.xsd. Поставщик OSC, разработанный с помощью OSC 1.1 или более поздней системы, проверяется в файле схемы OutlookSocialProvider_1.1.xsd. При использовании значения отображается оповещение об отлажении для всех загруженных поставщиков, а  `DebugProviders` не для конкретного поставщика. 
  
Чтобы отобразить кнопки отлаговки, которые помогут вам отвести поставщика, создайте значение типа DWORD в реестре Windows под ключом и установите значение `ShowDebugButtons` `SocialConnector` `ShowDebugButtons` 1. Чтобы скрыть кнопки панели командной отлаговки, установите  `ShowDebugButtons` значение 0. 
  
В Outlook 2010 г. и в клиентских приложениях Office 2013 г.  кнопки отламывателя отображаются на вкладке Надстройки ленты проводника. В Outlook 2007 и Outlook 2003 года кнопки отлаговки отображаются в стандартной панели команд окна Outlook explorer. 
  
В следующей таблице описаны кнопки отлаговки.
  
|**Кнопка отламывка**|**Function**|
|:-----|:-----|
|Синхронизация контактов  <br/> |Вызывает osc, чтобы попросить поставщика OSC для кэшировать контакты только.  <br/> |
|Синхронизация GAL  <br/> |Заставляет OSC заполнять данные из глобального списка адресов Exchange для Outlook контактов.  <br/> |
|Недействительный кэш категории  <br/> |Вызывает загрузку списка категорий для каждого магазина при обновлении ленты действий.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler — это средство отладки по проводам для проверки вызовов API, отправленных от поставщика в социальную сеть, и XML, отправленных социальной сетью поставщику. Fiddler доступен для скачивания в [прокси-сервере веб-отладки Fiddler.](https://www.fiddler2.com/fiddler2/version.asp)
  
## <a name="see-also"></a>См. также

- [Быстрые шаги для обучения разработке поставщика](quick-steps-for-learning-to-develop-a-provider.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md) 
- [Лучшие практики для разработки поставщика](best-practices-for-developing-a-provider.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)  
- [Разработка поставщика с помощью схемы XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Получение готовности к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md)

