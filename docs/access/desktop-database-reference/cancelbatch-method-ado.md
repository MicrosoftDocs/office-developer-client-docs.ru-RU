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
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="3a116-102">Метод CancelBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a116-102">CancelBatch method (ADO)</span></span>

<span data-ttu-id="3a116-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a116-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a116-104">Отменяет ожидающее пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="3a116-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a116-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a116-105">Syntax</span></span>

<span data-ttu-id="3a116-106">*набор записей*. CancelBatch *аффектрекордс*</span><span class="sxs-lookup"><span data-stu-id="3a116-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="3a116-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a116-107">Parameters</span></span>

|<span data-ttu-id="3a116-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="3a116-108">Parameter</span></span>|<span data-ttu-id="3a116-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3a116-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3a116-110">*аффектрекордс*</span><span class="sxs-lookup"><span data-stu-id="3a116-110">*AffectRecords*</span></span> |<span data-ttu-id="3a116-111">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="3a116-111">Optional.</span></span> <span data-ttu-id="3a116-112">Значение [аффектенум](affectenum.md) , указывающее количество записей, на которые влияет метод **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="3a116-112">An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span> |

## <a name="remarks"></a><span data-ttu-id="3a116-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a116-113">Remarks</span></span>

<span data-ttu-id="3a116-114">Используйте метод **CancelBatch** , чтобы отменить все ожидающие обновления в [наборе записей](recordset-object-ado.md) в режиме пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="3a116-114">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode.</span></span> <span data-ttu-id="3a116-115">Если **набор записей** находится в режиме немедленного обновления, то при вызове **CancelBatch** без **адаффекткуррент** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a116-115">If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="3a116-116">Если вы редактируете текущую запись или добавляете новую запись при вызове **CancelBatch**, ADO сначала вызывает метод [CancelUpdate](cancelupdate-method-ado.md) для отмены всех кэшированных изменений.</span><span class="sxs-lookup"><span data-stu-id="3a116-116">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes.</span></span> <span data-ttu-id="3a116-117">После этого отменяются все ожидающие изменения в **наборе записей** .</span><span class="sxs-lookup"><span data-stu-id="3a116-117">After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="3a116-118">Возможно, что текущая запись станет недетерминированной после вызова **CancelBatch** , особенно в том случае, если вы намерены добавить новую запись.</span><span class="sxs-lookup"><span data-stu-id="3a116-118">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record.</span></span> <span data-ttu-id="3a116-119">По этой причине рекомендуется присвоить текущей позиции записи известное расположение в **наборе записей** после вызова **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="3a116-119">For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call.</span></span> <span data-ttu-id="3a116-120">Например, вызовите метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3a116-120">For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="3a116-121">Если попытка отменить ожидающие обновления не удалась из-за конфликта с базовыми данными (например, запись была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию [ошибок](errors-collection-ado.md) , но не приостанавливает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="3a116-121">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="3a116-122">Ошибка во время выполнения возникает только в том случае, если имеются конфликты со всеми запрошенными записями.</span><span class="sxs-lookup"><span data-stu-id="3a116-122">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="3a116-123">Используйте свойство [Filter](filter-property-ado.md) (**адфилтераффектедрекордс**) и свойство [Status](status-property-ado-recordset.md) для обнаружения записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="3a116-123">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

