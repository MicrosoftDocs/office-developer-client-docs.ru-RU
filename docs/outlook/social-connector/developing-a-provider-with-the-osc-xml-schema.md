---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительное сведения, передаваемые из социальных сетей через сеть OSC поставщика OSC.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812723"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Разработка поставщика с использованием схемы XML OSC

XML-схема поставщика Outlook Social Connector (OSC) определяет формат значительное сведения, передаваемые из социальных сетей через сеть OSC поставщика OSC. Схема XML позволяет поставщика OSC для указания возможностей поставщика, друзей и веб-канал элементов в социальных сетях, используя три основных элемента, **возможности**, **друзей**и **activityFeed**и их дочерних активности элементы. Поставщика OSC реализует интерфейсы и методы их возможности расширения поставщика OSC возвращение строк XML как выходные параметры, совместимые с использованием схемы XML поставщика OSC. OSC вызывает эти методы для получения информации, которая понять, как указано в схеме XML.
  
> [!NOTE]
> Возможности расширения поставщика OSC поддерживает отладки поставщиков, задав `DebugProviders` значение `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` раздела реестра значение 1. При включении отладки поставщика OSC проверяет поставщика XML для версии схемы XML для OSC, указанные в XML-атрибут **xmlns** . Для OSC 1.1 и версий OSC с момента Outlook Social Connector 2013 укажите атрибут **xmlns** следующим образом.`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>В этой статье

- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md): описываются различные способы, поставщики OSC можно синхронизировать друзей, не являющиеся друзей и действий в социальных сетях. 
    
- [Примеры XML поставщика OSC](osc-provider-xml-examples.md): включает в себя XML примеры, показывающие, как для указания возможностей поставщика OSC, друзей и активности веб-канала элементы в социальных сетях с использованием схемы XML для OSC.
    
- [XML-код для возможности](xml-for-capabilities.md): описание - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) метод, который OSC используется для получения сведений о возможностях, выраженная в **возможности** XML, от поставщика OSC. В этом разделе также описываются элементы XML в XML-схему поставщика OSC, позволяющих поставщика OSC указать его функциональные возможности, включая как оно выполняет проверку подлинности пользователей, а также сведения об друзей и действия. 
    
- [XML-код для друзей](xml-for-friends.md): приведены примеры интерфейсов API, OSC для получения сведений о друзей, выраженная в **друзья** XML, от поставщика OSC. В этом разделе также описываются элементы в **друзья** XML. 
    
- [XML-код для действий](xml-for-activities.md): приведены примеры интерфейсов API, OSC для получения сведений о действиях, выраженная в **activityFeed** XML, от поставщика OSC. В этом разделе также описываются элементы XML в XML-схему поставщика OSC, позволяющих поставщика OSC указать веб-канал активности. Веб-канал активности включает в себя сеть, где веб-канала активности элементов была создана, подробные сведения для каждого веб-канал активности элемента (например, владельца, введите и дата действия публикации) и шаблон для отображения действия. 
    
## <a name="reference"></a>Справочные материалы

- [Справочник поставщика по Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Шаблоны OSC примера](osc-sample-templates.md)
  
- [Типичные последовательности вызовов OSC](osc-typical-calling-sequences.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Рекомендации по разработке поставщика](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [Отладка поставщика](debugging-a-provider.md)

