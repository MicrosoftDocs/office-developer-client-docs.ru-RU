---
title: Инициализация utilities MAPI
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
# <a name="initializing-the-mapi-utilities"></a>Инициализация utilities MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если необходимо использовать только программы MAPI, интерфейсы и функции, объявленные в MAPI MAPI MAPI. Файл H-загона, например **IPropData** и **ITableData,** не требуется вызывать **MAPIInitialize** для инициализации. Дополнительные сведения см. в [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md). Вместо этого вызовите **функцию ScInitMapiUtil.** Дополнительные сведения [см. в подразделе ScInitMapiUtil.](scinitmapiutil.md) **ScInitMapiUtil** позволяет клиентские приложения использовать функции и методы, для которых требуются средства назначения MAPI, но которые не требуют их явно. 
  
Во время завершения работы вызовите **DeinitMapiUtil,** чтобы освободить ресурсы, подключенные к средствам. Не **вызывай MAPIUninitialize.** Дополнительные сведения [см. в подразделах DeinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize.](mapiuninitialize.md)
  
Следует помнить, что интерфейс **ITableData** не поддерживает уведомления таблиц для клиентов, которые вызвали **ScInitMapiUtil,** а **не MAPIInitialize**. 
  

