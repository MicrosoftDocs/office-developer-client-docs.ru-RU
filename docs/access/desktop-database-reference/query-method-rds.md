---
title: Метод Query (RDS - ссылки для настольных баз данных Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717358"
---
# <a name="query-method-rds"></a><span data-ttu-id="8ebdd-102">Метод Query (RDS)</span><span class="sxs-lookup"><span data-stu-id="8ebdd-102">Query method (RDS)</span></span>

<span data-ttu-id="8ebdd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ebdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ebdd-104">Допустимая строка запроса SQL используется для возврата [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8ebdd-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ebdd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ebdd-105">Syntax</span></span>

<span data-ttu-id="8ebdd-106">Установка*набора записей* = *DataFactory*. Запрос (*подключения*, *запросов*)</span><span class="sxs-lookup"><span data-stu-id="8ebdd-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="8ebdd-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8ebdd-107">Parameters</span></span>

|<span data-ttu-id="8ebdd-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="8ebdd-108">Parameter</span></span>|<span data-ttu-id="8ebdd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8ebdd-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8ebdd-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="8ebdd-110">*Recordset*</span></span> |<span data-ttu-id="8ebdd-111">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8ebdd-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="8ebdd-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="8ebdd-112">*DataFactory*</span></span> |<span data-ttu-id="8ebdd-113">Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebdd-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="8ebdd-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="8ebdd-114">*Connection*</span></span> |<span data-ttu-id="8ebdd-115">**Строковое** значение, содержащее сведения о подключении сервера.</span><span class="sxs-lookup"><span data-stu-id="8ebdd-115">A **String** value that contains the server connection information.</span></span> <span data-ttu-id="8ebdd-116">Это свойства [подключения](connect-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebdd-116">This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="8ebdd-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="8ebdd-117">*Query*</span></span> |<span data-ttu-id="8ebdd-118">**Строка** , содержащая запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="8ebdd-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8ebdd-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="8ebdd-119">Remarks</span></span>

<span data-ttu-id="8ebdd-120">Запрос следует использовать диалект SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="8ebdd-120">The query should use the SQL dialect of the database server.</span></span> <span data-ttu-id="8ebdd-121">Если возникает ошибка при выполнении запроса, был выполнен возвращается состояние результатов.</span><span class="sxs-lookup"><span data-stu-id="8ebdd-121">A result status is returned if there is an error with the query that was executed.</span></span> <span data-ttu-id="8ebdd-122">Метод **Query** не выполняет проверку строки **запроса** синтаксис.</span><span class="sxs-lookup"><span data-stu-id="8ebdd-122">The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

