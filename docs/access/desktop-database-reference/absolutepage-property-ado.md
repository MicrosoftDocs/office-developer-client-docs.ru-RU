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
# <a name="absolutepage-property-ado"></a><span data-ttu-id="5884e-102">Свойство AbsolutePage (ADO)</span><span class="sxs-lookup"><span data-stu-id="5884e-102">AbsolutePage property (ADO)</span></span>

<span data-ttu-id="5884e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5884e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5884e-104">Указывает, на какой странице располагается текущая запись.</span><span class="sxs-lookup"><span data-stu-id="5884e-104">Indicates on which page the current record resides.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5884e-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5884e-105">Settings and return values</span></span>

<span data-ttu-id="5884e-106">Задает или возвращает значение **типа Long** от 1 до числа страниц в объекте [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) или возвращает одно из значений [поситионенум](positionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="5884e-106">Sets or returns a **Long** value from 1 to the number of pages in the [Recordset](recordset-object-ado.md) object ([PageCount](pagecount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5884e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="5884e-107">Remarks</span></span>

<span data-ttu-id="5884e-108">Это свойство можно использовать для определения номера страницы, на которой расположена текущая запись.</span><span class="sxs-lookup"><span data-stu-id="5884e-108">This property can be used to identify the page number on which the current record is located.</span></span> <span data-ttu-id="5884e-109">Он использует свойство [pageSize](pagesize-property-ado.md) , чтобы логически разделить общее количество наборов строк объекта **Recordset** на серии страниц, каждая из которых содержит число записей, равное **pageSize** (за исключением последней страницы, которая может содержать меньше записей).</span><span class="sxs-lookup"><span data-stu-id="5884e-109">It uses the [PageSize](pagesize-property-ado.md) property to logically divide the total rowset count of the **Recordset** object into a series of pages, each of which has the number of records equal to **PageSize** (except for the last page, which may have fewer records).</span></span> <span data-ttu-id="5884e-110">Чтобы это свойство было доступно, поставщик должен поддерживать соответствующие функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="5884e-110">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="5884e-111">При извлечении или задании свойства **ABSOLUTEPAGE** ADO использует свойство [AbsolutePosition](absoluteposition-property-ado.md) и свойство [pageSize](pagesize-property-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5884e-111">When getting or setting the **AbsolutePage** property, ADO uses the [AbsolutePosition](absoluteposition-property-ado.md) property and the [PageSize](pagesize-property-ado.md) property together as follows:</span></span>

- <span data-ttu-id="5884e-112">Чтобы получить **AbsolutePage**, ADO сначала извлекает **AbsolutePosition**, а затем разделяет его на **pageSize**.</span><span class="sxs-lookup"><span data-stu-id="5884e-112">To get the **AbsolutePage**, ADO first retrieves the **AbsolutePosition**, and then divides it by the **PageSize**.</span></span>

- <span data-ttu-id="5884e-113">Чтобы задать **AbsolutePage**, ADO переместит **AbsolutePosition** следующим образом: он умножает значение **pageSize** на новое значение **AbsolutePage** , а затем добавляет 1 к значению.</span><span class="sxs-lookup"><span data-stu-id="5884e-113">To set the **AbsolutePage**, ADO moves the **AbsolutePosition** as follows: it multiplies the **PageSize** by the new **AbsolutePage** value and then adds 1 to the value.</span></span> <span data-ttu-id="5884e-114">В результате текущая позиция в **наборе записей** после успешной установки **AbsolutePage** является первой записью на этой странице.</span><span class="sxs-lookup"><span data-stu-id="5884e-114">As a result, the current position in the **Recordset** after successfully setting **AbsolutePage** is the first record in that page.</span></span>

<span data-ttu-id="5884e-115">Как и свойство **AbsolutePosition** , **AbsolutePage** имеет значение 1 и равняется 1, если текущая запись является первой записью в наборе **записей**.</span><span class="sxs-lookup"><span data-stu-id="5884e-115">Like the **AbsolutePosition** property, **AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="5884e-116">Задайте это свойство, чтобы перейти к первой записи определенной страницы.</span><span class="sxs-lookup"><span data-stu-id="5884e-116">Set this property to move to the first record of a particular page.</span></span> <span data-ttu-id="5884e-117">Получение общего числа страниц из свойства **PageCount** .</span><span class="sxs-lookup"><span data-stu-id="5884e-117">Obtain the total number of pages from the **PageCount** property.</span></span>

