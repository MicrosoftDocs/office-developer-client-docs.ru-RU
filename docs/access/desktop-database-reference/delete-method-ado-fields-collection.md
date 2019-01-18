---
title: Удаление метода (коллекции полей ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718261"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="76de2-102">Удаление метода (коллекции полей ADO)</span><span class="sxs-lookup"><span data-stu-id="76de2-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="76de2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76de2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="76de2-104">Удаляет объект из коллекции [полей](fields-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="76de2-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="76de2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76de2-105">Syntax</span></span>

<span data-ttu-id="76de2-106">*Поля*. Удаление*поля*</span><span class="sxs-lookup"><span data-stu-id="76de2-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="76de2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="76de2-107">Parameters</span></span>

|<span data-ttu-id="76de2-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="76de2-108">Parameter</span></span>|<span data-ttu-id="76de2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="76de2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="76de2-110">*Поле*</span><span class="sxs-lookup"><span data-stu-id="76de2-110">*Field*</span></span> |<span data-ttu-id="76de2-111">**Variant** , который определяет удаляемый объект [поля](field-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="76de2-111">A **Variant** that designates the [Field](field-object-ado.md) object to delete.</span></span> <span data-ttu-id="76de2-112">Этот параметр может быть имя объекта **поля** или порядковый номер самого объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="76de2-112">This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="76de2-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="76de2-113">Remarks</span></span>

<span data-ttu-id="76de2-114">Вызов метода **Fields.Delete** для открытия [набора записей](recordset-object-ado.md) вызывает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="76de2-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

