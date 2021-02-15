---
title: Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288688"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="b4c8c-102">Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)</span><span class="sxs-lookup"><span data-stu-id="b4c8c-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="b4c8c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4c8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4c8c-104">Перемещается к первой, последней, следующей или предыдущей записи в указанном [объекте Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b4c8c-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4c8c-105">Syntax</span></span>

<span data-ttu-id="b4c8c-106">*DataControl*. Recordset. {</span><span class="sxs-lookup"><span data-stu-id="b4c8c-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="b4c8c-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="b4c8c-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="b4c8c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4c8c-108">Parameters</span></span>

|<span data-ttu-id="b4c8c-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="b4c8c-109">Parameter</span></span>|<span data-ttu-id="b4c8c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b4c8c-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b4c8c-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b4c8c-111">*DataControl*</span></span> |<span data-ttu-id="b4c8c-112">Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)</span><span class="sxs-lookup"><span data-stu-id="b4c8c-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b4c8c-113">Заметки</span><span class="sxs-lookup"><span data-stu-id="b4c8c-113">Remarks</span></span>

<span data-ttu-id="b4c8c-114">С RDS **можно** использовать методы **Move. Объект DataControl** для навигации по записям данных в привязанных к данным элементов управления на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="b4c8c-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="b4c8c-115">Например, предположим, что набор **записей** отображается в сетке путем привязки к **RDS. Объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="b4c8c-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="b4c8c-116">Затем можно включить кнопки "Первая", "Последняя", "Далее" и "Предыдущая", которые пользователи могут нажать, чтобы перейти к первой, последней, следующей или предыдущей записи в отображаемом наборе **записей.**</span><span class="sxs-lookup"><span data-stu-id="b4c8c-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="b4c8c-117">Для этого необходимо вызывать методы **MoveFirst,** **MoveLast,** **MoveNext** и **MovePrevious** **служб RDS. Объект DataControl** в процедурах onClick для кнопок First, Last, Next и Previous соответственно.</span><span class="sxs-lookup"><span data-stu-id="b4c8c-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="b4c8c-118">В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="b4c8c-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

