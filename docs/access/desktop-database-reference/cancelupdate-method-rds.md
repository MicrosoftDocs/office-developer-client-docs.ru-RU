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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296670"
---
# <a name="cancelupdate-method-rds"></a><span data-ttu-id="df317-102">Метод CancelUpdate (RDS)</span><span class="sxs-lookup"><span data-stu-id="df317-102">CancelUpdate method (RDS)</span></span>

<span data-ttu-id="df317-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df317-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="df317-104">Отменяет все изменения, внесенные в текущую или новую строку объекта [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="df317-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="df317-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df317-105">Syntax</span></span>

<span data-ttu-id="df317-106">*DataControl*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="df317-106">*DataControl*.CancelUpdate</span></span>

## <a name="parameters"></a><span data-ttu-id="df317-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="df317-107">Parameters</span></span>

|<span data-ttu-id="df317-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="df317-108">Parameter</span></span>|<span data-ttu-id="df317-109">Описание</span><span class="sxs-lookup"><span data-stu-id="df317-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="df317-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="df317-110">*DataControl*</span></span> |<span data-ttu-id="df317-111">Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="df317-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="df317-112">Заметки</span><span class="sxs-lookup"><span data-stu-id="df317-112">Remarks</span></span>

<span data-ttu-id="df317-113">Служба курсоров для OLE DB сохраняет копию исходных значений и кэш изменений.</span><span class="sxs-lookup"><span data-stu-id="df317-113">The Cursor Service for OLE DB keeps both a copy of the original values and a cache of changes.</span></span> <span data-ttu-id="df317-114">При вызове **CancelUpdate** кэш изменений сбрасывается в пустое состояние, а все связанные элементы управления обновляются исходными данными.</span><span class="sxs-lookup"><span data-stu-id="df317-114">When you call **CancelUpdate**, the cache of changes is reset to empty, and any bound controls are refreshed with the original data.</span></span>

