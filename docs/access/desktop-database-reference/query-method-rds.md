---
title: Метод Query (RDS - ссылки для настольных баз данных Access)
TOCTitle: Query Method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70f4a1c7a16a97710ef2b0c04bbc0a3924864231
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876031"
---
# <a name="query-method-rds"></a><span data-ttu-id="3852c-102">Метод Query (RDS)</span><span class="sxs-lookup"><span data-stu-id="3852c-102">Query Method (RDS)</span></span>


<span data-ttu-id="3852c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3852c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3852c-104">Допустимая строка запроса SQL используется для возврата [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3852c-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3852c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3852c-105">Syntax</span></span>

<span data-ttu-id="3852c-106">Установка*набора записей* = *DataFactory*. Запрос (*подключения*, *запросов*)</span><span class="sxs-lookup"><span data-stu-id="3852c-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="3852c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3852c-107">Parameters</span></span>

  - <span data-ttu-id="3852c-108">*Набор записей*</span><span class="sxs-lookup"><span data-stu-id="3852c-108">*Recordset*</span></span>

  - <span data-ttu-id="3852c-109">Объектная переменная, представляющий объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3852c-109">An object variable that represents a **Recordset** object.</span></span>

  - <span data-ttu-id="3852c-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="3852c-110">*DataFactory*</span></span>

  - <span data-ttu-id="3852c-111">Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="3852c-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>

  - <span data-ttu-id="3852c-112">*Подключение*</span><span class="sxs-lookup"><span data-stu-id="3852c-112">*Connection*</span></span>

  - <span data-ttu-id="3852c-113">**Строковое** значение, содержащее сведения о подключении сервера.</span><span class="sxs-lookup"><span data-stu-id="3852c-113">A **String** value that contains the server connection information.</span></span> <span data-ttu-id="3852c-114">Это свойства [подключения](connect-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="3852c-114">This is similar to the [Connect](connect-property-rds.md) property.</span></span>

  - <span data-ttu-id="3852c-115">*Query*</span><span class="sxs-lookup"><span data-stu-id="3852c-115">*Query*</span></span>

  - <span data-ttu-id="3852c-116">**Строка** , содержащая запрос SQL.</span><span class="sxs-lookup"><span data-stu-id="3852c-116">A **String** that contains the SQL query.</span></span>

## <a name="remarks"></a><span data-ttu-id="3852c-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="3852c-117">Remarks</span></span>

<span data-ttu-id="3852c-118">Запрос следует использовать диалект SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="3852c-118">The query should use the SQL dialect of the database server.</span></span> <span data-ttu-id="3852c-119">Если возникает ошибка при выполнении запроса, был выполнен возвращается состояние результатов.</span><span class="sxs-lookup"><span data-stu-id="3852c-119">A result status is returned if there is an error with the query that was executed.</span></span> <span data-ttu-id="3852c-120">Метод **Query** не выполняет проверку строки **запроса** синтаксис.</span><span class="sxs-lookup"><span data-stu-id="3852c-120">The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

