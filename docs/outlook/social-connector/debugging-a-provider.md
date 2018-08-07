---
title: Отладка поставщика
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: 'Существует несколько способов, чтобы выполнить отладку поставщика Outlook Social Connector (OSC):'
ms.openlocfilehash: ada439ca3b038ca9a0e849b47ff6a5f54e5016f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812714"
---
# <a name="debugging-a-provider"></a>Отладка поставщика

Существует несколько способов, чтобы выполнить отладку поставщика Outlook Social Connector (OSC): 
  
- С помощью команды отладки в компоненте ленты пользовательского интерфейса Office Fluent в Outlook или вспомогательные клиентского приложения Office для OSC для выполнения различных действий.
    
- С помощью Fiddler для трассировки API звонки и XML, передаваемая между социальной сети и его поставщика OSC
    
## <a name="debug-buttons"></a>Отладка кнопок

Возможности расширения поставщика OSC предоставляет возможность отладки поставщика OSC. Отладка поставщика, создайте `DebugProviders` значение введите значение DWORD в реестре Windows в разделе `SocialConnector` ключевые (как показано в следующей строке), а значение `DebugProviders` значение 1. 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
По умолчанию поставщик отладки отключен. Если `DebugProviders` значение не задано, или присутствует и выключен присвоено значение 0, отладки поставщика. 
  
Если включена отладка поставщика OSC отображает оповещения диалоговое окно со сведениями об ошибках verbose, когда ошибку и использует для проверки любого поставщика OSC XML соответствие схеме XML поставщика OSC. Основываясь на пространство имен, указанное для XML-строка, поставщика OSC, разработанных с помощью OSC 1.0 проверяется файл схемы версии 1.0 OSC OutlookSocialProvider.xsd. Поставщика OSC разработанных с помощью OSC 1.1 или более поздней версии проверен файл схемы OutlookSocialProvider_1.1.xsd. При использовании `DebugProviders` значение, появляется уведомление о отладки для всех загруженных поставщиков вместо определенного поставщика. 
  
Для отображения кнопки отладки, которые могут помочь в отладке поставщика, создайте `ShowDebugButtons` значение введите значение DWORD в реестре Windows в разделе `SocialConnector` ключа, а значение `ShowDebugButtons` значение 1. Чтобы скрыть кнопки панели команд Отладка, задайте `ShowDebugButtons` значение 0. 
  
Для Outlook 2010 и клиентских приложений с момента Office 2013 кнопки debug отображаются на вкладке **надстройки** на ленте explorer. Для Outlook 2007 и Outlook 2003 кнопки debug отображаются на панели стандартных команд окно проводника Outlook. 
  
В следующей таблице описываются кнопки отладки.
  
|**Отладка кнопки**|**�������**|
|:-----|:-----|
|Синхронизация контактов  <br/> |Вызывает OSC для запроса у поставщика OSC только кэшированные контакты.  <br/> |
|Синхронизация глобального списка адресов  <br/> |Вызывает OSC для заполнения данными из глобального списка адресов Exchange в список контактов.  <br/> |
|Объявить недействительным кэш категории  <br/> |Вызывает OSC будет перезагружена в список категорий для каждого хранилища при обновлении веб-канала активности.  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler — это средство отладки по сети для проверки вызовов API, отправленные от поставщика в социальной сети и XML, отправленные с социальной сети к поставщику. Fiddler доступно для загрузки в [Fiddler отладки прокси-сервера](http://www.fiddler2.com/fiddler2/version.asp).
  
## <a name="see-also"></a>См. также

- [Быстрый шаги, необходимые для разработки поставщика](quick-steps-for-learning-to-develop-a-provider.md)  
- [Синхронизация друзей и действия](synchronizing-friends-and-activities.md) 
- [Рекомендации по разработке поставщика](best-practices-for-developing-a-provider.md)
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)  
- [Разработка поставщика с использованием схемы XML для OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Подготовка к выпуску поставщика OSC](getting-ready-to-release-an-osc-provider.md)

