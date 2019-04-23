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
# <a name="nativeerror-property-ado"></a><span data-ttu-id="28dcd-102">Свойство NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="28dcd-102">NativeError property (ADO)</span></span>


<span data-ttu-id="28dcd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28dcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28dcd-104">Указывает код ошибки, зависящий от поставщика, для данного объекта [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="28dcd-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="28dcd-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28dcd-105">Return value</span></span>

<span data-ttu-id="28dcd-106">Возвращает значение **типа Long** , которое указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="28dcd-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28dcd-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="28dcd-107">Remarks</span></span>

<span data-ttu-id="28dcd-108">Используйте свойство **NativeError** для получения сведений об ошибках, связанных с базой данных, для определенного объекта **Error** .</span><span class="sxs-lookup"><span data-stu-id="28dcd-108">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object.</span></span> <span data-ttu-id="28dcd-109">Например, при использовании поставщика Microsoft ODBC для OLE DB с базой данных Microsoft SQL Server собственные коды ошибок, полученные с помощью ODBC и поставщика ODBC, в свойство ADO **NativeError** .</span><span class="sxs-lookup"><span data-stu-id="28dcd-109">For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

