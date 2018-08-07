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
ms.openlocfilehash: 8ee0504d4a8b9e2ce96e42a53b778d4e3f518fcc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809441"
---
# <a name="initializing-the-mapi-utilities"></a>Инициализация служебных программ MAPI

  
  
**Относится к**: Outlook 
  
Если только часть MAPI, которые необходимы для использования являются служебных программ, интерфейсы и функции, объявленные в MAPIUTIL MAPI's. Файл заголовка **IPropData** и **ITableData** — необходимо вызвать **MAPIInitialize** для инициализации. Дополнительные сведения можно [IPropData: IMAPIProp](ipropdataimapiprop.md), [ITableData: IUnknown](itabledataiunknown.md)и [MAPIInitialize](mapiinitialize.md). Вместо этого вызовите функцию **ScInitMapiUtil** . Для получения дополнительных сведений см [ScInitMapiUtil](scinitmapiutil.md). **ScInitMapiUtil** позволяет клиентским приложениям использовать вспомогательные функции и методы, требующие выделения пространства MAPI, однако, не запрашивать их явным образом. 
  
Во время завершения вызова с **DeinitMapiUtil** для освобождения ресурсов, подключенных к служебных программ. Не вызывайте **MAPIUninitialize**. Для получения дополнительных сведений см [DeinitMapiUtil](deinitmapiutil.md) и [MAPIUninitialize](mapiuninitialize.md).
  
Обратите внимание, что интерфейс **ITableData** не поддерживает уведомления о таблице для клиентов, которые вызвали **ScInitMapiUtil** , а не **MAPIInitialize**. 
  

