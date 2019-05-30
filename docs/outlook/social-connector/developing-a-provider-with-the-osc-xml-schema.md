---
title: Разработка поставщика с использованием схемы XML OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Схема XML поставщика Outlook Social Connector (OSC) определяет формат значительного объема данных, передаваемых из социальной сети через поставщик OSC сети на OSC.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539257"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Разработка поставщика с использованием схемы XML OSC

Схема XML поставщика Outlook Social Connector (OSC) определяет формат значительного объема данных, передаваемых из социальной сети через поставщик OSC сети на OSC. Схема XML позволяет поставщику OSC указывать возможности элементов "поставщик", "друзья" и "канал активности" в социальной сети, используя три основных элемента, **возможности**, **друзья**и **activityFeed**, а также их дочерние элементы. элемента. Поставщик OSC реализует интерфейсы и их методы в расширяемости поставщика OSC, возвращая XML-строки в качестве выходных параметров, которые соответствуют схеме XML поставщика OSC. OSC вызывает эти методы для получения информации, которая может быть определена схемой XML.
  
> [!NOTE]
> Расширяемость поставщика OSC поддерживает поставщиков отладки путем установки `DebugProviders` для раздела `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` реестра значения 1. Когда вы включаете отладку поставщика, OSC проверяет XML-код поставщика на соответствие версии XML-схемы OSC, указанной в атрибуте **xmlns** XML. Для OSC 1,1 и версий файла OSC, начиная с Outlook Social Connector 2013, укажите атрибут **xmlns** следующим образом:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>В этом разделе:

- [Синхронизация друзей и действий](synchronizing-friends-and-activities.md): в этой статье описываются различные способы синхронизации с друзьями, недрузьями и действиями в социальных сетях. 
    
- [Примеры XML-кода поставщика OSC](osc-provider-xml-examples.md): включает XML-примеры, демонстрирующие, как указать возможности поставщика OSC, друзей и элементов веб-каналов активности в социальной сети с помощью XML-схемы OSC.
    
- [XML для возможностей](xml-for-capabilities.md): объясняющий метод- [исоЦиалпровидер::-CAPABILITIES](isocialprovider-getcapabilities.md) , который OSC использует для получения сведений о возможностях, представленных в XML-коде **возможностей** , от поставщика OSC. В этом разделе также описаны XML-элементы в XML-схеме поставщика OSC, позволяющие поставщику OSC указывать свои функции, в том числе способ проверки подлинности пользователей и синхронизации друзей и действий. 
    
- [XML для друзей](xml-for-friends.md): содержит примеры интерфейсов API, которые OSC использует для получения сведений о друзьях, выраженных в XML-коде **друзей** , от поставщика OSC. В этом разделе также описываются элементы в XML-коде **друзей** . 
    
- [XML для действий](xml-for-activities.md): содержит примеры интерфейсов API, которые OSC использует для получения сведений о действиях, представленных в XML **activityFeed** , от поставщика OSC. В этом разделе также описываются XML-элементы в XML-схеме поставщика OSC, которые позволяют поставщику OSC указать канал активности. Канал активности включает сеть, в которой созданы элементы веб-канала активности, сведения о каждом элементе веб-канала активности (например, сведения о владельце, типе и публикации даты действия), а также шаблон для отображения действия. 
    
## <a name="reference"></a>Справочные материалы

- [Справочник по поставщику Outlook Social Connector](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Связанные разделы

- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Примеры шаблонов OSC](osc-sample-templates.md)
  
- [Переosc типичные последовательности вызовов](osc-typical-calling-sequences.md)
  
- [Отладка поставщика](debugging-a-provider.md)
  
- [Развертывание поставщика](deploying-a-provider.md)
  
- [Рекомендации по разработке поставщика](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>См. также

- [Отладка поставщика](debugging-a-provider.md)

