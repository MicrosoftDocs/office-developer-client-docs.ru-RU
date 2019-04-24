---
title: 'Ошибка интернет-сервера: "Отказано в доступе"'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291257"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="945a2-102">Ошибка интернет-сервера: "Отказано в доступе"</span><span class="sxs-lookup"><span data-stu-id="945a2-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="945a2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="945a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="945a2-104">Если возникнет эта ошибка, обычно это означает, что службы Microsoft IIS возвратили следующее состояние:</span><span class="sxs-lookup"><span data-stu-id="945a2-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="945a2-105">HTTP\_-\_состояние отклонено 401</span><span class="sxs-lookup"><span data-stu-id="945a2-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="945a2-106">Убедитесь, что в каталогах, к которым у IIS есть соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="945a2-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="945a2-107">RDS может связываться с веб-сервером IIS, работающим в одном из трех режимов проверки поДлинности паролей: anonymous, Basic или NT Challenge/Response (встроенная проверка подлинности Windows в Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="945a2-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="945a2-108">Кроме того, у веб-сервера должны быть разрешения на доступ к компьютеру источника данных, если это компьютер с Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="945a2-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

