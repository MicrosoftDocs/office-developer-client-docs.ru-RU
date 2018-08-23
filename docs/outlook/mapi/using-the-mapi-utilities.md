---
title: Использование служебных программ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569535"
---
# <a name="using-the-mapi-utilities"></a>Использование служебных программ MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Служебные программы MAPI состоят из таблицы данных и объекты данных свойств и множество функций для поддержки функций Разное. Существует возможность клиенту требуются только этих служебных программ и не должны входить в подсистему MAPI для установления соединения с поставщиками услуг. Если ваш клиент умещается в этой категории, вызовите функцию API [ScInitMapiUtil](scinitmapiutil.md) вместо функции [MAPIInitialize](mapiinitialize.md) во время инициализации. 
  
 **ScInitMapiUtil** позволяет клиентам использовать функции служебной программы, требующие выделения пространства MAPI, однако, не запрашивать выделения пространства явным образом. Когда это время остановки вызов [DeinitMapiUtil](deinitmapiutil.md) для освобождения ресурсов, а не [MAPIUninitialize](mapiuninitialize.md). Клиенты, которые никогда не могут вызывать **MAPIInitialize** не должны вызывать **MAPIUninitialize**.
  
Если уже звонил **ScInitMapiUtil** , а не **MAPIInitialize** и с помощью таблиц **ITableData** способами, а не через методы **IMAPITable** , обратите внимание, уведомления о таблице не будут работать. Уведомления о требуется использование библиотек MAPI и [IMAPITable: IUnknown](imapitableiunknown.md).
  

