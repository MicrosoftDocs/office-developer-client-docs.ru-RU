---
title: Connection.QueryTimeout Property (DAO)
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
ms.openlocfilehash: 8f5ce9faa1ebd56bdc8e4de5aeea417835c950b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878810"
---
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="39ef6-102">Connection.QueryTimeout Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="39ef6-102">Connection.QueryTimeout Property (DAO)</span></span>


<span data-ttu-id="39ef6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39ef6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39ef6-104">Задает или возвращает значение, указывающее количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса на источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="39ef6-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ef6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39ef6-105">Syntax</span></span>

<span data-ttu-id="39ef6-106">*выражение* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="39ef6-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="39ef6-107">*выражение* Переменная, которая содержит объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="39ef6-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="39ef6-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="39ef6-108">Remarks</span></span>

<span data-ttu-id="39ef6-109">Значение по умолчанию — 60.</span><span class="sxs-lookup"><span data-stu-id="39ef6-109">The default value is 60.</span></span>

<span data-ttu-id="39ef6-110">При использовании базы данных ODBC, например Microsoft SQL Server, могут возникнуть задержки из-за сетевой трафик или высокая интенсивность операций использования ODBC сервера.</span><span class="sxs-lookup"><span data-stu-id="39ef6-110">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server.</span></span> <span data-ttu-id="39ef6-111">Вместо ожидания, можно указать время ожидания.</span><span class="sxs-lookup"><span data-stu-id="39ef6-111">Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="39ef6-112">При использовании **QueryTimeout** с объектом **[подключения](connection-object-dao.md)** или **[базы данных](database-object-dao.md)** , задает глобальное значение для всех запросов, связанной с базой данных.</span><span class="sxs-lookup"><span data-stu-id="39ef6-112">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database.</span></span> <span data-ttu-id="39ef6-113">Можно переопределить это значение для конкретного запроса, задав свойство **время ожидания ODBC** определенного объекта **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="39ef6-113">You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

