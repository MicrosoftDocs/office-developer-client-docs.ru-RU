---
title: Удаление метода (коллекции параметров ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b18a09d6a0c9d6a6ad8e9f579068c4f6d7162d1f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944874"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="b7a8c-102">Удаление метода (коллекции параметров ADO)</span><span class="sxs-lookup"><span data-stu-id="b7a8c-102">Delete method (ADO Parameters Collection)</span></span>


<span data-ttu-id="b7a8c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7a8c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b7a8c-104">Удаляет объект из коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a8c-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7a8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7a8c-105">Syntax</span></span>

<span data-ttu-id="b7a8c-106">*Параметры*. Удаление *индекса*</span><span class="sxs-lookup"><span data-stu-id="b7a8c-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="b7a8c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7a8c-107">Parameters</span></span>

- <span data-ttu-id="b7a8c-108">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="b7a8c-108">*Index*</span></span>

  - <span data-ttu-id="b7a8c-109">**Строковое** значение, содержащее имя объекта, который требуется удалить или объекты порядковый номер (индекс) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b7a8c-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7a8c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7a8c-110">Remarks</span></span>

<span data-ttu-id="b7a8c-111">С помощью метода **Delete** в семействе сайтов позволяет удалить один из объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b7a8c-111">Using the **Delete** method on a collection lets you remove one of the objects in the collection.</span></span> <span data-ttu-id="b7a8c-112">Этот метод доступен только в коллекции **параметров** объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a8c-112">This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="b7a8c-113">Необходимо использовать свойство [Name](name-property-ado.md) объекта [параметра](parameter-object-ado.md) или индекса коллекции при вызове метода **Delete** — объектная переменная не является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="b7a8c-113">You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

