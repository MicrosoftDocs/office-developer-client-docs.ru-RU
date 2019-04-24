---
title: Свойство Recordset. Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307555"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="e8ef0-102">Свойство Recordset. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8ef0-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="e8ef0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8ef0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8ef0-104">Задает или возвращает значение, которое указывает операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="e8ef0-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="e8ef0-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="e8ef0-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ef0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8ef0-106">Syntax</span></span>

<span data-ttu-id="e8ef0-107">*Expression* . Тип</span><span class="sxs-lookup"><span data-stu-id="e8ef0-107">*expression* .Type</span></span>

<span data-ttu-id="e8ef0-108">*expression*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e8ef0-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ef0-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8ef0-109">Remarks</span></span>

<span data-ttu-id="e8ef0-110">Для объекта **Recordset** возможны следующие параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="e8ef0-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8ef0-111">Константа</span><span class="sxs-lookup"><span data-stu-id="e8ef0-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8ef0-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="e8ef0-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8ef0-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="e8ef0-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="e8ef0-114">Таблица (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="e8ef0-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ef0-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="e8ef0-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="e8ef0-116">Dynamic (только для рабочих областей ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="e8ef0-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="e8ef0-117"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="e8ef0-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="e8ef0-118">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e8ef0-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ef0-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="e8ef0-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="e8ef0-120">Типа dynaset</span><span class="sxs-lookup"><span data-stu-id="e8ef0-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ef0-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="e8ef0-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="e8ef0-122">Статически</span><span class="sxs-lookup"><span data-stu-id="e8ef0-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ef0-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="e8ef0-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="e8ef0-124">Только вперед</span><span class="sxs-lookup"><span data-stu-id="e8ef0-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

