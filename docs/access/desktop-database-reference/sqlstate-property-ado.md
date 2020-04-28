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
# <a name="sqlstate-property-ado"></a><span data-ttu-id="0e119-102">Свойство SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="0e119-102">SQLState property (ADO)</span></span>


<span data-ttu-id="0e119-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e119-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e119-104">Указывает состояние SQL для данного объекта [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0e119-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="0e119-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e119-105">Return value</span></span>

<span data-ttu-id="0e119-106">Возвращает **строковое** значение из пяти символов, которое соответствует стандарту ANSI SQL и указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0e119-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e119-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e119-107">Remarks</span></span>

<span data-ttu-id="0e119-108">Используйте свойство **SQLSTATE** для считывания кода ошибки из пяти символов, который возвращает поставщик при возникновении ошибки во время обработки оператора SQL.</span><span class="sxs-lookup"><span data-stu-id="0e119-108">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</span></span> <span data-ttu-id="0e119-109">Например, при использовании поставщика Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server коды ошибок состояния SQL берутся из ODBC, на основе ошибок, относящихся к ODBC или об ошибках, происходящих из Microsoft SQL Server, а затем сопоставляются с ошибками ODBC.</span><span class="sxs-lookup"><span data-stu-id="0e119-109">For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</span></span> <span data-ttu-id="0e119-110">Эти коды ошибок задокументированы в стандарте ANSI SQL, но могут по-разному реализовываться различными источниками данных.</span><span class="sxs-lookup"><span data-stu-id="0e119-110">These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

