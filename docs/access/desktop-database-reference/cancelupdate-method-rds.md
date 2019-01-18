---
title: Метод CancelUpdate (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0c02a9ca72add763e1d3ccf62d5ede8adaecc6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718618"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="d5214-102">Метод CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="d5214-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="d5214-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5214-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5214-104">Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d5214-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5214-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5214-105">Syntax</span></span>

<span data-ttu-id="d5214-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="d5214-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="d5214-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5214-107">Parameters</span></span>

|<span data-ttu-id="d5214-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d5214-108">Parameter</span></span>|<span data-ttu-id="d5214-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d5214-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d5214-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d5214-110">*DataControl*</span></span> |<span data-ttu-id="d5214-111">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="d5214-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d5214-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="d5214-112">Remarks</span></span>

<span data-ttu-id="d5214-113">Служба курсора для OLE DB сохраняет как копию исходных значений, так и в кэш изменений.</span><span class="sxs-lookup"><span data-stu-id="d5214-113">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</span></span> <span data-ttu-id="d5214-114">При вызове **CancelUpdate**выполнен сброс кэша изменения пустая строка, и все привязки элементов управления обновляется с исходными данными.</span><span class="sxs-lookup"><span data-stu-id="d5214-114">When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

