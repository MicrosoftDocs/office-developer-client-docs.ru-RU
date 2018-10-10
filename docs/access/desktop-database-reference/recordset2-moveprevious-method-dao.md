---
title: Recordset2.MovePrevious Method (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d437fe3bb271cc50c187b185bcd3078b523a73a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479989"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="1b324-102">Recordset2.MovePrevious Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="1b324-102">Recordset2.MovePrevious Method (DAO)</span></span>


<span data-ttu-id="1b324-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b324-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1b324-104">Переход к предыдущей записи в указанный **набор записей** объекта и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1b324-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b324-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b324-105">Syntax</span></span>

<span data-ttu-id="1b324-106">*выражение* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="1b324-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="1b324-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="1b324-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b324-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b324-108">Remarks</span></span>

<span data-ttu-id="1b324-109">Используйте методы **перемещения** для перемещения между записями без применения условие.</span><span class="sxs-lookup"><span data-stu-id="1b324-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="1b324-110">При изменении текущей записи убедитесь, что использование метода **Update** для сохранения изменений перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="1b324-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="1b324-111">При перемещении к другой записи без обновления, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="1b324-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="1b324-112">При открытии **набора записей**первой записи текущего и **BOF** свойство имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="1b324-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="1b324-113">**Набор записей** не содержит записей, свойство **BOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1b324-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="1b324-114">При использовании **MovePrevious** при первой записи текущего **BOF** свойство имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1b324-114">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record.</span></span> <span data-ttu-id="1b324-115">Если вы используете **MovePrevious** еще раз, возникает ошибка, и **BOF** остается равным **True**.</span><span class="sxs-lookup"><span data-stu-id="1b324-115">If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="1b324-116">Если записей относится к таблице типа **записей** (только для рабочих областей Microsoft Access), перемещение за текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="1b324-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="1b324-117">Индекс текущей можно задать с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="1b324-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="1b324-118">Если не установить текущий индекс, порядок возвращаемых записей не определено.</span><span class="sxs-lookup"><span data-stu-id="1b324-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="1b324-119">Нельзя использовать методы **MoveFirst** **MoveLast**и **MovePrevious** для прямого — только – тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1b324-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="1b324-120">Для смещения позиции текущего записей в объекте **набора записей** определенного количества записей вперед или назад, используйте метод **Move** .</span><span class="sxs-lookup"><span data-stu-id="1b324-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

