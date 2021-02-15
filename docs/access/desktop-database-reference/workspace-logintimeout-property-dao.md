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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306911"
---
# <a name="workspacelogintimeout-property-dao"></a><span data-ttu-id="071df-102">Свойство Workspace.LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="071df-102">Workspace.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="071df-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="071df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="071df-104">Задает или возвращает количество секунд до возникновения ошибки при попытке входа в базу данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="071df-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="071df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="071df-105">Syntax</span></span>

<span data-ttu-id="071df-106">*выражение .* LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="071df-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="071df-107">*expression*: переменная, представляющая объект **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="071df-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="071df-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="071df-108">Remarks</span></span>

<span data-ttu-id="071df-109">Значение свойства **LoginTimeout по** умолчанию — 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="071df-109">The default **LoginTimeout** property setting is 20 seconds.</span></span> <span data-ttu-id="071df-110">Если для **свойства LoginTimeout** установлено 0, время не происходит.</span><span class="sxs-lookup"><span data-stu-id="071df-110">When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="071df-111">При попытке входа в базу данных ODBC, например Microsoft SQL Server, подключение может быть сбой в результате сетевых ошибок или из-за того, что сервер не работает.</span><span class="sxs-lookup"><span data-stu-id="071df-111">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running.</span></span> <span data-ttu-id="071df-112">Вместо того чтобы ждать подключения по умолчанию в течение 20 секунд, можно указать время ожидания перед тем, как будет выявить ошибку.</span><span class="sxs-lookup"><span data-stu-id="071df-112">Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error.</span></span> <span data-ttu-id="071df-113">Вход на сервер происходит неявно в рамках ряда различных событий, таких как запуск запроса во внешней базе данных серверов.</span><span class="sxs-lookup"><span data-stu-id="071df-113">Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

