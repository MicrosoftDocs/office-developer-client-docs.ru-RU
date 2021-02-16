---
title: Отладка поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Существует несколько способов отлаки поставщика Outlook Social Connector (OSC):'
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281071"
---
# <a name="debugging-a-provider"></a>Отладка поставщика

Существует несколько способов отлаки поставщика Outlook Social Connector (OSC): 
  
- Использование команд отлаки в компоненте ленты пользовательского интерфейса Office Fluent в Outlook или поддерживающих клиентские приложения Office приведет к тому, что osC будет принимать различные действия.
    
- Использование Fiddler для отслеживания вызовов API и XML, отправленных между социальной сетью и ее поставщиком OSC
    
## <a name="debug-buttons"></a>Кнопки отлаки

Возможность расшифровки поставщика OSC предоставляет возможность отладки поставщика OSC. Чтобы отладить поставщика, создайте значение типа DWORD в реестре Windows под ключом (как показано в следующей строке) и задайте значение  `DebugProviders`  `SocialConnector`  `DebugProviders` 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
По умолчанию отладка поставщика отключена. Если значение не присутствует или имеет значение 0, отладка поставщика  `DebugProviders` отключена. 
  
Если отладка поставщика включена, OSC отображает диалоговое окно оповещения с подробными сведениями об ошибке при ошибке и проверяет любой XML-адрес поставщика OSC на XML-схеме поставщика OSC. На основе пространства имен, указанного для строки XML, поставщик OSC, разработанный с помощью OSC 1.0, проверяется на основе файла схемы OSC 1.0 OutlookSocialProvider.xsd. Поставщик OSC, разработанный с помощью OSC 1.1 или более поздней, проверяется с использованием файла схемы, OutlookSocialProvider_1.1.xsd. При использовании значения оповещение отлажено для всех загруженных поставщиков, а не  `DebugProviders` для определенного поставщика. 
  
Чтобы отобразить кнопки отлаки, которые помогут отлажать поставщика, создайте значение типа DWORD в реестре Windows под ключом и задайте значение  `ShowDebugButtons`  `SocialConnector`  `ShowDebugButtons` 1. Чтобы скрыть кнопки панели команд отлаки, установите значение  `ShowDebugButtons` 0. 
  
В Outlook 2010 и клиентских приложениях, начиная с Office 2013, кнопки отлаки отображаются на вкладке "Надстройки" ленты проводника.  В Outlook 2007 и Outlook 2003 кнопки отлаки отображаются на стандартной панели команд окна проводника Outlook. 
  
В следующей таблице описаны кнопки отлаки.
  
|**Кнопка отлаки**|**Function**|
|:-----|:-----|
|Синхронизация контактов  <br/> |Заставляет OSC запросить у поставщика OSC только кэшировать контакты.  <br/> |
|Синхронизация gal  <br/> |Вызывает заполнение osc данными из глобального списка адресов Exchange для контактов Outlook.  <br/> |
|Недействительный кэш категорий  <br/> |Вызывает перезагрузку списка категорий для каждого магазина при обновлении веб-канала активности.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler — это средство отладки по сети для проверки вызовов API, отправленных поставщиком в социальные сети, и XML- и XML-данных, отправленных социальной сетью поставщику. Fiddler можно скачать на [прокси-сервере веб-отладки Fiddler.](https://www.fiddler2.com/fiddler2/version.asp)
  
## <a name="see-also"></a>См. также

- [Быстрые шаги по обучению разработке поставщика](quick-steps-for-learning-to-develop-a-provider.md)  
- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md) 
- [Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)  
- [Разработка поставщика с помощью схемы OSC XML](developing-a-provider-with-the-osc-xml-schema.md)  
- [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md)

