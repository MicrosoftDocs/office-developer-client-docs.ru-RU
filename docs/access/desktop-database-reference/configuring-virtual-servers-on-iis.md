---
title: Настройка виртуальных серверов в IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8ab3bf8e6ffec2b72744d3abacceb4725c98b02
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946729"
---
# <a name="configuring-virtual-servers-on-iis"></a>Настройка виртуальных серверов в IIS

**Применимо к**: Access 2013, Office 2013

При создании виртуальных серверов в Internet Information Services 4.0, необходимы две дополнительные шаги для настройки виртуального сервера для работы с помощью служб удаленных рабочих СТОЛОВ:

1.  При настройке сервера, проверьте «Разрешить выполнение доступ».

2.  Перемещение msadcs.dll *виртуального корня*\\службу, где *виртуального корня* — домашнего каталога виртуального сервера.

