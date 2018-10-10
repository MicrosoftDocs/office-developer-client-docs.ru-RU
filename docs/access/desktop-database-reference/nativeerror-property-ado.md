---
title: NativeError Property (ADO)
TOCTitle: NativeError Property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b98d9695e29df63371b5ee375f864e7b1d4961ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483159"
---
# <a name="nativeerror-property-ado"></a><span data-ttu-id="b61b5-102">NativeError Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="b61b5-102">NativeError Property (ADO)</span></span>


<span data-ttu-id="b61b5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b61b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b61b5-104">Указывает код ошибки поставщика для того или иного объекта [ошибки](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b61b5-104">Indicates the provider-specific error code for a given [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="b61b5-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b61b5-105">Return Value</span></span>

<span data-ttu-id="b61b5-106">Возвращает значение типа **Long** , указывающее код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b61b5-106">Returns a **Long** value that indicates the error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b61b5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="b61b5-107">Remarks</span></span>

<span data-ttu-id="b61b5-108">Используйте свойство **NativeError** получение сведений о базе данных об ошибке для определенный объект **Error** .</span><span class="sxs-lookup"><span data-stu-id="b61b5-108">Use the **NativeError** property to retrieve the database-specific error information for a particular **Error** object.</span></span> <span data-ttu-id="b61b5-109">Например при использовании поставщика ODBC Microsoft для OLE DB с базой данных Microsoft SQL Server, коды собственной ошибки, которые создаются из SQL Server проходить через ODBC и поставщика ODBC свойство ADO **NativeError** .</span><span class="sxs-lookup"><span data-stu-id="b61b5-109">For example, when using the Microsoft ODBC Provider for OLE DB with a Microsoft SQL Server database, native error codes that originate from SQL Server pass through ODBC and the ODBC Provider to the ADO **NativeError** property.</span></span>

