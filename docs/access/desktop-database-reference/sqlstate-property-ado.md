---
title: Свойство SQLState (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb4a9adbc6060b7c33e128a0a3fca8c1eb7bc10d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308555"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="b1f82-102">Свойство SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="b1f82-102">SQLState property (ADO)</span></span>


<span data-ttu-id="b1f82-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1f82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1f82-104">Указывает состояние SQL для заданного объекта [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b1f82-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1f82-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1f82-105">Return value</span></span>

<span data-ttu-id="b1f82-106">Возвращает строковое значение  из пяти символов, которое следует стандарту ANSI SQL и указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1f82-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f82-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="b1f82-107">Remarks</span></span>

<span data-ttu-id="b1f82-108">Используйте свойство **SQLState,** чтобы прочитать код ошибки из пяти символов, возвращаемой поставщиком при ошибке во время обработки SQL оператора.</span><span class="sxs-lookup"><span data-stu-id="b1f82-108">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</span></span> <span data-ttu-id="b1f82-109">Например, при использовании поставщика Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server коды ошибок состояния SQL исходят из ODBC на основе ошибок, характерных для ODBC, или на ошибках, которые происходят из Microsoft SQL Server, а затем соедиируются с ошибками ODBC.</span><span class="sxs-lookup"><span data-stu-id="b1f82-109">For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</span></span> <span data-ttu-id="b1f82-110">Эти коды ошибок задокументированы в стандарте anSI SQL, но могут быть реализованы по-разному различными источниками данных.</span><span class="sxs-lookup"><span data-stu-id="b1f82-110">These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

