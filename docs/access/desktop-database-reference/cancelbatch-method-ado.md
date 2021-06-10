---
title: Метод CancelBatch (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 832b367824fd8043486ff85f63739c3288696774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296642"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="401a2-102">Метод CancelBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="401a2-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="401a2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="401a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="401a2-104">Отмена ожидающих пакетных обновлений.</span><span class="sxs-lookup"><span data-stu-id="401a2-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="401a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="401a2-105">Syntax</span></span>

<span data-ttu-id="401a2-106">*набор записей.* CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="401a2-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="401a2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="401a2-107">Parameters</span></span>

|<span data-ttu-id="401a2-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="401a2-108">Parameter</span></span>|<span data-ttu-id="401a2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="401a2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="401a2-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="401a2-110">*AffectRecords*</span></span> |<span data-ttu-id="401a2-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="401a2-111">Optional.</span></span> <span data-ttu-id="401a2-112">Значение [AffectEnum,](affectenum.md) которое указывает, сколько записей повлияет на метод **CancelBatch.**</span><span class="sxs-lookup"><span data-stu-id="401a2-112">An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="401a2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="401a2-113">Remarks</span></span>

<span data-ttu-id="401a2-114">Используйте метод **CancelBatch** для отмены ожидающих обновлений в [наборе записей](recordset-object-ado.md) в режиме пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="401a2-114">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode.</span></span> <span data-ttu-id="401a2-115">Если Набор **записей находится** в режиме немедленного обновления, вызов **CancelBatch** без **adAffectCurrent** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="401a2-115">If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="401a2-116">Если вы редактируете текущую запись или добавляете новую запись при вызове **CancelBatch,** ADO сначала вызывает метод [CancelUpdate,](cancelupdate-method-ado.md) чтобы отменить любые кэшированые изменения.</span><span class="sxs-lookup"><span data-stu-id="401a2-116">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes.</span></span> <span data-ttu-id="401a2-117">После этого все ожидающих изменений **в Наборе записей** отменяются.</span><span class="sxs-lookup"><span data-stu-id="401a2-117">After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="401a2-118">Возможно, текущая запись будет неопределима после вызова **CancelBatch,** особенно если вы были в процессе добавления новой записи.</span><span class="sxs-lookup"><span data-stu-id="401a2-118">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record.</span></span> <span data-ttu-id="401a2-119">По этой причине целесообразно установить текущее положение записи в известном расположении в **Наборе** записей после вызова **CancelBatch.**</span><span class="sxs-lookup"><span data-stu-id="401a2-119">For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call.</span></span> <span data-ttu-id="401a2-120">Например, позвоните [методу MoveFirst.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="401a2-120">For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="401a2-121">Если попытка отменить ожидающие обновления не удалась из-за конфликта с данными( например, запись была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию Ошибок, но не прекращает выполнение программы. [](errors-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="401a2-121">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="401a2-122">Ошибка во время запуска возникает только в том случае, если во всех запрашиваемых записях имеются конфликты.</span><span class="sxs-lookup"><span data-stu-id="401a2-122">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="401a2-123">Используйте свойство [Filter](filter-property-ado.md) **(adFilterAffectedRecords)** и свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="401a2-123">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

