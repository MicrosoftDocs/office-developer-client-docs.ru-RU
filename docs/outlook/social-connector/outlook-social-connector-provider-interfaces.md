---
title: Интерфейсы поставщика социальных соединителей Outlook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) — это компонент Office, совместно используемый клиентскими приложениями Office, которые подключаются к социальным и деловым сетям, поэтому пользователи могут оставаться на связи с людьми в своих сетях, не выходя из Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422812"
---
# <a name="outlook-social-connector-provider-interfaces"></a>Интерфейсы поставщика социальных соединителей Outlook

Outlook Social Connector (OSC) — это компонент Office, совместно используемый клиентскими приложениями Office, которые подключаются к социальным и деловым сетям, поэтому пользователи могут оставаться на связи с людьми в своих сетях, не выходя из Office. 
  
Поставщик OSC — это DLL-библиотека COM, которая позволяет OSC получать доступ к данным социальных сетей так, как это не зависит от API каждой социальной сети. В следующей таблице перечислены интерфейсы расширяемости поставщика OSC. Поставщик OSC должен реализовать четыре из пяти интерфейсов для общения с OSC: [исоЦиалперсон](isocialpersoniunknown.md), [исоЦиалпрофиле](isocialprofileisocialperson.md), [исоЦиалпровидер](isocialprovideriunknown.md)и [настроенный ISocialSession](isocialsessioniunknown.md). Если поставщик OSC поддерживает синхронизацию действий, выполнение по требованию или гибридную синхронизацию друзей, кэширование учетных данных входа и вход в систему с использованием кэшированных учетных данных или возможность отслеживать человека, то поставщик также должен реализовать [ISocialSession2](isocialsession2iunknown.md).
  
|**Название**|**Описание**|
|:-----|:-----|
|[исоЦиалперсон](isocialpersoniunknown.md) <br/> |Представляет пользователя в социальной сети.  <br/> |
|[исоЦиалпрофиле](isocialprofileisocialperson.md) <br/> |Представляет пользователя, выполнившего вход в систему.  <br/> |
|[исоЦиалпровидер](isocialprovideriunknown.md) <br/> |Представляет экземпляр поставщика OSC.  <br/> |
|[Настроенный ISocialSession](isocialsessioniunknown.md) <br/> |Представляет подключение к сайту социальных сетей.  <br/> |
|[ISocialSession2](isocialsession2iunknown.md) <br/> |Поддерживает синхронизацию действий, добавление друзей, по запросу или гибридную синхронизацию друзей, а также вход в социальную сеть с помощью кэшированных учетных данных.  <br/> |
   

