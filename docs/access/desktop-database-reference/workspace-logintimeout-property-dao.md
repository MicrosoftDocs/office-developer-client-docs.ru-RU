---
title: Свойство Workspace.LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbc0ed4849e8c22bc7023bd4254fdee74a5d016c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699613"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="2f78a-102">Свойство Workspace.LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f78a-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="2f78a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f78a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f78a-104">Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="2f78a-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f78a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f78a-105">Syntax</span></span>

<span data-ttu-id="2f78a-106">*выражение* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="2f78a-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="2f78a-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="2f78a-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f78a-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f78a-108">Remarks</span></span>

<span data-ttu-id="2f78a-109">Свойство **LoginTimeout** по умолчанию установлено 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="2f78a-109">The default **LoginTimeout** property setting is 20 seconds.</span></span> <span data-ttu-id="2f78a-110">Если свойство **LoginTimeout** имеет значение 0, происходит нет времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="2f78a-110">When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="2f78a-111">Когда вы при входе в систему в базе данных ODBC, например Microsoft SQL Server может возникнуть сбой подключения из-за ошибки сети, или сервер не будет запущен.</span><span class="sxs-lookup"><span data-stu-id="2f78a-111">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running.</span></span> <span data-ttu-id="2f78a-112">Без необходимости по умолчанию 20 секунд для подключения, можно указать время до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="2f78a-112">Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error.</span></span> <span data-ttu-id="2f78a-113">Вход в систему на сервере происходит неявно, как часть из нескольких разных события, такие как выполнение запроса базы данных внешнего сервера.</span><span class="sxs-lookup"><span data-stu-id="2f78a-113">Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

