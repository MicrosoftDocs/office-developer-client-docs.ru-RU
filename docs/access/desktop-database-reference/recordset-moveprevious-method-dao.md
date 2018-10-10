---
title: Recordset.MovePrevious Method (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 82a3bc3e-5221-9a1a-1350-47bc6759edeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196699(v=office.15)
ms:contentKeyID: 48545984
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052872
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 22832abd8a573c4e7dc45b5f7827019e5e577964
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480960"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="9cad7-102">Recordset.MovePrevious Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="9cad7-102">Recordset.MovePrevious Method (DAO)</span></span>


<span data-ttu-id="9cad7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cad7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9cad7-104">Переход к предыдущей записи в указанный **набор записей** объекта и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9cad7-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cad7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cad7-105">Syntax</span></span>

<span data-ttu-id="9cad7-106">*выражение* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="9cad7-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="9cad7-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9cad7-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cad7-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="9cad7-108">Remarks</span></span>

<span data-ttu-id="9cad7-109">Используйте методы **перемещения** для перемещения между записями без применения условие.</span><span class="sxs-lookup"><span data-stu-id="9cad7-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="9cad7-110">При изменении текущей записи убедитесь, что использование метода **Update** для сохранения изменений перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="9cad7-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="9cad7-111">При перемещении к другой записи без обновления, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9cad7-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="9cad7-112">При открытии **набора записей**первой записи текущего и **BOF** свойство имеет **значение False**.</span><span class="sxs-lookup"><span data-stu-id="9cad7-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="9cad7-113">**Набор записей** не содержит записей, свойство **BOF** имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9cad7-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="9cad7-114">При использовании **MovePrevious** при первой записи текущего **BOF** свойство имеет **значение True**, и нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="9cad7-114">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record.</span></span> <span data-ttu-id="9cad7-115">Если вы используете **MovePrevious** еще раз, возникает ошибка, и **BOF** остается равным **True**.</span><span class="sxs-lookup"><span data-stu-id="9cad7-115">If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="9cad7-116">Если записей относится к таблице типа **записей** (только для рабочих областей Microsoft Access), перемещение за текущий индекс.</span><span class="sxs-lookup"><span data-stu-id="9cad7-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="9cad7-117">Индекс текущей можно задать с помощью свойства **индекса** .</span><span class="sxs-lookup"><span data-stu-id="9cad7-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="9cad7-118">Если не установить текущий индекс, порядок возвращаемых записей не определено.</span><span class="sxs-lookup"><span data-stu-id="9cad7-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="9cad7-119">Нельзя использовать методы **MoveFirst** **MoveLast**и **MovePrevious** для прямого — только – тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9cad7-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="9cad7-120">Для смещения позиции текущего записей в объекте **набора записей** определенного количества записей вперед или назад, используйте метод **Move** .</span><span class="sxs-lookup"><span data-stu-id="9cad7-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

