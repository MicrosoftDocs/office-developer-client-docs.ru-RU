---
title: Свойство AbsolutePage (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280686"
---
# <a name="absolutepage-property-ado"></a><span data-ttu-id="e8414-102">Свойство AbsolutePage (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8414-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="e8414-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8414-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8414-104">Указывает, на какой странице находится текущая запись.</span><span class="sxs-lookup"><span data-stu-id="e8414-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e8414-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="e8414-105">Settings and return values</span></span>

<span data-ttu-id="e8414-106">Задает или возвращает значение **Long** от 1 до количества страниц в объекте [Recordset](recordset-object-ado.md) [(PageCount)](pagecount-property-ado.md)или возвращает одно из [значений PositionEnum.](positionenum.md)</span><span class="sxs-lookup"><span data-stu-id="e8414-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8414-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8414-107">Remarks</span></span>

<span data-ttu-id="e8414-108">Это свойство можно использовать для определения номера страницы, на котором расположена текущая запись.</span><span class="sxs-lookup"><span data-stu-id="e8414-108">This property can be used to identify the page number on which the current record is located.</span></span> <span data-ttu-id="e8414-109">Свойство [PageSize](pagesize-property-ado.md) логически делит общее число строк объекта **Recordset** на ряд страниц, каждая из которых имеет количество записей, равное **PageSize** (за исключением последней страницы, записей может быть меньше).</span><span class="sxs-lookup"><span data-stu-id="e8414-109">It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records).</span></span> <span data-ttu-id="e8414-110">Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.</span><span class="sxs-lookup"><span data-stu-id="e8414-110">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="e8414-111">При получении или настройке **свойства AbsolutePage** ADO использует свойство [AbsolutePosition](absoluteposition-property-ado.md) и [свойство PageSize](pagesize-property-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e8414-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="e8414-112">Чтобы получить **AbsolutePage,** ADO сначала извлекает **AbsolutePosition,** а затем делит его на **PageSize.**</span><span class="sxs-lookup"><span data-stu-id="e8414-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="e8414-113">Чтобы установить **AbsolutePage,** ADO перемещает **AbsolutePosition** следующим образом: она умножает **PageSize** на новое значение **AbsolutePage** и добавляет 1 к значению.</span><span class="sxs-lookup"><span data-stu-id="e8414-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="e8414-114">В результате текущее положение в **Наборе записей** после успешного установки **AbsolutePage** является первой записью на этой странице.</span><span class="sxs-lookup"><span data-stu-id="e8414-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="e8414-115">Как и **свойство AbsolutePosition,** **AbsolutePage** основан на 1 и равен 1, когда текущая запись является первой записью в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="e8414-115">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="e8414-116">Установите это свойство, чтобы перейти к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="e8414-116">Set this property to move to the first record of a particular page.</span></span> <span data-ttu-id="e8414-117">Получение общего числа страниц из свойства **PageCount.**</span><span class="sxs-lookup"><span data-stu-id="e8414-117">Obtain the total number of pages from the **PageCount** property.</span></span>

