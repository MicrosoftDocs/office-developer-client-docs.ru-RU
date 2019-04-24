---
title: Метод query (Справочник по базам данных для рабочих столов RDS)
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
# <a name="query-method-rds"></a><span data-ttu-id="d8aa3-102">Метод query (RDS)</span><span class="sxs-lookup"><span data-stu-id="d8aa3-102">Query method (RDS)</span></span>

<span data-ttu-id="d8aa3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8aa3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8aa3-104">Для возврата объекта [Recordset](recordset-object-ado.md)используется допустимая строка запроса SQL.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8aa3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8aa3-105">Syntax</span></span>

<span data-ttu-id="d8aa3-106">Задание объекта Recordset для объекта*Recordset* = \**. Запрос (*Подключение\*, *запрос*)</span><span class="sxs-lookup"><span data-stu-id="d8aa3-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="d8aa3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8aa3-107">Parameters</span></span>

|<span data-ttu-id="d8aa3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d8aa3-108">Parameter</span></span>|<span data-ttu-id="d8aa3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8aa3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d8aa3-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="d8aa3-110">*Recordset*</span></span> |<span data-ttu-id="d8aa3-111">Объектная переменная, представляющая объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d8aa3-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="d8aa3-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="d8aa3-112">*DataFactory*</span></span> |<span data-ttu-id="d8aa3-113">Объектная переменная, представляющая объект [фактОв рдссервер.](datafactory-object-rdsserver.md) DataObject.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="d8aa3-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="d8aa3-114">*Connection*</span></span> |<span data-ttu-id="d8aa3-115">**Строковое** значение, содержащее сведения о подключении к серверу.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-115">A **String** value that contains the server connection information.</span></span> <span data-ttu-id="d8aa3-116">Оно аналогично свойству [Connect](connect-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="d8aa3-116">This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="d8aa3-117">*Query*</span><span class="sxs-lookup"><span data-stu-id="d8aa3-117">*Query*</span></span> |<span data-ttu-id="d8aa3-118">**Строка** , содержащая запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d8aa3-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8aa3-119">Remarks</span></span>

<span data-ttu-id="d8aa3-120">В запросе должен использоваться диалект SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-120">The query should use the SQL dialect of the database server.</span></span> <span data-ttu-id="d8aa3-121">Состояние результата возвращается при наличии ошибки в выполненном запросе.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-121">A result status is returned if there is an error with the query that was executed.</span></span> <span data-ttu-id="d8aa3-122">Метод **Query** не выполняет проверку синтаксиса в строке **запроса** .</span><span class="sxs-lookup"><span data-stu-id="d8aa3-122">The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

