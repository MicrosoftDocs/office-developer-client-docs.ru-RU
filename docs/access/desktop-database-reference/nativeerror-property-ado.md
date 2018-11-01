---
title: Свойство NativeError (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d572e7629deca0c7732bafbdfdb0c600ce34a35
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880182"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="be6db-102">Свойство NativeError (ADO)</span><span class="sxs-lookup"><span data-stu-id="be6db-102">NativeError property (ADO)</span></span>


<span data-ttu-id="be6db-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be6db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be6db-104">Указывает код ошибки поставщика для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="be6db-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="be6db-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be6db-105">Return value</span></span>

<span data-ttu-id="be6db-106">Возвращает значение типа **Long** , указывающее код ошибки.</span><span class="sxs-lookup"><span data-stu-id="be6db-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be6db-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="be6db-107">Remarks</span></span>

<span data-ttu-id="be6db-108">Используйте свойство **NativeError** получение сведений о базе данных об ошибке для определенный объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="be6db-108">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object.</span></span> <span data-ttu-id="be6db-109">Например при использовании поставщика ODBC Microsoft для OLE DB с базой данных Microsoft SQL Server, коды собственной ошибки, которые создаются из SQL Server проходить через ODBC и поставщика ODBC свойство ADO **NativeError** .</span><span class="sxs-lookup"><span data-stu-id="be6db-109">For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

