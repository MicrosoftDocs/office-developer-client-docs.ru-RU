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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716035"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="1d186-102">Методы MoveFirst, MoveLast, MoveNext и MovePrevious (RDS)</span><span class="sxs-lookup"><span data-stu-id="1d186-102">MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)</span></span>

<span data-ttu-id="1d186-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d186-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d186-104">Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d186-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d186-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d186-105">Syntax</span></span>

<span data-ttu-id="1d186-106">*DataControl*. Набор записей. {</span><span class="sxs-lookup"><span data-stu-id="1d186-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="1d186-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="1d186-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="1d186-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="1d186-108">Parameters</span></span>

|<span data-ttu-id="1d186-109">Параметр</span><span class="sxs-lookup"><span data-stu-id="1d186-109">Parameter</span></span>|<span data-ttu-id="1d186-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1d186-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1d186-111">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="1d186-111">*DataControl*</span></span> |<span data-ttu-id="1d186-112">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="1d186-112">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1d186-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d186-113">Remarks</span></span>

<span data-ttu-id="1d186-114">Можно использовать методы **перемещения** с **RDS. DataControl** объекта для перехода по записям данных в элементах управления с привязкой к данным на веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="1d186-114">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> 

<span data-ttu-id="1d186-115">Например предположим, что отображение **записей** в таблице путем привязки к **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="1d186-115">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="1d186-116">Первый, последний, Далее и назад кнопки, которая используется для перемещения на первый, последний, далее, затем можно включить или предыдущей записи в отображаемой **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="1d186-116">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="1d186-117">Это делается путем вызова **MoveFirst**, **MoveLast**, **MoveNext**и методы **MovePrevious** **RDS. DataControl** объект в процедуры onClick для кнопки первый, последний, Далее и назад, соответственно.</span><span class="sxs-lookup"><span data-stu-id="1d186-117">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="1d186-118">В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="1d186-118">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

