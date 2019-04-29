---
title: Обработка событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c989bc39c22f4e566c18feb4fdeaa8582c5525f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438269"
---
# <a name="handling-events"></a>Обработка событий

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Начиная с Excel 2010 XLL могут получать события, предназначенные для управления жизненным циклом асинхронной функции. Ниже приведены события.
  
- **Калкулатионендед**: вызывается после завершения вычисления Excel. После этого события можно освободить ресурсы, выделенные во время вычисления.
    
- **Калкулатионканцелед**: вызывается, когда пользователь прерывает вычисление. XLL остановить все асинхронные действия. Сразу после этого события вызывается событие **калкулатионендед** . 
    
Для обработки этих событий XLL использует функцию C API [кслевентрегистер](xleventregister.md). 
  
> [!NOTE]
> **Калкулатионендед** и **калкулатионканцелед** не вызываются во время программного пересчета. 
  

