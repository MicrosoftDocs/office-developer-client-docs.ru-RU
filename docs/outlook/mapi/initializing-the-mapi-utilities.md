---
title: Инициализация служебных программ MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0507a26b9ae5ae018111e2771e3af8b25761786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567673"
---
# <a name="initializing-the-mapi-utilities"></a>Инициализация служебных программ MAPI

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Если только часть MAPI, которые необходимы для использования являются служебных программ, интерфейсы и функции, объявленные в MAPIUTIL MAPI's. Файл заголовка **IPropData** и **ITableData** — необходимо вызвать **MAPIInitialize** для инициализации. Дополнительные сведения можно [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md). Вместо этого вызовите функцию **ScInitMapiUtil** . Для получения дополнительных сведений см [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** позволяет клиентским приложениям использовать вспомогательные функции и методы, требующие выделения пространства MAPI, однако, не запрашивать их явным образом. 
  
Во время завершения вызова с **DeinitMapiUtil** для освобождения ресурсов, подключенных к служебных программ. Не вызывайте **MAPIUninitialize**. Для получения дополнительных сведений см [DeinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize](mapiuninitialize.md).
  
Обратите внимание, что интерфейс **ITableData** не поддерживает уведомления о таблице для клиентов, которые вызвали **ScInitMapiUtil** , а не **MAPIInitialize**. 
  

