---
title: Метод Recordset.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f34085cf4b53bd94a9d9a7693cf68dd880e0a46
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922813"
---
# <a name="recordsetmovenext-method-dao"></a><span data-ttu-id="a9938-102">Метод Recordset.MoveNext (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9938-102">Recordset.MoveNext method (DAO)</span></span>


<span data-ttu-id="a9938-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9938-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9938-104">Переход к следующей записи в указанном объекте **набора записей** и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a9938-104">Moves to the next record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9938-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9938-105">Syntax</span></span>

<span data-ttu-id="a9938-106">*выражение* . MoveNext</span><span class="sxs-lookup"><span data-stu-id="a9938-106">*expression* .MoveNext</span></span>

<span data-ttu-id="a9938-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a9938-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9938-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="a9938-108">Remarks</span></span>

<span data-ttu-id="a9938-109">Используйте методы **перемещения** для перемещения между записями без применения условие.</span><span class="sxs-lookup"><span data-stu-id="a9938-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="a9938-110">При изменении текущей записи убедитесь, что использование метода **Update** для сохранения изменений перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="a9938-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="a9938-111">При перемещении к другой записи без обновления, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="a9938-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="a9938-112">При открытии **набора записей**первой записи текущего и **BOF** свойство имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="a9938-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="a9938-113">**Набор записей** не содержит записей, свойство **BOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a9938-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="a9938-114">При использовании **MoveNext** при последней записи текущего свойство **EOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="a9938-114">If you use **MoveNext** when the last record is current, the **EOF** property is **True**, and there is no current record.</span></span> <span data-ttu-id="a9938-115">Если вы используете **MoveNext** еще раз, возникает ошибка, и **EOF** остается равным **True**.</span><span class="sxs-lookup"><span data-stu-id="a9938-115">If you use **MoveNext** again, an error occurs, and **EOF** remains **True**.</span></span>

<span data-ttu-id="a9938-116">Если записей относится к таблице типа **записей** (только для рабочих областей Microsoft Access), перемещение за текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="a9938-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="a9938-117">Индекс текущей можно задать с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="a9938-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="a9938-118">Если не установить текущий индекс, порядок возвращаемых записей не определено.</span><span class="sxs-lookup"><span data-stu-id="a9938-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="a9938-119">Нельзя использовать методы **MoveFirst** **MoveLast**и **MovePrevious** для прямого — только – тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a9938-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="a9938-120">Для смещения позиции текущего записей в объекте **набора записей** определенного количества записей вперед или назад, используйте метод **Move** .</span><span class="sxs-lookup"><span data-stu-id="a9938-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

