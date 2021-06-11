---
title: Инициализация утилит MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420950"
---
# <a name="initializing-the-mapi-utilities"></a>Инициализация утилит MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Если единственной частью MAPI, которую необходимо использовать, являются утилиты — интерфейсы и функции, объявленные в MAPI MAPI. H заглавной файл, такие как **IPropData** и **ITableData** — вам не нужно вызывать **MAPIInitialize** для инициализации. Дополнительные сведения см. в [iPropData : IMAPIProp,](ipropdataimapiprop.md) [ITableData : IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md). Вместо этого позвоните **в функцию ScInitMapiUtil.** Дополнительные сведения см. [в ст. ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** позволяет клиентские приложения использовать полезные функции и методы, для которых требуются аллигаторы MAPI, но которые не требуют их явно. 
  
Во время остановки позвоните **в DeinitMapiUtil,** чтобы освободить ресурсы, подключенные к утилитам. Не **вызывай MAPIUninitialize**. Дополнительные сведения см. [в deinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize.](mapiuninitialize.md)
  
Следует помнить, что интерфейс **ITableData** не поддерживает таблицы уведомлений для клиентов, которые вызвали **ScInitMapiUtil,** а **не MAPIInitialize**. 
  

