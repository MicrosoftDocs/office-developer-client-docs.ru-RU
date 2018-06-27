---
title: О приглашений на собрания как информационные и полного обновления
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 084928ca-efc0-36da-fe4f-5cc45f226178
description: Приглашения на собрание — это сообщение электронной почты с IPM. Schedule.Meeting.Request как класс сообщения. По умолчанию участниками принимать приглашения на собрание отвечает на него напрямую.
ms.openlocfilehash: 3565b2af03ef79d70fc9f2817c64a788f031c416
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807676"
---
# <a name="about-meeting-requests-as-informational-updates-and-full-updates"></a>О приглашений на собрания как информационные и полного обновления

Приглашения на собрание — это сообщение электронной почты с **IPM. Schedule.Meeting.Request** как класс сообщения. По умолчанию участниками принимать приглашения на собрание отвечает на него напрямую. Outlook поддерживает настройку делегатов, которые могут отвечать на приглашения на собрания от имени субъекта получателя. Программными средствами Outlook устанавливается именованное свойство [PidLidMeetingType](http://msdn.microsoft.com/library/290b290c-7836-4a7e-bf1a-8d0225a07e56%28Office.15%29.aspx) приглашения на собрание, чтобы определить текущее состояние обновления. 
  
## <a name="recipients-without-delegates"></a>Получатели без делегатов

Когда Outlook получает нового приглашения на собрание, свойство **PidLidMeetingType** запроса на проведение собрания элемент **mtgRequest**наборов Outlook. Все последующие обновления этого собрания — **mtgFullUpdate** (полное обновление) или **mtgInfoUpdate** (информационные обновление) в зависимости от причины обновления с помощью Outlook, параметру **PidLidMeetingType** соответствующим образом. Полное обновление требует участником явным образом отвечать на приглашения на собрание и информационные обновления — нет. 
  
## <a name="full-updates"></a>Полное обновление

Существует два сценария, которые ведут к полного обновления.
  
- Когда инициатора изменяется дата, время, часовые пояса или повторения предыдущего приглашения на собрание, организатор необходимо отправить обновление всех участников. Это обновление является полное обновление, к которому участником необходимо явно отвечать на уведомление Организатор присутствия, так как Outlook игнорирует любые предыдущие ответы.
    
- Если участник не отвечает на запрос начального собрания и получает последующие обновления, начальное собрание становится устаревшим и обновление не полного обновления, независимо от того, причина обновления.
    
## <a name="informational-updates"></a>Информационные обновлений

Существует четыре сценария, в которых Outlook приводит к возникновению ошибки информационные обновления. В следующих сценариях реагирование на информационные обновления не является обязательным.
  
- Если инициатора изменяется местоположение предыдущего приглашения на собрание, организатор необходимо отправить обновление всех участников. Если участник уже приняли начального приглашения на собрание, участником получает обновление как информационные обновление.
    
- Если инициатора добавляет участника в предыдущей приглашения на собрание, организатор должны отправлять приглашения на собрание на новом добавленном attendee и имеет параметр для включения существующего собрания обновление. Только что добавленный участник получает запрос на собрание как новый запрос. По желанию организатора отправить обновление существующих участников участники получают обновление как информационные обновление.
    
- Если инициатора Удаление участника из предыдущего приглашения на собрание, организатор необходимо отправить обновление участнику, который был удален из приглашения на собрание и имеет возможность включить существующий участников на обновление. Участники получают обновление как информационные обновление.
    
- Если инициатора изменяется тема или текст из предыдущего приглашения на собрание, Организатор может отправить обновление участникам или просто сохранить изменения для организатора собственные копии приглашения на собрание. По желанию организатора отправить обновление участники получают обновление как информационные обновление.
    
## <a name="recipients-set-up-with-delegates"></a>Настройка получателей с помощью делегатов

Получателей, которые настройки делегаты могут быть делегаты ответ на приглашение на собрание, не отмеченные Private. По умолчанию участник получает копию приглашения на собрание или копию обновление предыдущей приглашения на собрание и делегаты всегда получают исходного приглашения на собрание или исходное обновление полного или информационные. В этой конфигурации по умолчанию субъекта всегда получает делегированные приглашения на собрания и обновления; делегаты субъекта получать приглашения на собрания как новые приглашений на собрания, полного обновления или информационные обновления, описанные для получателей без делегаты, представленные в разделе «Получателям без делегаты».
  
По умолчанию участников можно выбрать ответ на приглашения на собрания неконфиденциальные и обновления, даже если делегаты зависят от выбора этого от их имени. Тем не менее Кроме того, администраторы можно настроить политику для предотвращения участника получателей отвечать на запросы.
  
