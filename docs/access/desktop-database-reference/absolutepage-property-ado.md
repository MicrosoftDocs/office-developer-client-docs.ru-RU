---
title: Свойство AbsolutePage (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a285f9f9533e4ecd903e6cc6c0e427bf44c84ca4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870536"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="eba9f-102">Свойство AbsolutePage (ADO)</span><span class="sxs-lookup"><span data-stu-id="eba9f-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="eba9f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eba9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eba9f-104">Указывает, на какую страницу находится текущей записи.</span><span class="sxs-lookup"><span data-stu-id="eba9f-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="eba9f-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="eba9f-105">Settings and return values</span></span>

<span data-ttu-id="eba9f-106">Задает или возвращает значение типа **Long** от 1 число страниц в объекте [набора записей](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="eba9f-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="eba9f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="eba9f-107">Remarks</span></span>

<span data-ttu-id="eba9f-108">Это свойство можно использовать для идентификации номер страницы, на котором расположена текущая запись.</span><span class="sxs-lookup"><span data-stu-id="eba9f-108">This property can be used to identify the page number on which the current record is located.</span></span> <span data-ttu-id="eba9f-109">Он использует свойство [PageSize](pagesize-property-ado.md) логическое разделение строк общее число объекта **набора записей** в набор страниц, каждый из которых содержит число записей, равное **PageSize** (за исключением на последней странице, которая может быть меньше записей).</span><span class="sxs-lookup"><span data-stu-id="eba9f-109">It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records).</span></span> <span data-ttu-id="eba9f-110">Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.</span><span class="sxs-lookup"><span data-stu-id="eba9f-110">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="eba9f-111">После получения и установки свойства **AbsolutePage** , ADO используется свойство [AbsolutePosition](absoluteposition-property-ado.md) и свойство [PageSize](pagesize-property-ado.md) вместе следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eba9f-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="eba9f-112">Для получения **AbsolutePage**ADO сначала получает **AbsolutePosition**и затем делит их **PageSize**.</span><span class="sxs-lookup"><span data-stu-id="eba9f-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="eba9f-113">Чтобы задать **AbsolutePage**, ADO перемещает **AbsolutePosition** , как показано ниже: его умножает **PageSize** на новое значение **AbsolutePage** и затем добавляет значение 1.</span><span class="sxs-lookup"><span data-stu-id="eba9f-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="eba9f-114">В результате текущую позицию в **наборе записей** после успешной установки **AbsolutePage** является первой записи в эту страницу.</span><span class="sxs-lookup"><span data-stu-id="eba9f-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="eba9f-115">Как и свойство **AbsolutePosition** **AbsolutePage** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="eba9f-115">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="eba9f-116">Задайте это свойство, чтобы перейти к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="eba9f-116">Set this property to move to the first record of a particular page.</span></span> <span data-ttu-id="eba9f-117">Получите общее число страниц из свойства **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="eba9f-117">Obtain the total number of pages from the **PageCount** property.</span></span>

