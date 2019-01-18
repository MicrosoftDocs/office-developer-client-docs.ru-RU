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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702987"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="c9e5f-102">Метод CancelBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9e5f-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="c9e5f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9e5f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9e5f-104">Показано, как отменить ожидающие пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9e5f-105">Syntax</span></span>

<span data-ttu-id="c9e5f-106">*набор записей*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="c9e5f-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="c9e5f-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="c9e5f-107">Parameters</span></span>

|<span data-ttu-id="c9e5f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="c9e5f-108">Parameter</span></span>|<span data-ttu-id="c9e5f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c9e5f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c9e5f-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="c9e5f-110">*AffectRecords*</span></span> |<span data-ttu-id="c9e5f-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-111">Optional.</span></span> <span data-ttu-id="c9e5f-112">От [AffectEnum](affectenum.md) значение, которое указывает, сколько записей влияет на метод **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="c9e5f-112">An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="c9e5f-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9e5f-113">Remarks</span></span>

<span data-ttu-id="c9e5f-114">Используйте метод **CancelBatch** для отмены ли ожидающих установки обновлений в [записей](recordset-object-ado.md) в пакетном режиме обновления.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-114">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode.</span></span> <span data-ttu-id="c9e5f-115">Если в режиме немедленное обновление **набора записей** , вызов **CancelBatch** без **adAffectCurrent** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-115">If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="c9e5f-116">При изменении текущей записи или добавление новой записи при вызове **CancelBatch**ADO сначала вызывает метод [CancelUpdate](cancelupdate-method-ado.md) , чтобы отменить все изменения кэширования.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-116">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes.</span></span> <span data-ttu-id="c9e5f-117">После этого отменяются все ожидающие изменения в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="c9e5f-117">After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="c9e5f-118">Это и возможно, что текущей записи будут неопределенной после вызова метода **CancelBatch** , особенно в том случае, если были в процессе добавления новой записи.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-118">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record.</span></span> <span data-ttu-id="c9e5f-119">По этой причине лучше установка в настоящее время записи для заданного расположения в **записей** после вызова **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="c9e5f-119">For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call.</span></span> <span data-ttu-id="c9e5f-120">Например вызовите метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e5f-120">For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="c9e5f-121">Если не удалось отменить ожидающие обновления из-за конфликта с базовыми данными (например, запись была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-121">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="c9e5f-122">Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-122">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="c9e5f-123">Используйте свойство [фильтра](filter-property-ado.md) (**adFilterAffectedRecords**) и свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="c9e5f-123">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

