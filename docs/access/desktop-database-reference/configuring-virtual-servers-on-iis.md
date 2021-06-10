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
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="162f2-102">Настройка виртуальных серверов в IIS</span><span class="sxs-lookup"><span data-stu-id="162f2-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="162f2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="162f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="162f2-104">При создании виртуальных серверов в службы IIS 4.0 необходимы следующие два дополнительных шага, чтобы настроить виртуальный сервер для работы с RDS:</span><span class="sxs-lookup"><span data-stu-id="162f2-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="162f2-105">При настройке сервера проверьте "Разрешить выполнение доступа".</span><span class="sxs-lookup"><span data-stu-id="162f2-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="162f2-106">Переместите msadcs.dll *в vroot* \\ msadc, где *vroot* является домашним каталогом виртуального сервера.</span><span class="sxs-lookup"><span data-stu-id="162f2-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

