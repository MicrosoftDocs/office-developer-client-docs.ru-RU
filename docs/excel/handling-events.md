---
title: Обработка событий
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b67fcb83-a0e2-4349-88f5-bcc181306eac
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c5508df8466932b6fb5c7e04164aa00a5ea31a8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807254"
---
# <a name="handling-events"></a>Обработка событий

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Начиная с версии Excel 2010, XLL-модулей может получать события, предназначенное для управления жизненным циклом асинхронные функции. События, как показано ниже:
  
- **CalculationEnded**: возникает, когда завершения вычисления. После этого события можно освободить ресурсы, выделенные в процессе вычисления.
    
- **CalculationCanceled**: возникает, когда пользователь прерывает вычисления. XLL останавливает любые асинхронной операции. Сразу после этого события **CalculationEnded** событие. 
    
Обрабатывать следующие события, XLL использует функции интерфейса API для C [xlEventRegister](xleventregister.md). 
  
> [!NOTE]
> **CalculationEnded** и **CalculationCanceled** не возникает во время программный пересчета. 
  

