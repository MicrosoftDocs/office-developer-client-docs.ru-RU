---
title: Настройка виртуальных серверов в IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9c7f5782885aafd43e365ddc4f08dedd0975234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295977"
---
# <a name="configuring-virtual-servers-on-iis"></a>Настройка виртуальных серверов в IIS

**Область применения**: Access 2013, Office 2013

При создании виртуальных серверов в службах IIS 4,0 необходимо выполнить следующие два действия, чтобы настроить виртуальный сервер для работы с RDS:

1.  При настройке сервера установите флажок "разрешить выполнение доступа".

2.  Переместите мсадкс. dll в *VRoot*\\MSADC, где *VRoot* — это домашний каталог виртуального сервера.

