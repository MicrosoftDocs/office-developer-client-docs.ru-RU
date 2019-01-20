---
title: Метод Recordset.MoveFirst (DAO)
TOCTitle: MoveFirst Method
ms:assetid: 338f7e86-6997-b80a-fc7a-a395d10b4a62
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192329(v=office.15)
ms:contentKeyID: 48544109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 31d003d7ae98bf509aca8f24da9c37f0276af6fd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715727"
---
# <a name="recordsetmovefirst-method-dao"></a><span data-ttu-id="26a56-102">Метод Recordset.MoveFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="26a56-102">Recordset.MoveFirst Method (DAO)</span></span>


<span data-ttu-id="26a56-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26a56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26a56-104">Выполняет перемещение к первой записи в указанном объекте **Recordset** и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="26a56-104">Moves to the first record in a specified **Recordset** object and make that record the current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="26a56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26a56-105">Syntax</span></span>

<span data-ttu-id="26a56-106">*expression* .MoveFirst</span><span class="sxs-lookup"><span data-stu-id="26a56-106">*expression* .MoveFirst</span></span>

<span data-ttu-id="26a56-107">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="26a56-107">*expression* A variable that represents a **FileDialog** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="26a56-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26a56-108">Remarks</span></span>

<span data-ttu-id="26a56-109">Используйте методы **Move**, чтобы перейти от записи к записи, не применяя условие.</span><span class="sxs-lookup"><span data-stu-id="26a56-109">Use the **Move** methods to move from record to record without applying a condition.</span></span>

<span data-ttu-id="26a56-110">Если вы редактируете текущую запись, убедитесь, что вы используете метод **Update**, чтобы сохранить изменения, перед переходом к другой записи.</span><span class="sxs-lookup"><span data-stu-id="26a56-110">If you edit the current record, be sure you use the **Update** method to save the changes before you move to another record.</span></span> <span data-ttu-id="26a56-111">Если перейти к другой записи без обновления, изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="26a56-111">If you move to another record without updating, your changes are lost without warning.</span></span>

<span data-ttu-id="26a56-112">Когда вы открываете **Recordset**, первую запись является текущей, а свойство **BOF** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="26a56-112">When you open a **Recordset**, the first record is current and the **BOF** property is **False**.</span></span> <span data-ttu-id="26a56-113">Если **Recordset** не содержит записей, свойство **BOF** имеет значение **True**, а текущая запись отсутствует.</span><span class="sxs-lookup"><span data-stu-id="26a56-113">If the **Recordset** contains no records, the **BOF** property is **True**, and there is no current record.</span></span>

<span data-ttu-id="26a56-114">Если первая или последняя запись уже является текущей при использовании **MoveFirst** или **MoveLast**, текущая запись не меняется.</span><span class="sxs-lookup"><span data-stu-id="26a56-114">If the first or last record is already current when you use **MoveFirst** or **MoveLast**, the current record doesn't change.</span></span>

<span data-ttu-id="26a56-115">Если recordset указывает на табличный тип объекта **Recordset** (только для рабочих областей Microsoft Access), перемещение отвечает текущему индексу.</span><span class="sxs-lookup"><span data-stu-id="26a56-115">If recordset refers to a table-type **Recordset** (Microsoft Access workspaces only), movement follows the current index.</span></span> <span data-ttu-id="26a56-116">Вы можете задать текущий индекс с помощью свойства **Index**.</span><span class="sxs-lookup"><span data-stu-id="26a56-116">You can set the current index by using the **Index** property.</span></span> <span data-ttu-id="26a56-117">Если не задать текущей индекс, порядок возвращаемых записей будет не определен.</span><span class="sxs-lookup"><span data-stu-id="26a56-117">If you don't set the current index, the order of returned records is undefined.</span></span>

<span data-ttu-id="26a56-118">Вы не можете использовать методы **MoveFirst**, **MoveLast** и **MovePrevious** для объекта **Recordset** однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="26a56-118">You can't use the **MoveFirst**, **MoveLast**, and **MovePrevious** methods on a forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="26a56-119">Чтобы переместить положение текущей записи в объекте **Recordset** на определенное количество записей вперед или назад, используйте метод **Move**.</span><span class="sxs-lookup"><span data-stu-id="26a56-119">To move the position of the current record in a **Recordset** object a specific number of records forward or backward, use the **Move** method.</span></span>

