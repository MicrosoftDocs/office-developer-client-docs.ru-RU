---
title: Метод запроса (RDS — справочник по базе данных Access для настольных ПК)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301115"
---
# <a name="query-method-rds"></a><span data-ttu-id="3792e-102">Метод запроса (RDS)</span><span class="sxs-lookup"><span data-stu-id="3792e-102">Query method (RDS)</span></span>

<span data-ttu-id="3792e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3792e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3792e-104">Возвращает набор записей с помощью SQL строки [запроса.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3792e-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3792e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3792e-105">Syntax</span></span>

<span data-ttu-id="3792e-106">Set *Recordset*  =  *DataFactory*. Query(*Connection*, *Query*)</span><span class="sxs-lookup"><span data-stu-id="3792e-106">Set *Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="3792e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3792e-107">Parameters</span></span>

|<span data-ttu-id="3792e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="3792e-108">Parameter</span></span>|<span data-ttu-id="3792e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3792e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3792e-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="3792e-110">*Recordset*</span></span> |<span data-ttu-id="3792e-111">Объектная переменная, представляюная объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="3792e-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="3792e-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="3792e-112">*DataFactory*</span></span> |<span data-ttu-id="3792e-113">Объектная переменная, представляюная [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md)</span><span class="sxs-lookup"><span data-stu-id="3792e-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="3792e-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="3792e-114">*Connection*</span></span> |<span data-ttu-id="3792e-115">**Строка,** содержаная сведения о под подключением к серверу.</span><span class="sxs-lookup"><span data-stu-id="3792e-115">A **String** value that contains the server connection information.</span></span> <span data-ttu-id="3792e-116">Это свойство аналогично свойству [Connect.](connect-property-rds.md)</span><span class="sxs-lookup"><span data-stu-id="3792e-116">This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="3792e-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="3792e-117">*Query*</span></span> |<span data-ttu-id="3792e-118">**Строка,** содержаная SQL запроса.</span><span class="sxs-lookup"><span data-stu-id="3792e-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3792e-119">Заметки</span><span class="sxs-lookup"><span data-stu-id="3792e-119">Remarks</span></span>

<span data-ttu-id="3792e-120">В запросе должен SQL диалект сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="3792e-120">The query should use the SQL dialect of the database server.</span></span> <span data-ttu-id="3792e-121">Если при выполнении запроса произошла ошибка, возвращается состояние результата.</span><span class="sxs-lookup"><span data-stu-id="3792e-121">A result status is returned if there is an error with the query that was executed.</span></span> <span data-ttu-id="3792e-122">Метод **Query** не выполняет проверку синтаксиса в **строке запроса.**</span><span class="sxs-lookup"><span data-stu-id="3792e-122">The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

