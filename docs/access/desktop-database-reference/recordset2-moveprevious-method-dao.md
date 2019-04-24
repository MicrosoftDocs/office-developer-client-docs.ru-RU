---
title: Метод Recordset2. MovePrevious (DAO)
TOCTitle: MovePrevious Method
ms:assetid: 8c433810-4b19-e7c1-3cee-a0bc50b23e8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197336(v=office.15)
ms:contentKeyID: 48546235
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9753d3bbb586e2c1bd44755deb529758d8eab060
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307247"
---
# <a name="recordset2moveprevious-method-dao"></a><span data-ttu-id="9f942-102">Метод Recordset2. MovePrevious (DAO)</span><span class="sxs-lookup"><span data-stu-id="9f942-102">Recordset2.MovePrevious method (DAO)</span></span>


<span data-ttu-id="9f942-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f942-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f942-104">Выполняет перемещение к предыдущей записи в указанном объекте **Recordset** и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="9f942-104">Moves to the previous record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f942-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f942-105">Syntax</span></span>

<span data-ttu-id="9f942-106">*Expression* . MovePrevious</span><span class="sxs-lookup"><span data-stu-id="9f942-106">*expression* .MovePrevious</span></span>

<span data-ttu-id="9f942-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="9f942-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f942-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f942-108">Remarks</span></span>

<span data-ttu-id="9f942-109">Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.</span><span class="sxs-lookup"><span data-stu-id="9f942-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="9f942-110">Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="9f942-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="9f942-111">Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9f942-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="9f942-112">Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="9f942-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="9f942-113">Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9f942-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="9f942-114">Если используется **MovePrevious** , когда первая запись является текущей, свойство **BOF** имеет **значение true**, а текущая запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9f942-114">If you use **MovePrevious** when the first record is current, the **BOF** property is **True**, and there is no current record.</span></span> <span data-ttu-id="9f942-115">При повторном использовании **MovePrevious** возникает ошибка, и **BOF** остается **true**.</span><span class="sxs-lookup"><span data-stu-id="9f942-115">If you use **MovePrevious** again, an error occurs, and **BOF** remains **True**.</span></span>

<span data-ttu-id="9f942-116">Если recordset указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение отвечает текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="9f942-116">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="9f942-117">Вы можете задать текущий индекс с помощью свойства **Index**.</span><span class="sxs-lookup"><span data-stu-id="9f942-117">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="9f942-118">Если не задать текущей индекс, порядок возвращаемых записей будет не определен.</span><span class="sxs-lookup"><span data-stu-id="9f942-118">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="9f942-119">Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="9f942-119">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="9f942-120">Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.</span><span class="sxs-lookup"><span data-stu-id="9f942-120">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

