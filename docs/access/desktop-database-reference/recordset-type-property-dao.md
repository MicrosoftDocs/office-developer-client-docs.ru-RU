---
title: Свойство Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707425"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="9779d-102">Свойство Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="9779d-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="9779d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9779d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9779d-104">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="9779d-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="9779d-105">Только для чтения **целое число**.</span><span class="sxs-lookup"><span data-stu-id="9779d-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9779d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9779d-106">Syntax</span></span>

<span data-ttu-id="9779d-107">*выражение* . Тип</span><span class="sxs-lookup"><span data-stu-id="9779d-107">*expression* .Type</span></span>

<span data-ttu-id="9779d-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="9779d-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9779d-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="9779d-109">Remarks</span></span>

<span data-ttu-id="9779d-110">Для объекта **набора записей** возможные параметры и возвращаемые значения, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9779d-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9779d-111">Константа</span><span class="sxs-lookup"><span data-stu-id="9779d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="9779d-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="9779d-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9779d-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="9779d-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="9779d-114">В таблице (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="9779d-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9779d-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="9779d-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="9779d-116">Динамические (только для рабочих областей технология ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="9779d-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="9779d-117"><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="9779d-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="9779d-118">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9779d-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9779d-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="9779d-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="9779d-120">Динамический набор</span><span class="sxs-lookup"><span data-stu-id="9779d-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9779d-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="9779d-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="9779d-122">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="9779d-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9779d-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="9779d-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="9779d-124">Только вперед</span><span class="sxs-lookup"><span data-stu-id="9779d-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

