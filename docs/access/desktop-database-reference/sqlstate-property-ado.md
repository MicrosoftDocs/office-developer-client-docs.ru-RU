---
title: SQLState Property (ADO)
TOCTitle: SQLState Property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aead95e4276d61d69ae6ba5a86974cbe630f9043
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481428"
---
# <a name="sqlstate-property-ado"></a><span data-ttu-id="bd950-102">SQLState Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd950-102">SQLState Property (ADO)</span></span>


<span data-ttu-id="bd950-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd950-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd950-104">Указывает состояние SQL для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bd950-104">Indicates the SQL state for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd950-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd950-105">Return Value</span></span>

<span data-ttu-id="bd950-106">Возвращает **строковое** значение пяти символов, которая стандарту ANSI SQL и указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="bd950-106">Returns a five-character **String** value that follows the ANSI SQL standard and indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd950-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd950-107">Remarks</span></span>

<span data-ttu-id="bd950-108">Используйте свойство **SQLState** читать код ошибки пяти знаков, поставщик возвращает при возникновении ошибки во время обработки инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="bd950-108">Use the **SQLState** property to read the five-character error code that the provider returns when an error occurs during the processing of an SQL statement.</span></span> <span data-ttu-id="bd950-109">Например при использовании поставщик Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server, коды ошибок состояний SQL берутся из ODBC, основанные на ошибки, относящиеся к ODBC или на ошибки, которые создаются из Microsoft SQL Server, а затем сопоставляются с ODBC ошибки.</span><span class="sxs-lookup"><span data-stu-id="bd950-109">For example, when using the Microsoft OLE DB Provider for ODBC with a Microsoft SQL Server database, SQL state error codes originate from ODBC, based either on errors specific to ODBC or on errors that originate from Microsoft SQL Server, and are then mapped to ODBC errors.</span></span> <span data-ttu-id="bd950-110">Эти коды ошибок описаны в стандарте ANSI SQL, но может быть по-разному реализован различных источников данных.</span><span class="sxs-lookup"><span data-stu-id="bd950-110">These error codes are documented in the ANSI SQL standard, but may be implemented differently by different data sources.</span></span>

