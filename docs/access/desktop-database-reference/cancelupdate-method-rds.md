---
title: Метод CancelUpdate (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28216cbeb98a0ebc7dfbc6115ea8bc05fadc057f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887749"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="81e4b-102">Метод CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="81e4b-102">CancelUpdate Method (RDS)</span></span>


<span data-ttu-id="81e4b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81e4b-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="81e4b-104">Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="81e4b-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81e4b-105">Syntax</span></span>

<span data-ttu-id="81e4b-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="81e4b-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="81e4b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="81e4b-107">Parameters</span></span>

  - <span data-ttu-id="81e4b-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="81e4b-108">*DataControl*</span></span>

  - <span data-ttu-id="81e4b-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="81e4b-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e4b-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="81e4b-110">Remarks</span></span>

<span data-ttu-id="81e4b-111">Служба курсора для OLE DB сохраняет как копию исходных значений, так и в кэш изменений.</span><span class="sxs-lookup"><span data-stu-id="81e4b-111">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</span></span> <span data-ttu-id="81e4b-112">При вызове **CancelUpdate**выполнен сброс кэша изменения пустая строка, и все привязки элементов управления обновляется с исходными данными.</span><span class="sxs-lookup"><span data-stu-id="81e4b-112">When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

