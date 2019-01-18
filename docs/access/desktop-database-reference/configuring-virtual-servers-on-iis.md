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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719318"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="f213f-102">Настройка виртуальных серверов в IIS</span><span class="sxs-lookup"><span data-stu-id="f213f-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="f213f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f213f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f213f-104">При создании виртуальных серверов в Internet Information Services 4.0, необходимы две дополнительные шаги для настройки виртуального сервера для работы с помощью служб удаленных рабочих СТОЛОВ:</span><span class="sxs-lookup"><span data-stu-id="f213f-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="f213f-105">При настройке сервера, проверьте «Разрешить выполнение доступ».</span><span class="sxs-lookup"><span data-stu-id="f213f-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="f213f-106">Перемещение msadcs.dll *виртуального корня*\\службу, где *виртуального корня* — домашнего каталога виртуального сервера.</span><span class="sxs-lookup"><span data-stu-id="f213f-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

