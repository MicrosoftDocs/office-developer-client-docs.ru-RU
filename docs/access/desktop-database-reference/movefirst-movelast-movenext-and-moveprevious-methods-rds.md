---
title: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4671e57e3edb44bc1c927ca11f2cf79e70c2699
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481655"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="78119-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span><span class="sxs-lookup"><span data-stu-id="78119-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="78119-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="78119-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="78119-104">Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="78119-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="78119-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78119-105">Syntax</span></span>

<span data-ttu-id="78119-106">*DataControl*. Набор записей. {</span><span class="sxs-lookup"><span data-stu-id="78119-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="78119-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="78119-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="78119-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="78119-108">Parameters</span></span>

  - <span data-ttu-id="78119-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="78119-109">*DataControl*</span></span>

  - <span data-ttu-id="78119-110">Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="78119-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="78119-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="78119-111">Remarks</span></span>

<span data-ttu-id="78119-112">Можно использовать методы **перемещения** с **RDS. DataControl** объекта для перехода по записям данных в элементах управления с привязкой к данным на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="78119-112">You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a Web page.</span></span> <span data-ttu-id="78119-113">Например предположим, что отображение **записей** в таблице путем привязки к **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="78119-113">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="78119-114">Первый, последний, Далее и назад кнопки, которая используется для перемещения на первый, последний, далее, затем можно включить или предыдущей записи в отображаемой **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="78119-114">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="78119-115">Это делается путем вызова **MoveFirst**, **MoveLast**, **MoveNext**и методы **MovePrevious** **RDS. DataControl** объект в процедуры onClick для кнопки первый, последний, Далее и назад, соответственно.</span><span class="sxs-lookup"><span data-stu-id="78119-115">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="78119-116">В [примере адресной книги](address-book-navigation-buttons.md) показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="78119-116">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>

