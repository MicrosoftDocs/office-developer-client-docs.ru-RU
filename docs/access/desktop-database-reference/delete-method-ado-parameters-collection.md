---
title: Delete Method (ADO Parameters Collection)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482008"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="4dcda-102">Delete Method (ADO Parameters Collection)</span><span class="sxs-lookup"><span data-stu-id="4dcda-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="4dcda-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dcda-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="4dcda-104">Удаляет объект из коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4dcda-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dcda-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dcda-105">Syntax</span></span>

<span data-ttu-id="4dcda-106">*Параметры*. Удаление *индекса*</span><span class="sxs-lookup"><span data-stu-id="4dcda-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="4dcda-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dcda-107">Parameters</span></span>

  - <span data-ttu-id="4dcda-108">*Индекс*</span><span class="sxs-lookup"><span data-stu-id="4dcda-108">*Index*</span></span>

  - <span data-ttu-id="4dcda-109">**Строковое** значение, содержащее имя объекта, который требуется удалить или объекты порядковый номер (индекс) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4dcda-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dcda-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="4dcda-110">Remarks</span></span>

<span data-ttu-id="4dcda-111">С помощью метода **Delete** в семействе сайтов позволяет удалить один из объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4dcda-111">Using the **Delete** method on a collection lets you remove one of the objects in the collection.</span></span> <span data-ttu-id="4dcda-112">Этот метод доступен только в коллекции **параметров** объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4dcda-112">This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="4dcda-113">Необходимо использовать свойство [Name](name-property-ado.md) объекта [параметра](parameter-object-ado.md) или индекса коллекции при вызове метода **Delete** — объектная переменная не является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4dcda-113">You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

