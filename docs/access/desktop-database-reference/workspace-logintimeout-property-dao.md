---
title: Свойство Workspace.LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 5f03b166-abbc-20de-1a01-3869a9f2907d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194743(v=office.15)
ms:contentKeyID: 48545151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07b2945f2e9a59cc8a7db4a6f5a44cfaf9b35043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928287"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="e056a-102">Свойство Workspace.LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="e056a-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="e056a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e056a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e056a-104">Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="e056a-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e056a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e056a-105">Syntax</span></span>

<span data-ttu-id="e056a-106">*выражение* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="e056a-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="e056a-107">*выражение* Переменная, которая представляет собой объект- **рабочей области** .</span><span class="sxs-lookup"><span data-stu-id="e056a-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e056a-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e056a-108">Remarks</span></span>

<span data-ttu-id="e056a-109">Свойство **LoginTimeout** по умолчанию установлено 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="e056a-109">The default **LoginTimeout** property setting is 20 seconds.</span></span> <span data-ttu-id="e056a-110">Если свойство **LoginTimeout** имеет значение 0, происходит нет времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="e056a-110">When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="e056a-111">Когда вы при входе в систему в базе данных ODBC, например Microsoft SQL Server может возникнуть сбой подключения из-за ошибки сети, или сервер не будет запущен.</span><span class="sxs-lookup"><span data-stu-id="e056a-111">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running.</span></span> <span data-ttu-id="e056a-112">Без необходимости по умолчанию 20 секунд для подключения, можно указать время до возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="e056a-112">Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error.</span></span> <span data-ttu-id="e056a-113">Вход в систему на сервере происходит неявно, как часть из нескольких разных события, такие как выполнение запроса базы данных внешнего сервера.</span><span class="sxs-lookup"><span data-stu-id="e056a-113">Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

