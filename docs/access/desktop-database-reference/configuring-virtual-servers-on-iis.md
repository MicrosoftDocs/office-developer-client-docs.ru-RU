---
title: Настройка виртуальных серверов в службах IIS
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7408e2dc10a5e47b298b77a9244477b16bca3ff1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879244"
---
# <a name="configuring-virtual-servers-on-iis"></a>Настройка виртуальных серверов в службах IIS


**Применимо к**: Access 2013, Office 2013

При создании виртуальных серверов в Internet Information Services 4.0, необходимы две дополнительные шаги для настройки виртуального сервера для работы с помощью служб удаленных рабочих СТОЛОВ:

1.  При настройке сервера, проверьте «Разрешить выполнение доступ».

2.  Перемещение msadcs.dll *виртуального корня*\\службу, где *виртуального корня* — домашнего каталога виртуального сервера.

