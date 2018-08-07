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
ms.openlocfilehash: 3f461d50e838aac0caee37d295ba8e86b9559bd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812584"
---
# <a name="using-the-mapi-utilities"></a>Использование служебных программ MAPI

  
  
**Относится к**: Outlook 
  
Служебные программы MAPI состоят из таблицы данных и объекты данных свойств и множество функций для поддержки функций Разное. Существует возможность клиенту требуются только этих служебных программ и не должны входить в подсистему MAPI для установления соединения с поставщиками услуг. Если ваш клиент умещается в этой категории, вызовите функцию API [ScInitMapiUtil](scinitmapiutil.md) вместо функции [MAPIInitialize](mapiinitialize.md) во время инициализации. 
  
 **ScInitMapiUtil** позволяет клиентам использовать функции служебной программы, требующие выделения пространства MAPI, однако, не запрашивать выделения пространства явным образом. Когда это время остановки вызов [DeinitMapiUtil](deinitmapiutil.md) для освобождения ресурсов, а не [MAPIUninitialize](mapiuninitialize.md). Клиенты, которые никогда не могут вызывать **MAPIInitialize** не должны вызывать **MAPIUninitialize**.
  
Если уже звонил **ScInitMapiUtil** , а не **MAPIInitialize** и с помощью таблиц **ITableData** способами, а не через методы **IMAPITable** , обратите внимание, уведомления о таблице не будут работать. Уведомления о требуется использование библиотек MAPI и [IMAPITable: IUnknown](imapitableiunknown.md).
  

