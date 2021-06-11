---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Схема XML Outlook поставщика социальных соединителем (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539257"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Разработка поставщика с использованием схемы XML OSC

Схема XML Outlook поставщика социальных соединителем (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC. Схема XML позволяет поставщику OSC указывать возможности поставщика, друзей и элементов каналов активности в социальной сети с помощью трех основных элементов, **возможностей,** друзей и элементов **activityFeed** и их детских элементов. Поставщик OSC реализует интерфейсы и их методы в extensibility поставщика OSC, возвращая строки XML в качестве выходных параметров, которые соответствуют схеме XML поставщика OSC. OsC вызывает эти методы для получения информации, которую она может понять, как определено схемой XML.
  
> [!NOTE]
> Экстенсивность поставщика OSC поддерживает отладку поставщиков, устанавливая значение ключа реестра `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` до 1. При включении отладки поставщика OSC проверяет XML поставщика на версию схемы XML OSC, указанную в атрибуте **XML xmlns.** Для OSC 1.1 и версий OSC с Outlook Social Connector 2013 укажите атрибут **xmlns** следующим образом:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>В этом разделе

- [Синхронизация друзей](synchronizing-friends-and-activities.md)и действий. Описывает различные способы синхронизации друзей, не друзей и действий в социальной сети. 
    
- [Примеры XML поставщика OSC:](osc-provider-xml-examples.md)Включает примеры XML, которые показывают, как указать возможности поставщика OSC, друзей и элементов каналов активности в социальной сети с помощью схемы XML OSC.
    
- [XML для](xml-for-capabilities.md)возможностей. Объясняет метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) который OSC использует для получения сведений о возможностях, выраженных в возможностях **XML,** от поставщика OSC. В этом разделе также описываются элементы XML в схеме XML-поставщика OSC, которые позволяют поставщику OSC указать его функциональность, в том числе то, как он обеспечивает проверку подлинности пользователей и синхронизирует работу с друзьями и действиями. 
    
- [XML для друзей.](xml-for-friends.md)Приводит примеры API, которые OSC использует для получения сведений друзей, выраженных в **друзьях** XML, от поставщика OSC. В этом разделе также описываются элементы XML **друзей.** 
    
- [XML для действий](xml-for-activities.md). Приводит примеры API, которые OSC использует для получения сведений о действиях, выраженных в **activityFeed** XML, от поставщика OSC. В этом разделе также описываются элементы XML в схеме XML поставщика OSC, которые позволяют поставщику OSC указывать канал активности. Канал действий включает сеть, в которой появились элементы ленты действий, сведения о каждом элементе ленты действий (например, владелец, тип и дата публикации действия), а также шаблон для отображения действия. 
    
## <a name="reference"></a>Справочные материалы

- [Outlook Справка о поставщике социальных соединители](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало работы с разработкой Outlook поставщика социальных соединители](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Шаблоны образцов OSC](osc-sample-templates.md)
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Лучшие практики для разработки поставщика](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [Отладка поставщика](debugging-a-provider.md)

