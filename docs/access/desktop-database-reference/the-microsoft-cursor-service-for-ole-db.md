---
title: The Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314359"
---
# <a name="microsoft-cursor-service-for-ole-db"></a>Служба курсора (Майкрософт) для OLE DB


**Область применения**: Access 2013, Office 2013

Когда вы выбираете курсор на стороне клиента или задайте свойство **CursorLocation** **adUseClient,** вы приводите ссылку на службу Microsoft Cursor для OLE DB. Вы также можете увидеть ссылки на "Двигатель курсора клиента", который по сути является одним и тем же в контексте ADO. Эта служба дополняет функции поддержки курсора поставщиками данных. В результате вы можете воспринимать относительно однородные функции всех поставщиков данных.

Служба cursor для OLE DB делает динамические свойства доступными и улучшает поведение определенных методов. Например, **динамическое** свойство Оптимизируйте позволяет создавать временные индексы для облегчения определенных операций, например метода **Find.**

Служба Cursor во всех случаях поддерживает пакетное обновление. Он также имитирует более способные типы курсоров, например динамические курсоры, когда поставщик данных может поставлять только менее способные курсоры, например статические курсоры.

