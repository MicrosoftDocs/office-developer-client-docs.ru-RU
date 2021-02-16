---
title: Использование utilities MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409988"
---
# <a name="using-the-mapi-utilities"></a>Использование utilities MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Utilities MAPI are made up of table data and property data objects and a variety of functions to support miscellaneous features. Клиент может нуждаться только в этих средствах и не должен входить в подсистему MAPI для установления связи с поставщиками услуг. Если клиент помещается в эту категорию, вызовите функцию API [ScInitMapiUtil,](scinitmapiutil.md) а не [функцию MAPIInitialize](mapiinitialize.md) во время инициализации. 
  
 **ScInitMapiUtil** позволяет клиентам использовать дополнительные функции, для которых требуются средства назначения MAPI, но которые не требуют явного назначения. Когда пора закрыть работу, вызовите [DeinitMapiUtil,](deinitmapiutil.md) чтобы освободить ресурсы, а [не MAPIUninitialize.](mapiuninitialize.md) Клиенты, которые никогда не **вызывали MAPIInitialize,** не должны **вызывать MAPIUninitialize.**
  
Если вы вызвали **ScInitMapiUtil,** а не **MAPIInitialize** и используете таблицы с помощью методов **ITableData,** а не с помощью методов **IMAPITable,** следует помнить, что уведомления таблиц не будут работать. Для уведомлений необходимо использовать библиотеки MAPI и [IMAPITable : IUnknown](imapitableiunknown.md).
  

