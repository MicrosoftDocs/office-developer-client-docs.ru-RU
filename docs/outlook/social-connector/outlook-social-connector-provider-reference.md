---
title: Справочник по поставщикам Outlook Social Connector
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 предоставляет центр связи для личных и профессиональных коммуникаций.
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359838"
---
# <a name="outlook-social-connector-provider-reference"></a>Справочник по поставщикам Outlook Social Connector

Outlook Social Connector 2013 предоставляет центр связи для личных и профессиональных коммуникаций. Outlook Social Connector (OSC) работает с SharePoint Server, SharePoint Workspace, клиентом Lync и всеми клиентские приложения Office, которые поддерживают сведения о присутствии и карточку контакта, поддерживают OSC. 

В outlook, в частности, просто выбрав элемент Outlook, например сообщение электронной почты или запрос на собрание, и щелкнув отправитель или получателя в этом элементе, не выходя из Outlook, пользователи могут видеть в действиях области людей, фотографии и обновлениях состояния этого пользователя в избранных социальных сетях. Пользователи могут легко видеть все сообщения электронной почты, вложения и собрания Outlook, полученные от этого человека. В среде организации пользователи сайта SharePoint также могут видеть обновления документов области людей и другие действия этого пользователя на сайте SharePoint.
  
Социальная сеть может разработать поставщика для OSC для синхронизации и создания обновлений социальных сетей на вспомогательных серверах и в приложениях. Популярные социальные сети, такие как LinkedIn, Facebook и Windows Live, предлагают поставщиков для OSC. 
  
В справочнике по поставщикам Outlook Social Connector 2013 описывается разработка поставщика OSC с использованием возможности extensibility поставщика OSC. 
  
Если у вас нет опыта разработки решений для Outlook, см. статью [Выбор API или технологии разработки решений для Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md), чтобы выбрать API-интерфейсы и технологии, наиболее соответствующие вашим потребностям. 
  
## <a name="in-this-section"></a>В этом разделе:

- Начало работы с разработкой поставщика [Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md): обзор OSC, в том числе: как поставщик OSC может быть полезным, быстрые шаги для изучения разработки поставщика, технические требования, советы и новые возможности в этом выпуске.
    
- [Примеры шаблонов OSC](osc-sample-templates.md): описание Visual Studio шаблонов для разработки поставщика.
    
- Типичные последовательности [вызовов OSC](osc-typical-calling-sequences.md): описывает несколько типичных последовательностей вызовов osC членов в интерфейсах extensibility поставщика OSC. Это позволит лучше понять, как реализовать эти интерфейсы.
    
- Разработка поставщика с помощью схемы [OSC XML](developing-a-provider-with-the-osc-xml-schema.md): описывает, как интерфейсы extensibility поставщика OSC и схема OSC XML предназначены для поддержки поставщика OSC.
    
- [Отладка поставщика:](debugging-a-provider.md)предлагает несколько способов отладки поставщика OSC.
    
- [Развертывание поставщика](deploying-a-provider.md): описывает требования к регистрации для поставщика OSC и предоставляет контрольный список для установки поставщика.
    
- [Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releaseing an OSC provider.
    
- [Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.
    
## <a name="see-also"></a>См. также

- [Уведомление об авторских правах для поставщика Outlook Social Connector 2013](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [Условные обозначения в документах (Возможно, на английском языке)](https://msdn.microsoft.com/office/aa905365.aspx)   
- [Специальные возможности в продуктах Майкрософт (Возможно, на английском языке)](https://www.microsoft.com/enable/products/default.aspx)  
- [Уведомление о конфиденциальности (Майкрософт), доступное в Интернете](https://privacy.microsoft.com/en-us/privacystatement)
    

