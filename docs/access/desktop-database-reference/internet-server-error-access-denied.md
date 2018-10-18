---
title: 'Internet Server Error: Access Denied'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c874b7a2c4facb9f5969bf9a2150c86773a2687a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603345"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="9228d-102">Internet Server Error: Access Denied</span><span class="sxs-lookup"><span data-stu-id="9228d-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="9228d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9228d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9228d-104">Если возникнет ошибка, это обычно означает, что Microsoft Internet Information Services (IIS) возвращаются следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="9228d-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="9228d-105">HTTP\_состояние\_ЗАПРЕЩЕННЫЕ 401</span><span class="sxs-lookup"><span data-stu-id="9228d-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="9228d-106"><<<<<<< HEAD убедитесь, что каталоги, к которым получают доступ IIS имеют соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="9228d-106"><<<<<<< HEAD Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="9228d-107">Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервер IIS под управлением в одном из трех режимов проверки подлинности пароля: анонимный доступ, Basic или NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="9228d-107">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="9228d-108">Кроме того веб-сервера должны быть разрешения на компьютере источника данных Если это компьютер с Windows NT и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9228d-108">Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
<span data-ttu-id="9228d-109">=== Убедитесь, что каталоги, к которым получают доступ IIS имеют соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="9228d-109">======= Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="9228d-110">Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервере IIS, выполняющегося в любой из трех режимов проверки подлинности пароля: анонимный доступ, Basic или NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="9228d-110">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="9228d-111">Кроме того веб-сервера должны быть разрешения на компьютере источника данных Если это компьютер с Windows NT и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9228d-111">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
>>>>>>> <span data-ttu-id="9228d-112">master</span><span class="sxs-lookup"><span data-stu-id="9228d-112">master</span></span>

