---
title: Функции для работы с соединителями кластеров Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807177"
---
# <a name="excel-cluster-connector-functions"></a>Функции для работы с соединителями кластеров Excel

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Соединитель кластера Microsoft Excel 2013 библиотеки DLL необходимо реализовать функции, описанные в этом разделе.
  
Возвращаемые значения, упомянутые в ссылки в этом разделе определяются в пакете SDK включают файл, xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Архитектура соединителя кластера

Excel вызывает точки входа в соединитель кластера передача пользовательской функции вызова к высокой производительности вычислительному кластеру, а также для управления сеансами кластера.
  
## <a name="in-this-section"></a>В этой статье

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>См. также



[Разработка соединителей кластеров Excel](developing-excel-cluster-connectors.md)
  
[Функции защиты кластеров](cluster-safe-functions.md)

