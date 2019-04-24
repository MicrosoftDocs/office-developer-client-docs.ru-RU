---
title: Реализация одноразовой таблицы контейнера
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332888"
---
# <a name="implementing-a-container-one-off-table"></a>Реализация одноразовой таблицы контейнера

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Для доступа к односторонней таблице, принадлежащей одному из контейнеров, MAPI вызывает метод контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **пр_креате_темплатес** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с помощью **IMAPITable** . взаимодействия. В вашем контейнере предлагается возврат обратной таблицы, когда клиентское приложение пытается добавить получателя в контейнер. Если контейнер позволяет любому получателю, поставщик может возвратить свою собственную реализацию или вызов [имаписуппорт:: жетонеоффтабле](imapisupport-getoneofftable.md) , чтобы вернуть реализацию MAPI. 
  
Набор шаблонов в таблице отбираемых контейнеров должен отражать тип получателей, которые могут храниться в определенном контейнере. Как правило, это включает один или два шаблона, шаблоны для создания отдельного пользователя обмена сообщениями или списка рассылки. Идентификаторы записей для этих шаблонов хранятся в свойствах **пр_деф_креате_маилусер** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) и **пр_деф_креате_дл** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Однако контейнеры не ограничиваются этими типами записей. Они могут содержать других типов получателей или записей, отличных от получателей, таких как каталоги. 
  

