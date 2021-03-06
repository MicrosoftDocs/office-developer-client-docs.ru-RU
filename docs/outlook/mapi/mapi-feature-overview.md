---
title: Обзор функций MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b1087f5156ad79b20eb31ef55c0388ffd82e1601
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416925"
---
# <a name="mapi-feature-overview"></a>Обзор функций MAPI
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI имеет несколько ключевых функций, которые позволяют разработчикам работать с различными системами обмена сообщениями и использовать их в бесшовном режиме. Эти функции включают комплексный и открытый интерфейс программирования и поддержку отраслевых стандартов. 
  
Так как MAPI — это открытый интерфейс программирования, он предоставляет службы общим способом, что позволяет пользователям добавлять любую необходимую настройку сейчас и в будущем. Интерфейс программирования MAPI выполняет требования клиентских приложений с различными потребностями в обмене сообщениями, такими как приложение обработки слов, которое требует только возможности отправки документов или приложения workgroup, которое требует возможности обмена и хранения различных типов данных. На самом деле любое приложение, необходимое для обмена или хранения информации в определенном формате, может воспользоваться интерфейсом программирования MAPI. Любой поставщик услуг может использовать интерфейс для разоблачения уникальных функций своей системы обмена сообщениями, выбрав те функции, которые обеспечивают наибольшее преимущество для пользователей приложений.
  
MAPI обеспечивает разделение интерфейса программирования, используемого в клиентских приложениях для обмена сообщениями, и интерфейсом программирования, используемым поставщиками услуг. Отделение клиентского интерфейса от поставщика услуг позволяет одному приложению использовать несколько систем обмена сообщениями и несколько приложений для использования одного поставщика услуг. Каждый компонент работает с общим пользовательским интерфейсом Windows microsoft. Это большое преимущество для пользователей. Пользователи могут выбирать из различных систем в зависимости от их потребностей в любое время и могут последовательно работать с каждой выбранной системой, обеспечивая тем самым настоящую независимость от определенных систем обмена сообщениями. 
  
Например, одно клиентские приложения для обмена сообщениями могут получать сообщения из факса, голосовой почты и канала RSS. Сообщения из всех этих систем можно размещать в одном расположении или универсальном почтовом ящике по прибытии. Наличие единого приложения для обработки всех этих систем позволяет уменьшить затраты на разработку, обучение пользователей и администрирование системы. 
  
Разделение клиентского интерфейса с интерфейсом поставщика устраняет любые зависимости программирования, размещенные в приложении системой обмена сообщениями, и наоборот. Разработчики клиентских приложений и поставщиков услуг записывают код в стандартный набор функций MAPI, а не разнообразный набор функций, специфических для приложений или систем обмена сообщениями. Разработчики фокусируется только на своем компоненте, будь то клиент или поставщик услуг, а MAPI обрабатывает все остальное, сокращая время разработки и затраты.
  
Интерфейс программирования MAPI предоставляет полный набор функций. MAPI ориентирована на новый мощный рынок приложений workgroup — приложений, которые взаимодействуют с такими различными системами обмена сообщениями, как факс, DEC All-In-1, голосовая почта и службы общественных коммуникаций, такие как AT&T Easylink Services, CompuServe и MCI MAIL. Интерфейс MAPI позволяет поставщикам услуг быть доступными для всех этих систем. 
  
Объекты, совместимые с MAPI, похожи по форме на объекты Component Object Model (COM). Объекты COM реализуют набор методов, которые относятся к одному или более интерфейсам, или коллекции связанных функций, которые определяют поведение объектов и их работу в COM. Пользователи имеют доступ к объектам COM только с помощью указателей на эти интерфейсы.
  
MAPI обеспечивает межплатформовую поддержку с помощью таких отраслевых стандартов, как SMTP и X.400. Приложения MAPI можно запускать Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 и Windows XP. 
  
## <a name="see-also"></a>См. также

- [Функции и архитектура MAPI](mapi-features-and-architecture.md)

