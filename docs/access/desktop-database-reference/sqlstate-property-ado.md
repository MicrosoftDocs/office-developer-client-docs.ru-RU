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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716301"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="766ce-102">Свойство SQLState (ADO)</span><span class="sxs-lookup"><span data-stu-id="766ce-102">SQLState property (ADO)</span></span>


<span data-ttu-id="766ce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="766ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="766ce-104">Указывает состояние SQL для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="766ce-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="766ce-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="766ce-105">Return value</span></span>

<span data-ttu-id="766ce-106">Возвращает **строковое** значение пяти символов, которая стандарту ANSI SQL и указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="766ce-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="766ce-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="766ce-107">Remarks</span></span>

<span data-ttu-id="766ce-108">Используйте свойство **SQLState** читать код ошибки пяти знаков, поставщик возвращает при возникновении ошибки во время обработки инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="766ce-108">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</span></span> <span data-ttu-id="766ce-109">Например при использовании поставщик Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server, коды ошибок состояний SQL берутся из ODBC, основанные на ошибки, относящиеся к ODBC или на ошибки, которые создаются из Microsoft SQL Server, а затем сопоставляются с ODBC ошибки.</span><span class="sxs-lookup"><span data-stu-id="766ce-109">For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</span></span> <span data-ttu-id="766ce-110">Эти коды ошибок описаны в стандарте ANSI SQL, но может быть по-разному реализован различных источников данных.</span><span class="sxs-lookup"><span data-stu-id="766ce-110">These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

