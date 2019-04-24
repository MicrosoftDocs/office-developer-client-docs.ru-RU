---
title: Метод Delete (Коллекция параметров ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294094"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="024d6-102">Метод Delete (Коллекция параметров ADO)</span><span class="sxs-lookup"><span data-stu-id="024d6-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="024d6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="024d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="024d6-104">Удаляет объект из коллекции [Parameters](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="024d6-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="024d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="024d6-105">Syntax</span></span>

<span data-ttu-id="024d6-106">*Параметры*. Удаление *индекса*</span><span class="sxs-lookup"><span data-stu-id="024d6-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="024d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="024d6-107">Parameters</span></span>

|<span data-ttu-id="024d6-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="024d6-108">Parameter</span></span>|<span data-ttu-id="024d6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="024d6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="024d6-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="024d6-110">*Index*</span></span> |<span data-ttu-id="024d6-111">**Строковое** значение, содержащее имя удаляемого объекта или порядковый номер объекта (индекса) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="024d6-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="024d6-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="024d6-112">Remarks</span></span>

<span data-ttu-id="024d6-113">Использование метода **Delete** для коллекции позволяет удалить один из объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="024d6-113">Using the **Delete** method on a collection lets you remove one of the objects in the collection.</span></span> <span data-ttu-id="024d6-114">Этот метод доступен только для коллекции **Parameters** объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="024d6-114">This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="024d6-115">При вызове метода **Delete** необходимо использовать свойство [Name](name-property-ado.md) объекта [Parameter](parameter-object-ado.md) или его индекс (объектная переменная не является допустимым аргументом).</span><span class="sxs-lookup"><span data-stu-id="024d6-115">You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

