---
title: Метод CancelUpdate (RDS)
TOCTitle: CancelUpdate method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6a6427574cd04d8196153618c5960cb38da2b04
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924738"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="8345d-102">Метод CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="8345d-102">CancelUpdate method (RDS)</span></span>


<span data-ttu-id="8345d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8345d-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="8345d-104">Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8345d-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8345d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8345d-105">Syntax</span></span>

<span data-ttu-id="8345d-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="8345d-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="8345d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8345d-107">Parameters</span></span>

  - <span data-ttu-id="8345d-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="8345d-108">*DataControl*</span></span>

  - <span data-ttu-id="8345d-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="8345d-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8345d-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="8345d-110">Remarks</span></span>

<span data-ttu-id="8345d-111">Служба курсора для OLE DB сохраняет как копию исходных значений, так и в кэш изменений.</span><span class="sxs-lookup"><span data-stu-id="8345d-111">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</span></span> <span data-ttu-id="8345d-112">При вызове **CancelUpdate**выполнен сброс кэша изменения пустая строка, и все привязки элементов управления обновляется с исходными данными.</span><span class="sxs-lookup"><span data-stu-id="8345d-112">When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

