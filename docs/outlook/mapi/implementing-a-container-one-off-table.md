---
title: Реализация одноразовой таблицы контейнеров
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809286"
---
# <a name="implementing-a-container-one-off-table"></a>Реализация одноразовой таблицы контейнеров

  
  
**Относится к**: Outlook 
  
Для доступа к таблице одноразовых, относящегося к одному из вашего контейнеров, MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера, чтобы открыть свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) с **IMAPITable** интерфейс. Контейнера запрос для возврата его одноразовых таблицы при попытке добавить получателя в контейнере клиентского приложения. Если контейнер разрешает получателям, ваш поставщик может возвращаются собственная реализация таблицы или вызова [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) для возврата реализации интерфейса MAPI. 
  
Набор шаблонов в таблице одноразовых контейнер должны отражаться тип получателей, которые могут содержать конкретным контейнером. Как правило включает один или два шаблоны, шаблоны для создания отдельного пользователя обмена мгновенными сообщениями или список рассылки. Идентификаторы записей для этих шаблонов хранятся в свойства **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) и **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)). Тем не менее контейнеры являются далеко не только следующие типы записей. Они могут содержать других типов получателей или записи без получателя каталоги. 
  

