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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705948"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="74088-102">Свойство NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="74088-102">NativeError property (ADO)</span></span>


<span data-ttu-id="74088-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74088-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74088-104">Указывает код ошибки поставщика для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="74088-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="74088-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74088-105">Return value</span></span>

<span data-ttu-id="74088-106">Возвращает значение типа **Long** , указывающее код ошибки.</span><span class="sxs-lookup"><span data-stu-id="74088-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74088-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="74088-107">Remarks</span></span>

<span data-ttu-id="74088-108">Используйте свойство **NativeError** получение сведений о базе данных об ошибке для определенный объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="74088-108">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object.</span></span> <span data-ttu-id="74088-109">Например при использовании поставщика ODBC Microsoft для OLE DB с базой данных Microsoft SQL Server, коды собственной ошибки, которые создаются из SQL Server проходить через ODBC и поставщика ODBC свойство ADO **NativeError** .</span><span class="sxs-lookup"><span data-stu-id="74088-109">For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

