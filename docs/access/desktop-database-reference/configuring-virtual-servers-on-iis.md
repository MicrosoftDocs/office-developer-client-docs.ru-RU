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
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="0eedb-102">Настройка виртуальных серверов в службах IIS</span><span class="sxs-lookup"><span data-stu-id="0eedb-102">Configuring Virtual Servers on IIS</span></span>


<span data-ttu-id="0eedb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0eedb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0eedb-104">При создании виртуальных серверов в Internet Information Services 4.0, необходимы две дополнительные шаги для настройки виртуального сервера для работы с помощью служб удаленных рабочих СТОЛОВ:</span><span class="sxs-lookup"><span data-stu-id="0eedb-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="0eedb-105">При настройке сервера, проверьте «Разрешить выполнение доступ».</span><span class="sxs-lookup"><span data-stu-id="0eedb-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="0eedb-106">Перемещение msadcs.dll *виртуального корня*\\службу, где *виртуального корня* — домашнего каталога виртуального сервера.</span><span class="sxs-lookup"><span data-stu-id="0eedb-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

