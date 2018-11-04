---
title: Удаление метода (коллекции полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b33c15adf1d079e2da12590891d950aa35e5414f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950178"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="9e792-102">Удаление метода (коллекции полей ADO)</span><span class="sxs-lookup"><span data-stu-id="9e792-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="9e792-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e792-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9e792-104">Удаляет объект из коллекции [полей](fields-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9e792-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e792-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e792-105">Syntax</span></span>

<span data-ttu-id="9e792-106">*Поля*. Удаление*поля*</span><span class="sxs-lookup"><span data-stu-id="9e792-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="9e792-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e792-107">Parameters</span></span>

|<span data-ttu-id="9e792-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="9e792-108">Parameter</span></span>|<span data-ttu-id="9e792-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9e792-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9e792-110">*Поле*</span><span class="sxs-lookup"><span data-stu-id="9e792-110">*Field*</span></span> |<span data-ttu-id="9e792-111">**Variant** , который определяет удаляемый объект [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9e792-111">A **Variant** that designates the [Field](field-object-ado.md) object to delete.</span></span> <span data-ttu-id="9e792-112">Этот параметр может быть имя объекта **поля** или порядковый номер самого объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="9e792-112">This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9e792-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e792-113">Remarks</span></span>

<span data-ttu-id="9e792-114">Вызов метода **Fields.Delete** для открытия [набора записей](recordset-object-ado.md) вызывает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="9e792-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

