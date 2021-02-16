---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539257"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Разработка поставщика с использованием схемы XML OSC

XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительного объема информации, которая передается из социальной сети через поставщика OSC сети в OSC. Схема XML позволяет поставщику OSC указывать возможности поставщика, друзей и элементов веб-канала активности в социальной сети с помощью трех основных элементов, **возможностей,** друзей и **activityFeed** и их потомков. Поставщик OSC реализует интерфейсы и их методы в реализации возможностей поставщика OSC, возвращая строки XML в качестве выходных параметров, которые соответствуют XML-схеме поставщика OSC. OsC вызывает эти методы для получения сведений, которые могут быть понятны в схеме XML.
  
> [!NOTE]
> Возможность extensibility поставщика OSC поддерживает поставщиков отладки, устанавливая для ключа реестра значение `DebugProviders`  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` 1. При включении отладки поставщика OSC проверяет XML поставщика на основе версии схемы OSC XML, задаемой в атрибуте **XML xmlns.** Для OSC 1.1 и версий OSC, начиная с Outlook Social Connector 2013, укажите **атрибут xmlns** следующим образом: `xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>В этом разделе:

- [Синхронизация друзей](synchronizing-friends-and-activities.md)и действий : описание различных способов, которыми поставщики OSC могут синхронизировать друзей, не друзей и действия в социальной сети. 
    
- [XML-примеры](osc-provider-xml-examples.md)поставщика OSC : содержит примеры XML, которые показывают, как задать возможности поставщика OSC, друзей и элементов веб-канала активности в социальной сети с помощью схемы OSC XML.
    
- [XML for Capabilities](xml-for-capabilities.md): Explains the - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that the OSC uses to obtain capabilities information, expressed in **capabilities** XML, from the OSC provider. В этом разделе также описываются XML-элементы схемы XML поставщика OSC, которые позволяют поставщику OSC указывать свои функции, включая проверку подлинности пользователей и синхронизацию друзей и действий. 
    
- [XML для друзей](xml-for-friends.md): предоставляет примеры API, которые OSC использует для получения сведений о друзьях, выраженных **в** XML друзей, от поставщика OSC. В этом разделе также описываются элементы **XML-разных друзей.** 
    
- [XML для действий](xml-for-activities.md): предоставляет примеры API, которые OSC использует для получения сведений о действиях, выраженных в **XML activityFeed,** от поставщика OSC. В этом разделе также описываются XML-элементы в XML-схеме поставщика OSC, которые позволяют поставщику OSC указывать веб-канал активности. Веб-канал активности включает сеть, в которой ились элементы веб-канала активности, сведения о каждом элементе веб-канала активности (например, владелец, тип и дата публикации действия) и шаблон для отображения действия. 
    
## <a name="reference"></a>Справка

- [Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Примеры шаблонов OSC](osc-sample-templates.md)
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [Отладка поставщика](debugging-a-provider.md)

