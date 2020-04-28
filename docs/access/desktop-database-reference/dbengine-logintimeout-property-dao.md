---
title: Свойство DBEngine. LoginTimeout (DAO)
TOCTitle: LoginTimeout Property
ms:assetid: 81d14153-79c5-7860-b6a8-4079d2d7acf7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196648(v=office.15)
ms:contentKeyID: 48545964
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052923
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e3ff893a16e650fe7eb49b647ae8d67374375a0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294311"
---
# <a name="dbenginelogintimeout-property-dao"></a><span data-ttu-id="716c2-102">Свойство DBEngine. LoginTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="716c2-102">DBEngine.LoginTimeout property (DAO)</span></span>


<span data-ttu-id="716c2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="716c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="716c2-104">Задает или возвращает число секунд до возникновения ошибки при попытке входа в базу данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="716c2-104">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span>

## <a name="syntax"></a><span data-ttu-id="716c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="716c2-105">Syntax</span></span>

<span data-ttu-id="716c2-106">*Expression* . LoginTimeout</span><span class="sxs-lookup"><span data-stu-id="716c2-106">*expression* .LoginTimeout</span></span>

<span data-ttu-id="716c2-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="716c2-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="716c2-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="716c2-108">Remarks</span></span>

<span data-ttu-id="716c2-109">Значение свойства **LoginTimeOut** по умолчанию — 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="716c2-109">The default **LoginTimeout** property setting is 20 seconds.</span></span> <span data-ttu-id="716c2-110">Если для свойства **LoginTimeOut** задано значение 0, время ожидания не возникает.</span><span class="sxs-lookup"><span data-stu-id="716c2-110">When the **LoginTimeout** property is set to 0, no timeout occurs.</span></span>

<span data-ttu-id="716c2-111">При попытке войти в базу данных ODBC, например Microsoft SQL Server, подключение может завершиться неудачей из-за ошибок сети или из-за того, что сервер не запущен.</span><span class="sxs-lookup"><span data-stu-id="716c2-111">When you're attempting to log on to an ODBC database, such as Microsoft SQL Server, the connection can fail as a result of network errors or because the server isn't running.</span></span> <span data-ttu-id="716c2-112">Вместо того чтобы ждать подключения по умолчанию (20 секунд), можно указать время ожидания перед возникновением ошибки.</span><span class="sxs-lookup"><span data-stu-id="716c2-112">Rather than waiting for the default 20 seconds to connect, you can specify how long to wait before raising an error.</span></span> <span data-ttu-id="716c2-113">Вход на сервер неявно происходит в рамках ряда различных событий, например при выполнении запроса к базе данных внешнего сервера.</span><span class="sxs-lookup"><span data-stu-id="716c2-113">Logging on to the server happens implicitly as part of a number of different events, such as running a query on an external server database.</span></span>

