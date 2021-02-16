---
title: Функции соединители кластера Excel
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
# <a name="excel-cluster-connector-functions"></a>Функции соединители кластера Excel

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
DLL соединителя кластера Microsoft Excel 2013 должны реализовывать функции, описанные в этом разделе.
  
Возвращаемая величина, упомянутая в справочных разделах в этом разделе, определена в SDK include file, xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Архитектура соединители кластера

Excel вызывает точки входа в соединитель кластера для передачи вызовов пользовательских функций в высокоскоростной вычислительный кластер и для управления сеансами кластера.
  
## <a name="in-this-section"></a>В этом разделе:

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>См. также



[Разработка соединителей кластеров Excel](developing-excel-cluster-connectors.md)
  
[Функции защиты кластеров](cluster-safe-functions.md)

