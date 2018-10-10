---
title: Recordset.MoveFirst Method (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 12777635987d322517d17d93d02421a8f1490451
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481402"
---
# <a name="recordsetmovefirst-method-dao"></a><span data-ttu-id="f99d0-102">Recordset.MoveFirst Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="f99d0-102">Recordset.MoveFirst Method (DAO)</span></span>


<span data-ttu-id="f99d0-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f99d0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f99d0-104">Переход к первой записи в указанном объекте **набора записей** и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f99d0-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f99d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f99d0-105">Syntax</span></span>

<span data-ttu-id="f99d0-106">*выражение* . MoveFirst</span><span class="sxs-lookup"><span data-stu-id="f99d0-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="f99d0-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f99d0-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f99d0-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="f99d0-108">Remarks</span></span>

<span data-ttu-id="f99d0-109">Используйте методы **перемещения** для перемещения между записями без применения условие.</span><span class="sxs-lookup"><span data-stu-id="f99d0-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="f99d0-110">При изменении текущей записи убедитесь, что использование метода **Update** для сохранения изменений перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="f99d0-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="f99d0-111">При перемещении к другой записи без обновления, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="f99d0-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="f99d0-112">При открытии **набора записей**первой записи текущего и **BOF** свойство имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="f99d0-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="f99d0-113">**Набор записей** не содержит записей, свойство **BOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f99d0-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="f99d0-114">Если первой или последней записи текущего при использовании **MoveFirst** или **MoveLast**, не изменяется при текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f99d0-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="f99d0-115">Если записей относится к таблице типа **записей** (только для рабочих областей Microsoft Access), перемещение за текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="f99d0-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="f99d0-116">Индекс текущей можно задать с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="f99d0-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="f99d0-117">Если не установить текущий индекс, порядок возвращаемых записей не определено.</span><span class="sxs-lookup"><span data-stu-id="f99d0-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="f99d0-118">Нельзя использовать методы **MoveFirst** **MoveLast**и **MovePrevious** для прямого — только – тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="f99d0-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="f99d0-119">Для смещения позиции текущего записей в объекте **набора записей** определенного количества записей вперед или назад, используйте метод **Move** .</span><span class="sxs-lookup"><span data-stu-id="f99d0-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

