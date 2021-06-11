---
title: Excel Функции соединитетеля кластера
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408588"
---
# <a name="excel-cluster-connector-functions"></a>Excel Функции соединитетеля кластера

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 кластерных соединителов DLLs должны реализовать функции, описанные в этом разделе.
  
Возвращаемые значения, указанные в справочных разделах в этом разделе, определяются в SDK, включая файл xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Архитектура соединитеного кластера

Excel точки входа в соединители кластера для передачи вызовов функций, определенных пользователем, в высокоскоростной вычислительный кластер и для управления кластерными сеансами.
  
## <a name="in-this-section"></a>В этом разделе

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>См. также



[Разработка соединителей кластеров Excel](developing-excel-cluster-connectors.md)
  
[Функции защиты кластеров](cluster-safe-functions.md)

