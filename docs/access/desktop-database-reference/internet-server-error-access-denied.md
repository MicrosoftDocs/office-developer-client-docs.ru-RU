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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="18476-102">Ошибка интернет-сервера: "Отказано в доступе"</span><span class="sxs-lookup"><span data-stu-id="18476-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="18476-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18476-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18476-104">Если вы получите эту ошибку, обычно это означает, что Microsoft IIS (IIS) вернул следующее состояние:</span><span class="sxs-lookup"><span data-stu-id="18476-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="18476-105">HTTP \_ STATUS \_ DENIED 401</span><span class="sxs-lookup"><span data-stu-id="18476-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="18476-106">Убедитесь, что каталоги, к которые имеют доступ IIS, имеют соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="18476-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="18476-107">Службы RDS могут взаимодействовать с веб-сервером IIS, работающим в любом из трех режимов проверки подлинности паролем: анонимном, базовом или NT Challenge/Response (называемом встроенной проверкой подлинности Windows в Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="18476-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="18476-108">Кроме того, веб-сервер должен иметь разрешения на доступ к компьютеру источника данных, если это компьютер Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="18476-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

