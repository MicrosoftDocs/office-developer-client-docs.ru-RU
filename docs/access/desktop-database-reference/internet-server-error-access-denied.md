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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720389"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="31e83-102">Ошибка интернет-сервера: "Отказано в доступе"</span><span class="sxs-lookup"><span data-stu-id="31e83-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="31e83-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31e83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31e83-104">Если возникнет ошибка, это обычно означает, что Microsoft Internet Information Services (IIS) возвращаются следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="31e83-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="31e83-105">HTTP\_состояние\_ЗАПРЕЩЕННЫЕ 401</span><span class="sxs-lookup"><span data-stu-id="31e83-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="31e83-106">Убедитесь в том, что каталоги, к которым получают доступ служб IIS, имеют соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="31e83-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="31e83-107">Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервере IIS, выполняющегося в любой из трех режимов проверки подлинности пароля: анонимный доступ, Basic или NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="31e83-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="31e83-108">Кроме того веб-сервера должны быть разрешения на компьютере источника данных Если это компьютер с Windows NT и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="31e83-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

