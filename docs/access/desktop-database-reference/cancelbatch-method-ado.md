---
title: Метод CancelBatch (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eefe1042404c24040aef204a1ceca0ce583847e8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926957"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="d7a1f-102">Метод CancelBatch (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7a1f-102">CancelBatch method (ADO)</span></span>


<span data-ttu-id="d7a1f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7a1f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d7a1f-104">Показано, как отменить ожидающие пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7a1f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7a1f-105">Syntax</span></span>

<span data-ttu-id="d7a1f-106">*набор записей*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="d7a1f-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="d7a1f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7a1f-107">Parameters</span></span>

  - <span data-ttu-id="d7a1f-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="d7a1f-108">*AffectRecords*</span></span>

  - <span data-ttu-id="d7a1f-109">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-109">Optional.</span></span> <span data-ttu-id="d7a1f-110">От [AffectEnum](affectenum.md) значение, которое указывает, сколько записей влияет на метод **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="d7a1f-110">An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a1f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7a1f-111">Remarks</span></span>

<span data-ttu-id="d7a1f-112">Используйте метод **CancelBatch** для отмены ли ожидающих установки обновлений в [записей](recordset-object-ado.md) в пакетном режиме обновления.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-112">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode.</span></span> <span data-ttu-id="d7a1f-113">Если в режиме немедленное обновление **набора записей** , вызов **CancelBatch** без **adAffectCurrent** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-113">If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="d7a1f-114">При изменении текущей записи или добавление новой записи при вызове **CancelBatch**ADO сначала вызывает метод [CancelUpdate](cancelupdate-method-ado.md) , чтобы отменить все изменения кэширования.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-114">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes.</span></span> <span data-ttu-id="d7a1f-115">После этого отменяются все ожидающие изменения в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="d7a1f-115">After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="d7a1f-116">Это и возможно, что текущей записи будут неопределенной после вызова метода **CancelBatch** , особенно в том случае, если были в процессе добавления новой записи.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-116">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record.</span></span> <span data-ttu-id="d7a1f-117">По этой причине лучше установка в настоящее время записи для заданного расположения в **записей** после вызова **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="d7a1f-117">For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call.</span></span> <span data-ttu-id="d7a1f-118">Например вызовите метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a1f-118">For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="d7a1f-119">Если не удалось отменить ожидающие обновления из-за конфликта с базовыми данными (например, запись была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-119">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="d7a1f-120">Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-120">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="d7a1f-121">Используйте свойство [фильтра](filter-property-ado.md) (**adFilterAffectedRecords**) и свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="d7a1f-121">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

