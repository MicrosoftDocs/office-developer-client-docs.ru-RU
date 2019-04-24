---
title: Свойство Recordset2. Type (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6646658daf482373ef8b62f6d3420b1d11152cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307177"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="d635a-102">Свойство Recordset2. Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="d635a-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="d635a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d635a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d635a-104">Задает или возвращает значение, которое указывает операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="d635a-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="d635a-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="d635a-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d635a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d635a-106">Syntax</span></span>

<span data-ttu-id="d635a-107">*Expression* . Тип</span><span class="sxs-lookup"><span data-stu-id="d635a-107">*expression* .Type</span></span>

<span data-ttu-id="d635a-108">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d635a-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d635a-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="d635a-109">Remarks</span></span>

<span data-ttu-id="d635a-110">Для объекта **Recordset** возможны следующие параметры и возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="d635a-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d635a-111">Константа</span><span class="sxs-lookup"><span data-stu-id="d635a-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="d635a-112">Тип набора записей</span><span class="sxs-lookup"><span data-stu-id="d635a-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d635a-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="d635a-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="d635a-114">Таблица (только для рабочих областей Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="d635a-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d635a-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="d635a-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="d635a-116">Dynamic (только для рабочих областей ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="d635a-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="d635a-117"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="d635a-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="d635a-118">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d635a-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d635a-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="d635a-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="d635a-120">Типа dynaset</span><span class="sxs-lookup"><span data-stu-id="d635a-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d635a-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="d635a-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="d635a-122">Статически</span><span class="sxs-lookup"><span data-stu-id="d635a-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d635a-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="d635a-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="d635a-124">Только вперед</span><span class="sxs-lookup"><span data-stu-id="d635a-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

