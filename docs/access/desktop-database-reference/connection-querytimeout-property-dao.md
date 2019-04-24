---
title: Свойство Connection. QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295823"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="e8e8b-102">Свойство Connection. QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8e8b-102">Connection.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="e8e8b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8e8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8e8b-104">Задает или возвращает значение, задающее время ожидания в секундах до возникновения ошибки времени ожидания при выполнении запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="e8e8b-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8e8b-105">Syntax</span></span>

<span data-ttu-id="e8e8b-106">*Expression* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="e8e8b-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="e8e8b-107">*Expression (выражение* ) Переменная, представляющая объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="e8e8b-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8e8b-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="e8e8b-108">Remarks</span></span>

<span data-ttu-id="e8e8b-109">Значение по умолчанию  60.</span><span class="sxs-lookup"><span data-stu-id="e8e8b-109">The default value is 60.</span></span>

<span data-ttu-id="e8e8b-110">При использовании базы данных ODBC, такой как Microsoft SQL Server, могут возникать задержки из-за сетевого трафика или интенсивного использования сервера ODBC.</span><span class="sxs-lookup"><span data-stu-id="e8e8b-110">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server.</span></span> <span data-ttu-id="e8e8b-111">Вместо неопределенного периода ожидания можно указать время ожидания.</span><span class="sxs-lookup"><span data-stu-id="e8e8b-111">Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="e8e8b-112">При использовании **QueryTimeOut** с подключением **[](connection-object-dao.md)** или объектом **[базы данных](database-object-dao.md)** он задает глобальное значение для всех запросов, связанных с базой данных.</span><span class="sxs-lookup"><span data-stu-id="e8e8b-112">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database.</span></span> <span data-ttu-id="e8e8b-113">Вы можете переопределить это значение для определенного запроса, задав свойство **ODBCTimeout** для определенного объекта **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="e8e8b-113">You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

