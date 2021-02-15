---
title: Свойство Recordset2.Type (DAO)
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
# <a name="recordset2type-property-dao"></a><span data-ttu-id="01589-102">Свойство Recordset2.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="01589-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="01589-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01589-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01589-104">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="01589-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="01589-105">Только для чтения, **Integer**.</span><span class="sxs-lookup"><span data-stu-id="01589-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="01589-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01589-106">Syntax</span></span>

<span data-ttu-id="01589-107">*выражение* .Type</span><span class="sxs-lookup"><span data-stu-id="01589-107">*expression* .Type</span></span>

<span data-ttu-id="01589-108">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="01589-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="01589-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="01589-109">Remarks</span></span>

<span data-ttu-id="01589-110">Для объекта **Recordset** возможные параметры и возвращаемые значения:</span><span class="sxs-lookup"><span data-stu-id="01589-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01589-111">Константа</span><span class="sxs-lookup"><span data-stu-id="01589-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="01589-112">Тип recordset</span><span class="sxs-lookup"><span data-stu-id="01589-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01589-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="01589-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="01589-114">Таблица (только для рабочей области Microsoft Access)</span><span class="sxs-lookup"><span data-stu-id="01589-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01589-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="01589-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="01589-116">Динамический (только для рабочей области ODBCDirect)</span><span class="sxs-lookup"><span data-stu-id="01589-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="01589-117"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="01589-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="01589-118">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="01589-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01589-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="01589-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="01589-120">Dynaset</span><span class="sxs-lookup"><span data-stu-id="01589-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01589-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="01589-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="01589-122">Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="01589-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01589-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="01589-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="01589-124">Только для переад.</span><span class="sxs-lookup"><span data-stu-id="01589-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

