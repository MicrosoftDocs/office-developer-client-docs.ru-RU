---
title: Свойство NativeError (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288612"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="941f9-102">Свойство NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="941f9-102">NativeError property (ADO)</span></span>


<span data-ttu-id="941f9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="941f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="941f9-104">Указывает код ошибки для определенного поставщика для данного объекта [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="941f9-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="941f9-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="941f9-105">Return value</span></span>

<span data-ttu-id="941f9-106">Возвращает **длинное значение,** которое указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="941f9-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="941f9-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="941f9-107">Remarks</span></span>

<span data-ttu-id="941f9-108">Используйте свойство **NativeError** для получения сведений об ошибках для определенного объекта **Error.**</span><span class="sxs-lookup"><span data-stu-id="941f9-108">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object.</span></span> <span data-ttu-id="941f9-109">Например, при использовании поставщика ODBC Microsoft для OLE DB с базой данных Microsoft SQL Server, коды ошибок, которые происходят из SQL Server, передаются через ODBC и поставщику ODBC в свойство ADO **NativeError.**</span><span class="sxs-lookup"><span data-stu-id="941f9-109">For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

