---
title: Реализация таблицы One-Off контейнеров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417422"
---
# <a name="implementing-a-container-one-off-table"></a>Реализация таблицы One-Off контейнеров

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Чтобы получить доступ к разовой таблице, принадлежащей одному из контейнеров, MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия свойства **PR_CREATE_TEMPLATES** [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)с интерфейсом **IMAPITable.** Контейнеру будет предложено вернуть разовую таблицу при попытке клиентского приложения добавить получателя в контейнер. Если контейнер позволяет получателям, поставщик может либо вернуть собственную реализацию таблицы, либо вызвать [IMAPISupport::GetOneOffTable,](imapisupport-getoneofftable.md) чтобы вернуть реализацию MAPI. 
  
Набор шаблонов в одноразовой таблице контейнера должен отражать тип получателей, которые может держать определенный контейнер. Как правило, это один или два шаблона, шаблоны для создания отдельного пользователя обмена сообщениями или списка рассылки. Идентификаторы записи для этих шаблонов **находятся** в свойствах [PR_DEF_CREATE_MAILUSER (PidTagDefCreateMailuser)](pidtagdefcreatemailuser-canonical-property.md)и **PR_DEF_CREATE_DL** [(PidTagDefCreateDl).](pidtagdefcreatedl-canonical-property.md) Однако контейнеры не ограничиваются этими типами записей. Они могут держать другие типы получателей или записи, не получатели, такие как каталоги. 
  

