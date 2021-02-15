---
title: Метод Recordset.MovePrevious (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 95cf5daa9eac6644b17f47b09ebc749bd9ed928e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284513"
---
# <a name="recordsetmoveprevious-method-dao"></a><span data-ttu-id="16c39-102">Метод Recordset.MovePrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="16c39-102">Recordset.MovePrevious method (DAO)</span></span>


<span data-ttu-id="16c39-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16c39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16c39-104">Выполняет перемещение к предыдущей записи в указанном объекте **Recordset** и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="16c39-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c39-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16c39-105">Syntax</span></span>

<span data-ttu-id="16c39-106">*выражение .* MovePrevious</span><span class="sxs-lookup"><span data-stu-id="16c39-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="16c39-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="16c39-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16c39-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16c39-108">Remarks</span></span>

<span data-ttu-id="16c39-109">Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.</span><span class="sxs-lookup"><span data-stu-id="16c39-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="16c39-110">Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="16c39-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="16c39-111">Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="16c39-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="16c39-112">Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="16c39-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="16c39-113">Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="16c39-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="16c39-114">Если вы используете **MovePrevious,** когда первая запись является текущей, свойство **BOF** имеет свойство **True,** и текущая запись не существует.</span><span class="sxs-lookup"><span data-stu-id="16c39-114">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record.</span></span> <span data-ttu-id="16c39-115">Если вы снова **используете MovePrevious,** возникает ошибка, а **BOF** остается **true.**</span><span class="sxs-lookup"><span data-stu-id="16c39-115">If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="16c39-116">Если набор записей указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение соответствует текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="16c39-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="16c39-117">Вы можете задать текущий индекс с помощью свойства **Index**.</span><span class="sxs-lookup"><span data-stu-id="16c39-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="16c39-118">Если не задать текущей индекс, порядок возвращаемых записей будет не определен.</span><span class="sxs-lookup"><span data-stu-id="16c39-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="16c39-119">Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="16c39-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="16c39-120">Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.</span><span class="sxs-lookup"><span data-stu-id="16c39-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

