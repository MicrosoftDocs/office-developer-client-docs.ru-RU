---
title: 'Internet Server Error: Access Denied'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db78b6f2c51e2e5df918622043e33abc6bc9e674
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481012"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="d5f1a-102">Internet Server Error: Access Denied</span><span class="sxs-lookup"><span data-stu-id="d5f1a-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="d5f1a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5f1a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d5f1a-104">Если возникнет ошибка, это обычно означает, что Microsoft Internet Information Services (IIS) возвращаются следующие состояния:</span><span class="sxs-lookup"><span data-stu-id="d5f1a-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="d5f1a-105">HTTP\_состояние\_ЗАПРЕЩЕННЫЕ 401</span><span class="sxs-lookup"><span data-stu-id="d5f1a-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="d5f1a-106">Убедитесь в том, что каталоги, к которым получают доступ служб IIS, имеют соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="d5f1a-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="d5f1a-107">Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервер IIS под управлением в одном из трех режимов проверки подлинности пароля: анонимный доступ, Basic или NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="d5f1a-107">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="d5f1a-108">Кроме того веб-сервера должны быть разрешения на компьютере источника данных Если это компьютер с Windows NT и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d5f1a-108">Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

