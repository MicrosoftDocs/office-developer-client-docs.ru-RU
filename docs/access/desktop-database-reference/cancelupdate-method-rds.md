---
title: CancelUpdate Method (RDS)
TOCTitle: CancelUpdate Method (RDS)
ms:assetid: 373a3feb-125d-915a-fd56-d4b04b20db54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249130(v=office.15)
ms:contentKeyID: 48544188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea646f2412ec078f3a45334ec2b1cdbe449285b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481038"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="3db33-102">CancelUpdate Method (RDS)</span><span class="sxs-lookup"><span data-stu-id="3db33-102">CancelUpdate Method (RDS)</span></span>


<span data-ttu-id="3db33-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3db33-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3db33-104">Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3db33-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db33-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3db33-105">Syntax</span></span>

<span data-ttu-id="3db33-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="3db33-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="3db33-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3db33-107">Parameters</span></span>

  - <span data-ttu-id="3db33-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3db33-108">*DataControl*</span></span>

  - <span data-ttu-id="3db33-109">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="3db33-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3db33-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="3db33-110">Remarks</span></span>

<span data-ttu-id="3db33-111">Служба курсора для OLE DB сохраняет как копию исходных значений, так и в кэш изменений.</span><span class="sxs-lookup"><span data-stu-id="3db33-111">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</span></span> <span data-ttu-id="3db33-112">При вызове **CancelUpdate**выполнен сброс кэша изменения пустая строка, и все привязки элементов управления обновляется с исходными данными.</span><span class="sxs-lookup"><span data-stu-id="3db33-112">When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

