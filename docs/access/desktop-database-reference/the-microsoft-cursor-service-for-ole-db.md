---
title: The Microsoft Cursor Service for OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9db5617eecff862ad941a4160c4b92bfa09d4c2d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885922"
---
# <a name="the-microsoft-cursor-service-for-ole-db"></a>The Microsoft Cursor Service for OLE DB


**Применимо к**: Access 2013, Office 2013

При установке курсора со стороны клиента, или задайте для свойства **CursorLocation** значение **adUseClient**, вызовах службы Microsoft курсора для OLE DB. Можно также увидеть ссылки «Клиента курсора обработчик», который является по сути то же самое в контексте ADO. Эта служба используется в качестве дополнения функции поддержки курсора поставщиков данных. В результате воспринимает относительно универсальный код функции из всех поставщиков данных.

Служба курсора для OLE DB делает доступными динамические свойства и улучшающий поведение некоторых методов. К примеру динамическое свойство **оптимизировать** позволяет создавать временных индексов для облегчения определенные операции, такие как метод **поиска** .

Служба курсора обеспечивает поддержку для пакетного обновления во всех случаях. Также более производительные курсора типов, таких как динамические курсоры моделирует, когда поставщик данных может поддерживать только менее производительные курсоры, такие как статические курсоры.

