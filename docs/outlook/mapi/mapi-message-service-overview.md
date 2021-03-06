---
title: Обзор службы сообщений MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8973cdcee2b10346d0ba07033357b50f7e9a6a27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406257"
---
# <a name="mapi-message-service-overview"></a>Обзор службы сообщений MAPI
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Служба сообщений определяет группу связанных поставщиков услуг, как правило, поставщиков услуг, которые работают с одной и той же системой обмена сообщениями. В то время как поставщики услуг выполняют работу по связи между системами обмена сообщениями и подсистемой MAPI, службы сообщений выполняют работу взаимодействия между пользователем и поставщиками услуг, которые работают с общей системой обмена сообщениями.  
  
Службы сообщений существуют для упростить установку и настройку поставщиков услуг для пользователей. Пользователи никогда напрямую не устанавливают и не настраивают поставщика услуг; служба сообщений полностью обрабатывает установку и конфигурацию каждого из поставщиков услуг, которые относятся к службе. Из-за этой функции пользователям не нужно быть знакомыми с определенными требованиями к конфигурации поставщика услуг. 
  
На следующем рисунке показана связь между клиентом на основе обмена сообщениями и двумя службами сообщений.
  
**Установка и настройка почтовой службы**
  
![Установка службы сообщений и настройка](media/amapi_44.gif "установки и конфигурации службы сообщений")
  
Пользователь вызывает код установки каждой службы сообщений, чтобы добавить службу и ее поставщиков услуг в профиль. В одной из служб сообщений, показанных на рисунке, существует три поставщика услуг; в другой службе сообщений существует два поставщика услуг. В более позднее время после завершения установки, как правило, во время логоса настраиваются поставщики услуг в каждой службе сообщений. Код конфигурации в каждой службе сообщений обрабатывает конфигурацию поставщиков в службе.
  
При установке службы сообщений программа установки копирует необходимые файлы из источника установки на локальный диск пользователя и обновляет файл конфигурации Mapisvc.inf. Файл Mapisvc.inf содержит параметры конфигурации для всех служб и поставщиков сообщений, которые можно установить на компьютере. Она организована в иерархических разделах с ссылками между каждым разделом на каждом уровне. В разделе на верхнем уровне содержатся сведения, релевантные для подсистемы MAPI, например список всех доступных служб сообщений, а также для установки справки в Интернете. На следующем уровне есть разделы для каждой службы сообщений с такими сведениями, как имя файла DLL службы сообщений и имя ее функции точки входа конфигурации. На третьем уровне есть разделы с данными конфигурации для каждого поставщика услуг в службе сообщений. 
  
Для обработки конфигурации служба сообщений реализует функцию точки входа, которая соответствует прототипу, определенному MAPI, и диалоговое окно на вкладке, известное как лист свойств. MAPI вызывает функцию точки входа для обслуживания клиентских запросов, которые относятся к управлению профилем и управлению поставщиками услуг в службе сообщений. Листы свойств используются для просмотра и изменения свойств службы сообщений и конфигурации поставщика услуг. 
  
## <a name="see-also"></a>См. также

- [Функции и архитектура MAPI](mapi-features-and-architecture.md)

