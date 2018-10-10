---
title: CancelBatch Method (ADO)
TOCTitle: CancelBatch Method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cbc16d01e04bbcff7ff28ccc8e7cb4f3fd6f3dec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482147"
---
# <a name="cancelbatch-method-ado"></a><span data-ttu-id="01b85-102">CancelBatch Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="01b85-102">CancelBatch Method (ADO)</span></span>


<span data-ttu-id="01b85-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="01b85-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="01b85-104">Показано, как отменить ожидающие пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="01b85-104">Cancels a pending batch update.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b85-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01b85-105">Syntax</span></span>

<span data-ttu-id="01b85-106">*набор записей*. CancelBatch *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="01b85-106">*recordset*.CancelBatch *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="01b85-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01b85-107">Parameters</span></span>

  - <span data-ttu-id="01b85-108">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="01b85-108">*AffectRecords*</span></span>

  - <span data-ttu-id="01b85-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="01b85-109">Optional.</span></span> <span data-ttu-id="01b85-110">От [AffectEnum](affectenum.md) значение, которое указывает, сколько записей влияет на метод **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="01b85-110">An [AffectEnum](affectenum.md) value that indicates how many records the **CancelBatch** method will affect.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b85-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="01b85-111">Remarks</span></span>

<span data-ttu-id="01b85-112">Используйте метод **CancelBatch** для отмены ли ожидающих установки обновлений в [записей](recordset-object-ado.md) в пакетном режиме обновления.</span><span class="sxs-lookup"><span data-stu-id="01b85-112">Use the **CancelBatch** method to cancel any pending updates in a [Recordset](recordset-object-ado.md) in batch update mode.</span></span> <span data-ttu-id="01b85-113">Если в режиме немедленное обновление **набора записей** , вызов **CancelBatch** без **adAffectCurrent** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="01b85-113">If the **Recordset** is in immediate update mode, calling **CancelBatch** without **adAffectCurrent** generates an error.</span></span>

<span data-ttu-id="01b85-114">При изменении текущей записи или добавление новой записи при вызове **CancelBatch**ADO сначала вызывает метод [CancelUpdate](cancelupdate-method-ado.md) , чтобы отменить все изменения кэширования.</span><span class="sxs-lookup"><span data-stu-id="01b85-114">If you are editing the current record or are adding a new record when you call **CancelBatch**, ADO first calls the [CancelUpdate](cancelupdate-method-ado.md) method to cancel any cached changes.</span></span> <span data-ttu-id="01b85-115">После этого отменяются все ожидающие изменения в **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="01b85-115">After that, all pending changes in the **Recordset** are canceled.</span></span>

<span data-ttu-id="01b85-116">Это и возможно, что текущей записи будут неопределенной после вызова метода **CancelBatch** , особенно в том случае, если были в процессе добавления новой записи.</span><span class="sxs-lookup"><span data-stu-id="01b85-116">It's possible that the current record will be indeterminable after a **CancelBatch** call, especially if you were in the process of adding a new record.</span></span> <span data-ttu-id="01b85-117">По этой причине лучше установка в настоящее время записи для заданного расположения в **записей** после вызова **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="01b85-117">For this reason, it is prudent to set the current record position to a known location in the **Recordset** after the **CancelBatch** call.</span></span> <span data-ttu-id="01b85-118">Например вызовите метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="01b85-118">For example, call the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

<span data-ttu-id="01b85-119">Если не удалось отменить ожидающие обновления из-за конфликта с базовыми данными (например, запись была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="01b85-119">If the attempt to cancel the pending updates fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="01b85-120">Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="01b85-120">A run-time error occurs only if there are conflicts on all the requested records.</span></span> <span data-ttu-id="01b85-121">Используйте свойство [фильтра](filter-property-ado.md) (**adFilterAffectedRecords**) и свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.</span><span class="sxs-lookup"><span data-stu-id="01b85-121">Use the [Filter](filter-property-ado.md) property (**adFilterAffectedRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

